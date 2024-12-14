# SERP API Code Challenge

This document provides a solution to the SERP API Code Challenge. The original challenge description can be found [here](https://github.com/marselmustafin/serpapi-parsing-challenge/blob/master/CHALLENGE.md).

## Solution Overview

The core idea of the solution is to implement a scraper that employs multiple strategies for parsing the image gallery displayed at the top of the search results page. Since Google may return different results for similar queries each strategy relies on specific selectors and is encapsulated within its own class.


### Supported Cases

The solution currently handles the following cases:
<details> <summary> Van Gogh Paintings (challenge case) </summary> <img width="1512" alt="Screenshot 2024-12-14 at 18 07 23" src="https://github.com/user-attachments/assets/e77a592e-3505-468e-a48c-d488bd534d74" />
 </details> 
<details> <summary> List of Popes (another type of carousel) </summary>  <img width="1512" alt="list-of-popes" src="https://github.com/user-attachments/assets/9f51563b-df68-429c-a836-ecb076024f4b" /> </details>
<details> <summary> Red Hot Chili Peppers Members (grid) </summary> <img width="1512" alt="rhcp-members" src="https://github.com/user-attachments/assets/d97294bb-7d40-4f16-b572-c0d3e463d803" /> </details>
<details> <summary> Van Gogh Paintings (new request, another grid) </summary> <img width="1512" alt="van-gogh-paintings-new" src="https://github.com/user-attachments/assets/bded884d-6f23-4999-9a8f-11277bc4d9d1" /> </details>


### Commands

- `ruby scrape.rb` - runs scraper on all html documents and saves results in `files` dir.
- `bundle exec rspec --color spec/scraper/knowledge_graph_spec.rb` - runs tests

### Notes

*The solution may not cover all potential gallery types, as there appear to be many variations. However, it should effectively handle the listed cases and is designed to be extensible for future cases.*
