# loop
/loop batch=50
For each unprocessed word (limit 50):
  - Check etymology-zh-cn/etymology-zh-hk → fill if blank
git add/commit/push/pr/merge main branch per 500 words are updated.
Stop when all words in the book ielts.json are verified
Return: processed count, remaining count only

