# tag-test

### 1.tagからrelease作成
localで tagを作成し、GitHubへ push

Visual Studioで tagの設定はできるが、そのまま pushしても GitHubへは反映されなかった。
また tagを間違って付けたときVisualStudioで削除することもできなかった。
local gitを消すと VisualStudioで付けた tag情報は消えてしまうので注意。

ターミナルを利用し「git push origin タグ名」と pushすることで、対象 tagが GitHubへも反映される。

GitHubのtag（release）で対象の tagを選択し、release情報を登録する。
同じ tagがついている場合に、それを目印にソースが収集されるかは未確認。
（commitハッシュ情報を基に作成しているため、おそらく対象としたものだけを収集すると思われる　未確認）

gitコマンド
- git tag :tagの確認
- git push origin タグ名：tagのpush
- git tag -d タグ名：対象tagの削除。


### 2.GitHubでrelease情報作成
localで一切 tagを打たなくても GitHub上で releaseを行うことは可能。

1.で書いてあるように tagを目印にソースを収集するのかが重要なポイントとなる。
収集しないなら localで tagを打つ理由は個人的目印でしかない。
収集するなら releaseするうえで重要な情報となるため必須となる。

（その場合Visual Studioではターミナルを使用する必要が出てくる）

