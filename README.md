# mars_news_challenge

the last plot was difficult. Got assistance with the solutions from chat.openai.com

5. How many terrestrial (earth) days are there in a Martian year?
minimum_temperature_data = mars_df[['sol', 'min_temp']]
martian_year_in_sols = 687 # Length of a Martian year in Martian days (sols)
earth_days_in_a_martian_day = 1.0275 # Earth days in a Martian day (sol)

Calculate the number of terrestrial days for each Martian day
minimum_temperature_data['terrestrial_days'] = minimum_temperature_data['sol'] * earth_days_in_a_martian_day

Create a plot
plt.plot(minimum_temperature_data['terrestrial_days'], minimum_temperature_data['min_temp'])

Set plot labels and title
plt.xlabel('Number of Terrestrial Days')
plt.ylabel('Minimum Temperature (°C)')

plt.show()
