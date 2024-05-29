<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  cog.outl(f"# {config['name'].title()}")
]]]-->
# Argentina
<!--//[[[end]]]-->

## Mission

Tilt's mission is to map every theme to a basket of stocks for anyone to invest in. Mappings are AI generated and expert curated.
Expert improvements are accepted if they provide a better representation of a given theme.

## Theme Prompt
<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  cog.outl(config['prompt'])
]]]-->
Argentina's government is transitioning to be a champion of capitalism and free markets. Under the new leadership of Javier Milei, Argentinian companies can once again sell and profit from their incredible natural resources.
<!--[[[end]]]-->

## Theme Stocks

<!--[[[cog
import cog
import csv
import json

with open('context.json') as file:
  contexts = json.load(file)

def _get_context_str_for_ticker(ticker):
  try:
    context = contexts[ticker]
    context_str = context['chat_gpt'] or context['claude'] or ""
  except KeyError:
    context_str = ""

  return context_str

cog.outl("| Ticker  | Context | Source |")
cog.outl("| ------- | ---- | ---- |")

with open('theme.csv') as file:
  reader = csv.reader(file)
  next(reader) # skip the header
  for row in reader:
    context_str = _get_context_str_for_ticker(row[0])
    cog.outl(f"| {row[0]} | {context_str} | {row[1]} |")
]]]-->
| Ticker  | Context | Source |
| ------- | ---- | ---- |
| AGRO | Adecoagro, an agricultural company, will benefit from increased agricultural exports and market liberalization. Adecoagro, an agricultural company, will benefit from increased agricultural exports and market liberalization. | chat_gpt,google,claude |
| BBAR | BBVA Banco Frances, a major bank, will see growth from increased financial activity and market confidence. | chat_gpt,google,claude |
| BMA | Banco Macro, another major Argentinian bank, will benefit from increased economic activity and financial services demand. | chat_gpt,twitter,google,claude |
| CEPU | Central Puerto, a power generation company, stands to gain from increased demand for electricity and energy infrastructure investments. Central Puerto, a power generation company, stands to gain from increased demand for electricity and energy infrastructure investments. | chat_gpt,twitter,google,claude |
| CRESY | Cresud, a leading agricultural and real estate company, stands to gain from increased foreign investment and economic growth. Cresud, a leading agricultural and real estate company, stands to gain from increased foreign investment and economic growth. | chat_gpt,twitter,google,claude |
| EDN | Edenor, an electricity distribution company, will see growth from increased industrial activity and energy consumption. Edenor, an electricity distribution company, will see growth from increased industrial activity and energy consumption. | chat_gpt,google,claude |
| GGAL | Grupo Financiero Galicia is a leading financial institution in Argentina, likely to see growth from a more robust and open economy. | chat_gpt,twitter,google,claude |
| IRS | IRSA Inversiones y Representaciones, a real estate company, will benefit from a more stable and growing economy. | chat_gpt,google,claude |
| LOMA | Loma Negra, a leading cement producer, will benefit from increased construction and infrastructure projects. Loma Negra, a leading cement producer, will benefit from increased construction and infrastructure projects. | chat_gpt,google,claude |
| MELI | MercadoLibre, an e-commerce giant in Latin America, will benefit from increased consumer spending and economic stability. MercadoLibre, an e-commerce giant in Latin America, will benefit from increased consumer spending and economic stability. | chat_gpt,google,claude |
| PAM | Pampa Energia, a key player in Argentina's energy sector, stands to gain from deregulation and increased foreign investment. | chat_gpt,twitter,google,claude |
| SUPV | Grupo Supervielle, a financial services company, will benefit from a more open and growing economy. | chat_gpt,google,claude |
| TEO | Telecom Argentina, a telecommunications company, will see growth from increased demand for communication services. | chat_gpt,google,claude |
| TGS | Transportadora de Gas del Sur, a natural gas transportation company, will benefit from increased energy production and exports. Transportadora de Gas del Sur, a natural gas transportation company, will benefit from increased energy production and exports. | chat_gpt,twitter,google,claude |
| TX | Ternium, a steel manufacturer, will see growth from increased industrial activity and infrastructure development. Ternium, a steel manufacturer, will see growth from increased industrial activity and infrastructure development. | chat_gpt |
| VIST | Vista Oil & Gas, an oil and gas company, stands to gain from increased energy production and market liberalization. | chat_gpt,twitter,google |
| YPF | YPF is Argentina's largest energy company, poised to benefit from increased foreign investment and market liberalization. | chat_gpt,twitter,google,claude |
| GOLD |  | google |
| BIOX |  | google |
| LND |  | google |
| IBKR |  | google |
| XOM |  | google |
| CAAP | Corporación América Airports is a leading airport concession operator in Argentina and other Latin American countries. The company could benefit from increased air travel and tourism as the economy opens up and global connections expand. | claude |
| DESP | Despegar.com is the largest online travel agency in Argentina and Latin America, offering flights, hotels, packages, and other travel services. The company could benefit from increased tourism and travel as the economy opens up and global connections expand. | claude |
| GLOB | Globant is an Argentine software and IT services company, with a global presence and a focus on digital transformation, artificial intelligence, and customer experience. The company could benefit from increased demand for technology services as businesses seek to modernize and compete in the global economy. | claude |
<!--[[[end]]]-->

## License

<p>
This project is licensed under <a href="./LICENSE">AGPLv3</a>.
</p>


## Contributors

Thank you for your improvements! We appreciate all the contributions from the community.

<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  repo = config['github_repo'].lower()
  cog.outl(f'<a href="https://github.com/gettilt/{repo}/graphs/contributors">')
  cog.outl(f'  <img src="https://contrib.rocks/image?repo=gettilt/{repo}" />')
  cog.outl('</a>')
]]]-->
<a href="https://github.com/gettilt/argentina/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=gettilt/argentina" />
</a>
<!--[[[end]]]-->

## Join Our Community

<a href="https://discord.gg/4vYMhRpaMY" target="_blank">
<img src="https://discord.com/api/guilds/1179775688421683220/widget.png?style=banner3" alt="">
</a>
