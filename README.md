# helpful_python_code
Here is a bunch of things I find usefull


'''I will start entering some fun functions'''
## Here I combine all of the new text columns into one and just get rid of the extra dashes. I'm sure there 
## is an easier way to do this but I don't know hwo to do it yet. 
df['id'] = df[['col1','col2','col3','coln']].apply(lambda x: '-'.join(x.fillna('').map(str)), axis=1)

## Now I use the fun replace function to get rid of all of those pesky extra commas
rct_summary['check'] = rct_summary['check'].str.replace("----", "-")
rct_summary['check'] = rct_summary['check'].str.replace("---", "-")
rct_summary['check'] = rct_summary['check'].str.replace("--", "-")
rct_summary['check'] = rct_summary['check'].str.strip('-')
rct_summary.to_excel("doesitwork.xlsx")


