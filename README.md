# beautiful-soup-challenge
assistance recieved from tutoring.

 to answer exact estimate of number of martian days, following programming was inspired by chatGPT: 
start = df[df['ls'] == df['ls'].min()]['terrestrial_date'].iloc[0]
end = df[df['ls'] == df['ls'].max()]['terrestrial_date'].iloc[3]
days = (end - start).days

specific dtype constructs were made after consulting with chatgpt as well: 
df['id'] = df['id'].astype('category')
df['terrestrial_date'] = pd.to_datetime(df['terrestrial_date'])
df['sol'] = pd.to_numeric(df['sol'], errors='coerce').astype('int64')
df['ls'] = pd.to_numeric(df['ls'], errors='coerce').astype('int64')
df['month'] = pd.to_numeric(df['month'], errors='coerce').astype('int64')
df['min_temp'] = pd.to_numeric(df['min_temp'], errors='coerce').astype('float64')
df['pressure'] = pd.to_numeric(df['pressure'], errors='coerce').astype('float64')
df.dtypes


