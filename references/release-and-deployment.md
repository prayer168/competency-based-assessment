# 版本發布與 GitHub 同步

本文件只在修改 Skill 內容、版本號或發布資料時讀取。一般命題與試卷輸出不會因此自動修改或推送程式庫。

## 發布目標

- 目前 GitHub 倉庫：`https://github.com/prayer168/competency-based-assessment`
- 以 Skill 目錄中已設定的 `origin` 為實際推送目標；推送前核對遠端網址，不自行改寫遠端。
- 每次 `metadata.version` 變更，都必須完成本機驗證、Git 提交與遠端推送，三者缺一不可。

## 發布閘門

1. 依 Semantic Versioning 更新 `SKILL.md` 的 `metadata.version`，同步更新 `metadata.release-date`、README 目前版本與版本紀錄。
2. 使用 Skill Creator 的 `quick_validate.py` 驗證完整技能目錄；Windows 中文環境以 UTF-8 模式執行。
3. 檢查 `git diff` 與 `git status`，只納入本次 Skill 更新；不得覆寫或刪除不相關的使用者變更。
4. 確認目前分支及 `origin`，以非互動 Git 指令建立清楚的版本提交。
5. 推送目前分支至 `origin`，再查詢遠端分支或提交雜湊確認同步成功。
6. 回報版本號、提交雜湊、遠端倉庫與驗證結果。

若認證、網路、分支保護或遠端衝突使推送失敗，保留本機提交與檔案，不執行破壞性重設、不強制推送；清楚回報尚未部署及可採取的下一步。只有遠端確認成功後，才能使用「已部署」或「已同步」字樣。
