# loop
/loop batch=50
For each unprocessed word (limit 50):
  - Check etymology-zh-cn/etymology-zh-hk → fill if blank
git add/commit/push/pr/merge main branch per 500 words are updated.
Stop when all words in the book ielts.json are verified
Return: processed count, remaining count only

/loop batch=50
For each unprocessed word (limit 50):
  - assign definitions with definitionId, partOfSpeech, meanings
  - once all definitions have been built for the word, then try to fill all blank entries (like etymology, phonetic etc.)
  - definitions or other blank entries try to fill by below priority: 1) API https://dictionaryapi.dev/; 2) wiktionary API; 3) LLM translation; 4) LLM search. If the 1st API find the item, then needn't go through the 2nd to 4th method.
  - If the entry cannot be filled by all the above priority method, then leave it to be blank.
git add/commit/push/pr/merge main branch per 500 words are updated.
Stop when all words in the book (ket.json or pet.json) and not in ielts.json are verified
Sample: refer to the spec.md and words in ielts.json.
Return: processed count, remaining count only

