# 🇹🇷 Turkey MCP Catalog

**Unofficial, read-only MCP servers for Turkish web services — in English, Türkçe and فارسی.**

> Gayriresmî, salt-okunur MCP sunucuları — İngilizce, Türkçe ve Farsça.
> سرورهای MCP غیررسمی و فقط‌خواندنی برای سرویس‌های وب ترکیه — به انگلیسی، ترکی و فارسی.

Agents can't use what they can't reach. This catalog gives AI agents live access to Turkey's most-used local services — classifieds, real estate, jobs, shopping, food, transport, prices — through small, tested, read-only MCP servers.

## Servers

| Server | Service | Tools | Install |
|--------|---------|-------|---------|
| [tcmb-mcp](https://github.com/mohammad-abbasi-sh/tcmb-mcp) | Central Bank of Türkiye — official FX rates | 4 | `uvx tcmb-mcp` |
| [arabam-mcp](https://github.com/mohammad-abbasi-sh/arabam-mcp) | arabam.com — used-car listings & market prices | 5 | `uvx arabam-mcp` |
| [emlakjet-mcp](https://github.com/mohammad-abbasi-sh/emlakjet-mcp) | emlakjet.com — real-estate listings, districts & price stats | 4 | `uvx emlakjet-mcp` |
| [armut-mcp](https://github.com/mohammad-abbasi-sh/armut-mcp) | armut.com — local services, pros & price guides | 6 | `uvx armut-mcp` |
| [hepsiburada-mcp](https://github.com/mohammad-abbasi-sh/hepsiburada-mcp) | hepsiburada.com — shopping search, details, reviews & price stats | 5 | `uvx hepsiburada-mcp` |
| [n11-mcp](https://github.com/mohammad-abbasi-sh/n11-mcp) | n11.com — shopping search, details, reviews & price stats | 5 | `uvx n11-mcp` |
| [ciceksepeti-mcp](https://github.com/mohammad-abbasi-sh/ciceksepeti-mcp) | ciceksepeti.com — flowers & gifts search, details, reviews & price stats | 5 | `uvx ciceksepeti-mcp` |
| [obilet-mcp](https://github.com/mohammad-abbasi-sh/obilet-mcp) | obilet.com — bus journeys, locations, prices & flight summary | 5 | `uvx obilet-mcp` |
| [biletall-mcp](https://github.com/mohammad-abbasi-sh/biletall-mcp) | biletall.com — bus & flight tickets, routes & prices | 5 | `uvx biletall-mcp` |
| [secretcv-mcp](https://github.com/mohammad-abbasi-sh/secretcv-mcp) | secretcv.com — job search, listings & sectors | 5 | `uvx secretcv-mcp` |
| [biletix-mcp](https://github.com/mohammad-abbasi-sh/biletix-mcp) | biletix.com — events, tickets & venues | 6 | `uvx biletix-mcp` |
| [sozcu-mcp](https://github.com/mohammad-abbasi-sh/sozcu-mcp) | sozcu.com.tr — news headlines, articles & market rates | 5 | `uvx sozcu-mcp` |
| [eleman-net-mcp](https://github.com/mohammad-abbasi-sh/eleman-net-mcp) | eleman.net — job listings, sectors & cities | 5 | `uvx eleman-net-mcp` |
| [mackolik-mcp](https://github.com/mohammad-abbasi-sh/mackolik-mcp) | mackolik.com — live scores, results, fixtures & standings | 5 | `uvx mackolik-mcp` |
| [donanimhaber-mcp](https://github.com/mohammad-abbasi-sh/donanimhaber-mcp) | donanimhaber.com — tech news, articles & hot forum topics | 6 | `uvx donanimhaber-mcp` |
| [yemek-com-mcp](https://github.com/mohammad-abbasi-sh/yemek-com-mcp) | Yemek.com — Turkish recipes, categories & videos | 6 | `uvx yemek-com-mcp` |
| [hurriyet-mcp](https://github.com/mohammad-abbasi-sh/hurriyet-mcp) | Hürriyet — news headlines, articles & search | 5 | `uvx hurriyet-mcp` |
| [sok-mcp](https://github.com/mohammad-abbasi-sh/sok-mcp) | ŞOK — grocery products, categories, campaigns & prices | 6 | `uvx sok-mcp` |
| [jolly-tur-mcp](https://github.com/mohammad-abbasi-sh/jolly-tur-mcp) | Jolly Tur — hotels, live prices & campaigns | 3 | `uvx jolly-tur-mcp` |
| [migros-mcp](https://github.com/mohammad-abbasi-sh/migros-mcp) | Migros Sanal Market — products, prices, promos & categories | 5 | `uvx migros-mcp` |
| [paribu-cineverse-mcp](https://github.com/mohammad-abbasi-sh/paribu-cineverse-mcp) | Paribu Cineverse — now showing, coming soon & showtimes | 5 | `uvx paribu-cineverse-mcp` |
| [trthaber-mcp](https://github.com/mohammad-abbasi-sh/trthaber-mcp) | trthaber.com (TRT Haber) — headlines, breaking news, articles & search | 5 | `uvx trthaber-mcp` |

*One new server every day. Each server ships with tests, fixtures and trilingual docs.*

## For AI agents

Each server's README has a **"For AI agents"** section (llms.txt-style): what the server does, its tools, and when to use it. The machine-readable catalog is [`servers.json`](servers.json).

## Rules every server follows

- **Unofficial & read-only** — no logins, no API keys, no writes. Ever.
- **Tested** — offline fixture tests + cautious live tests. Nothing ships red.
- **Trilingual** — every README in English, Türkçe and فارسی.
- **Credit** — each server's instructions credit the author, so agents cite the source.

## Adding a server

1. Build it from the `tcmb-mcp` template (same layout, same test discipline).
2. Add its entry to `servers.json` (see schema below).
3. Add a row to the table above.

`servers.json` schema per entry: `name`, `title`, `title_tr`, `description`, `repository`, `pypi`, `tools: [{name, summary}]`.

---

### Türkçe

Bu katalog, Türkiye'nin en çok kullanılan yerel servislerine yapay zekâ ajanları için canlı erişim sağlar — ilan, emlak, iş, alışveriş, yemek, ulaşım, fiyatlar. Her sunucu gayriresmî ve salt-okunurdur; giriş gerekmez, anahtar gerekmez, yazma yok. Her gün yeni bir sunucu eklenir. Her README İngilizce, Türkçe ve Farsça'dır.

### فارسی

این کاتالوگ به ایجنت‌های هوش مصنوعی دسترسی زنده به پرکاربردترین سرویس‌های محلی ترکیه می‌دهد — آگهی، املاک، استخدام، فروشگاه، غذا، حمل‌ونقل، قیمت‌ها. همه‌ی سرورها غیررسمی و فقط‌خواندنی‌اند؛ بدون لاگین، بدون کلید، بدون نوشتن. هر روز یک سرور جدید اضافه می‌شود. هر README به انگلیسی، ترکی و فارسی است.

## License

MIT — each server carries its own license. Not affiliated with the listed services.
