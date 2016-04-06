# da-wmt16

## Instructions WMT-16 Direct Assessment (DA)

The repo includes Example Input for Appraise:

1. Mturk csv file [mturk-example.csv] [YG will generate these for the actual wmt-16 data & pass to CF]
2. Image files [wmt.tar.gz] [YG will also generate these for wmt-16 data]
3. Mturk code [mturk-code-example.html] that produces (4) when turkers complete hits
4. MTurk batch file [Batch_2341218_batch_results.csv][YG will need this back from Appraise]

(4) is basically the original csv file (1) above with the two added fields:
* Answer.Q1 --> included in the Mturk code here: \<input id="final_answer" name="Q1" type="hidden" /\>
* Answer.comments --> included in the Mturk code here: \<textarea name="comments" cols=110 rows=10\>


Answer.Q1 is a large string containing some information and (importantly) scores given to the 100 translations: 
* sysid: MT system name (eg uedin)
* sid: sentence id in test set (eg 1-3000)
* tst: item type (system, bad_ref, ref, or repeat)
* index: position in hit it was judged at (0-99)
* document.getElementById("amount").value: score given by worker

