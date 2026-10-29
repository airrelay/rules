# AirRoute 规则集

所有 `.list` 均为无出口动作的 classical 文本。中国大陆日常直连使用 `region/cn.list`，局域网使用 `special/lan.list`。具体服务域名通常放在分类、厂商总集和地区 IP 前。

中国大陆只提供 `region/cn.list`：国内域名优先，统一核查后的大陆 IP 兜底。地理意见来自 IPLocate 与 DB-IP；运营商清单、BGP 与公共 geofeed 是辅助线索，不投物理位置票。其他地区仅表达地理 IP。跨地区未决争议暂不归属，范围明确的高置信度完整 Anycast 单列，强 partial 候选隔离复核；无证据集合可仅含注释。

厂商总集可含其托管平台全部租户，云/CDN 集合表达基础设施，不能当作某个应用的专属身份。分类按用途筛选成员，供应商的宽范围例外不自动继承。DNS 观测与 CDN 地址不会被转为永久服务归属规则；同一主机上的不同 URL 功能无法只靠域名区分。进程、HTTP、ASN 等条件需要平台相应元数据。

## 国家地区

| 规则 | 文件 | 条数 |
|---|---|---:|
| 中国大陆 | [region/cn](region/cn.list) | 129622 |
| 港澳 | [region/hk-mo](region/hk-mo.list) | 15504 |
| 台湾 | [region/tw](region/tw.list) | 4297 |
| 东北亚 | [region/northeast-asia](region/northeast-asia.list) | 25281 |
| 东南亚 | [region/southeast-asia](region/southeast-asia.list) | 63657 |
| 南亚 | [region/south-asia](region/south-asia.list) | 24908 |
| 中亚 | [region/central-asia](region/central-asia.list) | 2990 |
| 西亚 | [region/west-asia](region/west-asia.list) | 29152 |
| 俄罗斯 | [region/ru](region/ru.list) | 23231 |
| 欧洲 | [region/europe](region/europe.list) | 373288 |
| 美国 | [region/us](region/us.list) | 280187 |
| 北美其他 | [region/north-america-other](region/north-america-other.list) | 35702 |
| 拉美与加勒比 | [region/latin-america-caribbean](region/latin-america-caribbean.list) | 46742 |
| 大洋洲 | [region/oceania](region/oceania.list) | 98481 |
| 非洲 | [region/africa](region/africa.list) | 14201 |
| 南极 | [region/antarctica](region/antarctica.list) | 62 |

## 分类服务

| 规则 | 文件 | 条数 |
|---|---|---:|
| 全部 AI | [category/ai-all](category/ai-all.list) | 341 |
| 中国大陆 AI | [category/ai-cn](category/ai-cn.list) | 116 |
| 海外 AI | [category/ai-overseas](category/ai-overseas.list) | 225 |
| CDN 与托管网络 | [category/cdn](category/cdn.list) | 217 |
| 云服务 | [category/cloud](category/cloud.list) | 518 |
| 容器与镜像仓库 | [category/containers](category/containers.list) | 19 |
| 开发与软件分发 | [category/development](category/development.list) | 697 |
| 教育与学习 | [category/education](category/education.list) | 16 |
| 游戏与平台 | [category/gaming](category/gaming.list) | 1241 |
| 邮件 | [category/mail](category/mail.list) | 13 |
| 会议与团队协作 | [category/meetings](category/meetings.list) | 34 |
| 即时通信 | [category/messaging](category/messaging.list) | 280 |
| 音乐 | [category/music](category/music.list) | 149 |
| 办公与设计 | [category/office-design](category/office-design.list) | 200 |
| Linux / BSD 开源发行 | [category/os](category/os.list) | 110 |
| 支付 | [category/payments](category/payments.list) | 597 |
| 播客 | [category/podcasts](category/podcasts.list) | 5 |
| 远程接入 | [category/remote](category/remote.list) | 16 |
| 学术与期刊 | [category/scholar](category/scholar.list) | 478 |
| 搜索与知识 | [category/search-knowledge](category/search-knowledge.list) | 95 |
| 购物与出行 | [category/shopping-travel](category/shopping-travel.list) | 559 |
| 社交与社区 | [category/social](category/social.list) | 829 |
| 网盘与同步 | [category/storage](category/storage.list) | 144 |
| 视频与直播 | [category/video](category/video.list) | 2047 |

## 服务商与产品

| 规则 | 文件 | 条数 |
|---|---|---:|
| Anthropic / Claude | [provider/anthropic](provider/anthropic.list) | 19 |
| Arena | [provider/arena](provider/arena.list) | 1 |
| Cerebras | [provider/cerebras](provider/cerebras.list) | 1 |
| Chutes | [provider/chutes](provider/chutes.list) | 1 |
| Cline | [provider/cline](provider/cline.list) | 1 |
| CodeRabbit | [provider/coderabbit](provider/coderabbit.list) | 2 |
| Cohere | [provider/cohere](provider/cohere.list) | 2 |
| Comfy | [provider/comfy](provider/comfy.list) | 4 |
| Context7 | [provider/context7](provider/context7.list) | 1 |
| CrewAI | [provider/crewai](provider/crewai.list) | 1 |
| Cursor | [provider/cursor](provider/cursor.list) | 5 |
| DeepWiki | [provider/deepwiki](provider/deepwiki.list) | 2 |
| Devin | [provider/devin](provider/devin.list) | 1 |
| Dify | [provider/dify](provider/dify.list) | 1 |
| ElevenLabs | [provider/elevenlabs](provider/elevenlabs.list) | 2 |
| GitHub Copilot | [provider/github-copilot](provider/github-copilot.list) | 6 |
| Google AI / Gemini / NotebookLM | [provider/google-ai](provider/google-ai.list) | 48 |
| Groq | [provider/groq](provider/groq.list) | 1 |
| Hugging Face | [provider/huggingface](provider/huggingface.list) | 3 |
| JetBrains AI | [provider/jetbrains-ai](provider/jetbrains-ai.list) | 3 |
| Kiro | [provider/kiro](provider/kiro.list) | 1 |
| LangChain | [provider/langchain](provider/langchain.list) | 1 |
| LM Studio | [provider/lm-studio](provider/lm-studio.list) | 1 |
| Lovart | [provider/lovart](provider/lovart.list) | 1 |
| Manus | [provider/manus](provider/manus.list) | 2 |
| Meta AI | [provider/meta-ai](provider/meta-ai.list) | 3 |
| Microsoft Copilot | [provider/microsoft-copilot](provider/microsoft-copilot.list) | 10 |
| Midjourney | [provider/midjourney](provider/midjourney.list) | 1 |
| Mistral | [provider/mistral](provider/mistral.list) | 1 |
| Ollama | [provider/ollama](provider/ollama.list) | 1 |
| OpenAI | [provider/openai](provider/openai.list) | 26 |
| OpenArt | [provider/openart](provider/openart.list) | 1 |
| OpenClaw | [provider/openclaw](provider/openclaw.list) | 2 |
| OpenCode | [provider/opencode](provider/opencode.list) | 1 |
| OpenRouter | [provider/openrouter](provider/openrouter.list) | 1 |
| Perplexity | [provider/perplexity](provider/perplexity.list) | 5 |
| Poe | [provider/poe](provider/poe.list) | 2 |
| Qoder | [provider/qoder](provider/qoder.list) | 1 |
| Sider | [provider/sider](provider/sider.list) | 1 |
| Tripo3D | [provider/tripo3d](provider/tripo3d.list) | 1 |
| Windsurf | [provider/windsurf](provider/windsurf.list) | 4 |
| xAI / Grok | [provider/xai](provider/xai.list) | 4 |
| YouMind | [provider/youmind](provider/youmind.list) | 3 |
| Akamai | [provider/akamai](provider/akamai.list) | 81 |
| AWS | [provider/aws](provider/aws.list) | 80 |
| Azure 云与托管网络 | [provider/azure](provider/azure.list) | 151 |
| Cloudflare 网络与托管平台 | [provider/cloudflare](provider/cloudflare.list) | 98 |
| DigitalOcean | [provider/digitalocean](provider/digitalocean.list) | 6 |
| Fastly | [provider/fastly](provider/fastly.list) | 7 |
| Firebase | [provider/firebase](provider/firebase.list) | 21 |
| Heroku 托管平台 | [provider/heroku](provider/heroku.list) | 12 |
| Hetzner | [provider/hetzner](provider/hetzner.list) | 14 |
| Netlify 托管平台 | [provider/netlify](provider/netlify.list) | 10 |
| Oracle | [provider/oracle](provider/oracle.list) | 25 |
| Vercel 托管平台 | [provider/vercel](provider/vercel.list) | 30 |
| Vultr | [provider/vultr](provider/vultr.list) | 1 |
| Adobe | [provider/adobe](provider/adobe.list) | 141 |
| AnyDesk | [provider/anydesk](provider/anydesk.list) | 1 |
| Atlassian | [provider/atlassian](provider/atlassian.list) | 11 |
| Canva | [provider/canva](provider/canva.list) | 6 |
| Dropbox | [provider/dropbox](provider/dropbox.list) | 25 |
| Figma | [provider/figma](provider/figma.list) | 1 |
| Google Drive | [provider/google-drive](provider/google-drive.list) | 4 |
| MEGA | [provider/mega](provider/mega.list) | 18 |
| NoMachine | [provider/nomachine](provider/nomachine.list) | 1 |
| Notion | [provider/notion](provider/notion.list) | 8 |
| PikPak | [provider/pikpak](provider/pikpak.list) | 7 |
| RustDesk | [provider/rustdesk](provider/rustdesk.list) | 1 |
| Tailscale | [provider/tailscale](provider/tailscale.list) | 3 |
| TeamViewer | [provider/teamviewer](provider/teamviewer.list) | 11 |
| TeraBox | [provider/terabox](provider/terabox.list) | 7 |
| Trello | [provider/trello](provider/trello.list) | 2 |
| Zendesk | [provider/zendesk](provider/zendesk.list) | 6 |
| Zoho | [provider/zoho](provider/zoho.list) | 13 |
| Apple | [provider/apple](provider/apple.list) | 1628 |
| Apple 开发者 | [provider/apple-dev](provider/apple-dev.list) | 40 |
| Apple Intelligence | [provider/apple-intelligence](provider/apple-intelligence.list) | 5 |
| Apple Music | [provider/apple-music](provider/apple-music.list) | 19 |
| Apple Podcasts | [provider/apple-podcasts](provider/apple-podcasts.list) | 2 |
| Apple TV | [provider/apple-tvplus](provider/apple-tvplus.list) | 9 |
| Apple 更新下载 | [provider/apple-update](provider/apple-update.list) | 21 |
| App Store | [provider/appstore](provider/appstore.list) | 2 |
| Bing | [provider/bing](provider/bing.list) | 33 |
| Google | [provider/google](provider/google.list) | 891 |
| Google Play | [provider/google-play](provider/google-play.list) | 9 |
| Google Search | [provider/googlesearch](provider/googlesearch.list) | 2 |
| iCloud | [provider/icloud](provider/icloud.list) | 60 |
| Microsoft | [provider/microsoft](provider/microsoft.list) | 760 |
| Microsoft 开发工具 | [provider/microsoft-dev](provider/microsoft-dev.list) | 74 |
| Microsoft 365 / Office | [provider/microsoft-office](provider/microsoft-office.list) | 19 |
| Microsoft Teams | [provider/microsoft-teams](provider/microsoft-teams.list) | 4 |
| Mozilla / Firefox | [provider/mozilla](provider/mozilla.list) | 74 |
| OneDrive / SharePoint | [provider/onedrive](provider/onedrive.list) | 21 |
| Outlook | [provider/outlook](provider/outlook.list) | 2 |
| TestFlight | [provider/testflight](provider/testflight.list) | 2 |
| Windows 更新 | [provider/windows-update](provider/windows-update.list) | 9 |
| Anaconda | [provider/anaconda](provider/anaconda.list) | 4 |
| Apache | [provider/apache](provider/apache.list) | 1 |
| Arch Linux | [provider/archlinux](provider/archlinux.list) | 6 |
| Azure Container Registry | [provider/azure-container-registry](provider/azure-container-registry.list) | 1 |
| Ubuntu / Canonical | [provider/canonical](provider/canonical.list) | 60 |
| Chocolatey | [provider/chocolatey](provider/chocolatey.list) | 1 |
| Codeberg | [provider/codeberg](provider/codeberg.list) | 2 |
| Dart | [provider/dart](provider/dart.list) | 3 |
| Debian | [provider/debian](provider/debian.list) | 2 |
| Deno | [provider/deno](provider/deno.list) | 2 |
| Docker | [provider/docker](provider/docker.list) | 10 |
| Fedora | [provider/fedora](provider/fedora.list) | 6 |
| Flatpak | [provider/flatpak](provider/flatpak.list) | 2 |
| Flutter | [provider/flutter](provider/flutter.list) | 3 |
| FreeBSD | [provider/freebsd](provider/freebsd.list) | 1 |
| GitBook | [provider/gitbook](provider/gitbook.list) | 3 |
| GitHub | [provider/github](provider/github.list) | 63 |
| GitHub Container Registry | [provider/github-container-registry](provider/github-container-registry.list) | 1 |
| GitLab | [provider/gitlab](provider/gitlab.list) | 7 |
| GitLab Registry | [provider/gitlab-registry](provider/gitlab-registry.list) | 1 |
| GNU | [provider/gnu](provider/gnu.list) | 1 |
| Go | [provider/golang](provider/golang.list) | 8 |
| Google Container Registry | [provider/google-container-registry](provider/google-container-registry.list) | 1 |
| HashiCorp | [provider/hashicorp](provider/hashicorp.list) | 8 |
| Haskell | [provider/haskell](provider/haskell.list) | 3 |
| Homebrew | [provider/homebrew](provider/homebrew.list) | 2 |
| Java | [provider/java](provider/java.list) | 2 |
| JetBrains | [provider/jetbrains](provider/jetbrains.list) | 24 |
| JFrog | [provider/jfrog](provider/jfrog.list) | 4 |
| Kubernetes | [provider/kubernetes](provider/kubernetes.list) | 2 |
| Kubernetes Registry | [provider/kubernetes-registry](provider/kubernetes-registry.list) | 1 |
| Microsoft Container Registry | [provider/microsoft-container-registry](provider/microsoft-container-registry.list) | 1 |
| MongoDB | [provider/mongodb](provider/mongodb.list) | 2 |
| MSYS2 | [provider/msys2](provider/msys2.list) | 1 |
| NGINX | [provider/nginx](provider/nginx.list) | 2 |
| NixOS | [provider/nixos](provider/nixos.list) | 12 |
| NodeSource | [provider/nodesource](provider/nodesource.list) | 1 |
| npm | [provider/npmjs](provider/npmjs.list) | 3 |
| OpenWrt | [provider/openwrt](provider/openwrt.list) | 2 |
| Packagist | [provider/packagist](provider/packagist.list) | 1 |
| Perl | [provider/perl](provider/perl.list) | 5 |
| PHP | [provider/php](provider/php.list) | 1 |
| PostgreSQL | [provider/postgresql](provider/postgresql.list) | 1 |
| Postman | [provider/postman](provider/postman.list) | 1 |
| Python / PyPI | [provider/python](provider/python.list) | 6 |
| Qt | [provider/qt](provider/qt.list) | 2 |
| Quay | [provider/quay](provider/quay.list) | 1 |
| Read the Docs | [provider/readthedocs](provider/readthedocs.list) | 4 |
| Red Hat | [provider/redhat](provider/redhat.list) | 2 |
| Redis | [provider/redis](provider/redis.list) | 2 |
| Ruby | [provider/ruby](provider/ruby.list) | 2 |
| Rust / Cargo | [provider/rust](provider/rust.list) | 4 |
| Scala | [provider/scala](provider/scala.list) | 2 |
| Scoop | [provider/scoop](provider/scoop.list) | 1 |
| SourceHut | [provider/sourcehut](provider/sourcehut.list) | 2 |
| SQLite | [provider/sqlite](provider/sqlite.list) | 1 |
| Stack Exchange / Stack Overflow | [provider/stackexchange](provider/stackexchange.list) | 25 |
| Termux | [provider/termux](provider/termux.list) | 3 |
| Linux Foundation | [provider/thelinuxfoundation](provider/thelinuxfoundation.list) | 16 |
| Unity | [provider/unity](provider/unity.list) | 10 |
| unpkg | [provider/unpkg](provider/unpkg.list) | 1 |
| Yarn | [provider/yarn](provider/yarn.list) | 1 |
| Zig | [provider/zig](provider/zig.list) | 1 |
| Battle.net / Blizzard | [provider/blizzard](provider/blizzard.list) | 64 |
| Bohemia | [provider/bohemia](provider/bohemia.list) | 9 |
| CurseForge | [provider/curseforge](provider/curseforge.list) | 2 |
| Cygames | [provider/cygames](provider/cygames.list) | 5 |
| EA | [provider/ea](provider/ea.list) | 165 |
| Epic Games | [provider/epicgames](provider/epicgames.list) | 34 |
| Faceit | [provider/faceit](provider/faceit.list) | 2 |
| Gaijin | [provider/gaijin](provider/gaijin.list) | 13 |
| Gamesplanet | [provider/gamesplanet](provider/gamesplanet.list) | 3 |
| Garena | [provider/garena](provider/garena.list) | 16 |
| GOG | [provider/gog](provider/gog.list) | 8 |
| Humble Bundle | [provider/humblebundle](provider/humblebundle.list) | 2 |
| itch.io | [provider/itchio](provider/itchio.list) | 2 |
| Konami | [provider/konami](provider/konami.list) | 19 |
| HoYoverse 国际 | [provider/mihoyo](provider/mihoyo.list) | 25 |
| Modrinth | [provider/modrinth](provider/modrinth.list) | 1 |
| Nexon | [provider/nexon](provider/nexon.list) | 6 |
| Nexus Mods | [provider/nexusmods](provider/nexusmods.list) | 2 |
| Nintendo | [provider/nintendo](provider/nintendo.list) | 128 |
| osu! | [provider/osu](provider/osu.list) | 9 |
| PlayStation | [provider/playstation](provider/playstation.list) | 4 |
| PUBG | [provider/pubg](provider/pubg.list) | 4 |
| Riot | [provider/riot](provider/riot.list) | 55 |
| Roblox | [provider/roblox](provider/roblox.list) | 51 |
| Steam | [provider/steam](provider/steam.list) | 78 |
| Supercell | [provider/supercell](provider/supercell.list) | 45 |
| Take-Two / Rockstar | [provider/take-two](provider/take-two.list) | 17 |
| Ubisoft | [provider/ubisoft](provider/ubisoft.list) | 31 |
| VRChat | [provider/vrchat](provider/vrchat.list) | 3 |
| Wargaming | [provider/wargaming](provider/wargaming.list) | 12 |
| Warner Bros. Games | [provider/wbgames](provider/wbgames.list) | 6 |
| Xbox | [provider/xbox](provider/xbox.list) | 48 |
| Yostar | [provider/yostar](provider/yostar.list) | 9 |
| ACM | [provider/acm](provider/acm.list) | 1 |
| Airbnb | [provider/airbnb](provider/airbnb.list) | 83 |
| Amazon 生态（含 AWS） | [provider/amazon](provider/amazon.list) | 261 |
| Internet Archive | [provider/archive](provider/archive.list) | 18 |
| arXiv | [provider/arxiv](provider/arxiv.list) | 1 |
| Booking | [provider/booking](provider/booking.list) | 3 |
| Coursera | [provider/coursera](provider/coursera.list) | 4 |
| DuckDuckGo | [provider/duckduckgo](provider/duckduckgo.list) | 44 |
| Duolingo | [provider/duolingo](provider/duolingo.list) | 2 |
| eBay | [provider/ebay](provider/ebay.list) | 370 |
| edX | [provider/edx](provider/edx.list) | 2 |
| Elsevier | [provider/elsevier](provider/elsevier.list) | 14 |
| Google Scholar | [provider/google-scholar](provider/google-scholar.list) | 76 |
| IEEE | [provider/ieee](provider/ieee.list) | 54 |
| Mastercard | [provider/mastercard](provider/mastercard.list) | 184 |
| O'Reilly | [provider/oreilly](provider/oreilly.list) | 6 |
| PayPal | [provider/paypal](provider/paypal.list) | 246 |
| Rakuten | [provider/rakuten](provider/rakuten.list) | 36 |
| ResearchGate | [provider/researchgate](provider/researchgate.list) | 1 |
| Shopee 国际 | [provider/shopee](provider/shopee.list) | 21 |
| Shopify | [provider/shopify](provider/shopify.list) | 8 |
| Springer Nature | [provider/springer](provider/springer.list) | 5 |
| Stripe | [provider/stripe](provider/stripe.list) | 8 |
| Uber | [provider/uber](provider/uber.list) | 3 |
| Udemy | [provider/udemy](provider/udemy.list) | 2 |
| Visa | [provider/visa](provider/visa.list) | 160 |
| Wikipedia / Wikimedia | [provider/wikimedia](provider/wikimedia.list) | 19 |
| ABEMA | [provider/abema](provider/abema.list) | 23 |
| 巴哈姆特动画疯 | [provider/bahamut](provider/bahamut.list) | 7 |
| Bandcamp | [provider/bandcamp](provider/bandcamp.list) | 2 |
| BBC | [provider/bbc](provider/bbc.list) | 33 |
| Bilibili International | [provider/bilibili-international](provider/bilibili-international.list) | 2 |
| Catchplay | [provider/catchplay](provider/catchplay.list) | 2 |
| Crunchyroll | [provider/crunchyroll](provider/crunchyroll.list) | 1 |
| Dailymotion | [provider/dailymotion](provider/dailymotion.list) | 5 |
| DAZN | [provider/dazn](provider/dazn.list) | 18 |
| Deezer | [provider/deezer](provider/deezer.list) | 2 |
| Discovery+ | [provider/discoveryplus](provider/discoveryplus.list) | 14 |
| Disney+ / Hulu 关联服务 | [provider/disney](provider/disney.list) | 236 |
| Emby | [provider/emby](provider/emby.list) | 49 |
| F1 | [provider/formula1](provider/formula1.list) | 3 |
| friDay | [provider/friday](provider/friday.list) | 2 |
| Hami Video | [provider/hamivideo](provider/hamivideo.list) | 20 |
| HBO / Max | [provider/hbo](provider/hbo.list) | 87 |
| Hulu 日本 | [provider/hulujp](provider/hulujp.list) | 5 |
| IMDb | [provider/imdb](provider/imdb.list) | 4 |
| ITV | [provider/itv](provider/itv.list) | 3 |
| JOOX | [provider/joox](provider/joox.list) | 6 |
| Kick | [provider/kick](provider/kick.list) | 1 |
| KKBOX | [provider/kkbox](provider/kkbox.list) | 9 |
| KKTV | [provider/kktv](provider/kktv.list) | 4 |
| Last.fm | [provider/lastfm](provider/lastfm.list) | 32 |
| LiTV | [provider/litv](provider/litv.list) | 12 |
| MOOV | [provider/moov](provider/moov.list) | 2 |
| MUBI | [provider/mubi](provider/mubi.list) | 2 |
| myTVSUPER | [provider/mytvsuper](provider/mytvsuper.list) | 4 |
| Netflix | [provider/netflix](provider/netflix.list) | 1153 |
| Niconico | [provider/niconico](provider/niconico.list) | 11 |
| Now | [provider/now](provider/now.list) | 7 |
| Overcast | [provider/overcast](provider/overcast.list) | 1 |
| Paramount+ | [provider/paramountplus](provider/paramountplus.list) | 9 |
| PBS | [provider/pbs](provider/pbs.list) | 1 |
| Peacock | [provider/peacock](provider/peacock.list) | 1 |
| Plex | [provider/plex](provider/plex.list) | 4 |
| Pluto TV | [provider/plutotv](provider/plutotv.list) | 2 |
| Pocket Casts | [provider/pocketcasts](provider/pocketcasts.list) | 2 |
| Prime Video | [provider/primevideo](provider/primevideo.list) | 30 |
| Qobuz | [provider/qobuz](provider/qobuz.list) | 33 |
| Radiko | [provider/radiko](provider/radiko.list) | 3 |
| Roku | [provider/roku](provider/roku.list) | 6 |
| Sling | [provider/sling](provider/sling.list) | 5 |
| SoundCloud | [provider/soundcloud](provider/soundcloud.list) | 4 |
| Spotify | [provider/spotify](provider/spotify.list) | 32 |
| TheTVDB | [provider/thetvdb](provider/thetvdb.list) | 1 |
| TIDAL | [provider/tidal](provider/tidal.list) | 4 |
| TikTok | [provider/tiktok](provider/tiktok.list) | 56 |
| TMDB | [provider/tmdb](provider/tmdb.list) | 4 |
| TVB | [provider/tvb](provider/tvb.list) | 22 |
| TVer | [provider/tver](provider/tver.list) | 6 |
| Twitch | [provider/twitch](provider/twitch.list) | 49 |
| U-NEXT | [provider/unext](provider/unext.list) | 4 |
| Vimeo | [provider/vimeo](provider/vimeo.list) | 17 |
| Viu | [provider/viu](provider/viu.list) | 7 |
| ViuTV | [provider/viutv](provider/viutv.list) | 9 |
| WeTV | [provider/wetv](provider/wetv.list) | 9 |
| YouTube | [provider/youtube](provider/youtube.list) | 183 |
| YouTube Music | [provider/youtube-music](provider/youtube-music.list) | 1 |
| Zee | [provider/zee](provider/zee.list) | 22 |
| Bluesky | [provider/bluesky](provider/bluesky.list) | 3 |
| Discord | [provider/discord](provider/discord.list) | 29 |
| Disqus | [provider/disqus](provider/disqus.list) | 4 |
| Facebook | [provider/facebook](provider/facebook.list) | 572 |
| Imgur | [provider/imgur](provider/imgur.list) | 3 |
| Instagram | [provider/instagram](provider/instagram.list) | 73 |
| Intercom | [provider/intercom](provider/intercom.list) | 2 |
| KakaoTalk | [provider/kakao](provider/kakao.list) | 65 |
| Keybase | [provider/keybase](provider/keybase.list) | 2 |
| LINE | [provider/line](provider/line.list) | 36 |
| LinkedIn | [provider/linkedin](provider/linkedin.list) | 12 |
| Mail.com | [provider/mailcom](provider/mailcom.list) | 4 |
| Mastodon | [provider/mastodon](provider/mastodon.list) | 3 |
| Matrix | [provider/matrix](provider/matrix.list) | 9 |
| Messenger | [provider/messenger](provider/messenger.list) | 4 |
| Misskey | [provider/misskey](provider/misskey.list) | 34 |
| Patreon | [provider/patreon](provider/patreon.list) | 4 |
| Pinterest | [provider/pinterest](provider/pinterest.list) | 52 |
| Pixiv | [provider/pixiv](provider/pixiv.list) | 12 |
| Proton Mail | [provider/protonmail](provider/protonmail.list) | 7 |
| Quora | [provider/quora](provider/quora.list) | 6 |
| Reddit | [provider/reddit](provider/reddit.list) | 15 |
| Signal | [provider/signal](provider/signal.list) | 8 |
| Slack | [provider/slack](provider/slack.list) | 11 |
| Snapchat | [provider/snap](provider/snap.list) | 9 |
| TeamSpeak | [provider/teamspeak](provider/teamspeak.list) | 3 |
| Telegram | [provider/telegram](provider/telegram.list) | 48 |
| Threads | [provider/threads](provider/threads.list) | 2 |
| Tumblr | [provider/tumblr](provider/tumblr.list) | 3 |
| X / Twitter | [provider/twitter](provider/twitter.list) | 33 |
| Viber | [provider/viber](provider/viber.list) | 6 |
| VK | [provider/vk](provider/vk.list) | 38 |
| Webex | [provider/webex](provider/webex.list) | 16 |
| WhatsApp | [provider/whatsapp](provider/whatsapp.list) | 25 |
| Zoom | [provider/zoom](provider/zoom.list) | 3 |

## 特殊用途

| 规则 | 文件 | 条数 |
|---|---|---:|
| 广告域名 | [special/ads](special/ads.list) | 38534 |
| Apple APNs | [special/apns](special/apns.list) | 2 |
| 门户与联网检测 | [special/connectivity](special/connectivity.list) | 24 |
| 软件与内容下载 | [special/downloads](special/downloads.list) | 34 |
| 加密 DNS 端点 | [special/encrypted-dns](special/encrypted-dns.list) | 203 |
| Google FCM | [special/fcm](special/fcm.list) | 41 |
| 游戏平台下载 | [special/game-downloads](special/game-downloads.list) | 491 |
| 已知劫持端点 | [special/hijacking](special/hijacking.list) | 228 |
| 中国大陆 HTTPDNS | [special/httpdns-cn](special/httpdns-cn.list) | 91 |
| 局域网 | [special/lan](special/lan.list) | 106 |
| 网络授时 | [special/ntp](special/ntp.list) | 169 |
| Apple/Microsoft 证书验证端点 | [special/pki](special/pki.list) | 14 |
| iCloud Private Relay | [special/private-relay](special/private-relay.list) | 6 |
| PT 站点 | [special/private-trackers](special/private-trackers.list) | 306 |
| 公开 BT Tracker | [special/public-trackers](special/public-trackers.list) | 431 |
| 测速服务 | [special/speedtest](special/speedtest.list) | 329 |
| Steam 大陆下载 | [special/steam-cn-downloads](special/steam-cn-downloads.list) | 22 |
| STUN 发现端点 | [special/stun](special/stun.list) | 535 |
| 遥测与跟踪 | [special/telemetry](special/telemetry.list) | 40126 |
| Windows WNS | [special/wns](special/wns.list) | 1 |
| Anycast（高置信度范围） | [special/anycast](special/anycast.list) | 8544 |

## 来源与许可

域名来自 [v2fly/domain-list-community](https://github.com/v2fly/domain-list-community)（MIT）、[blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script)（GPL-2.0）、[dnsmasq-china-list](https://github.com/felixonmars/dnsmasq-china-list)（WTFPL）。中国网络辅助分类来自 [gaoyifan/china-operator-ip](https://github.com/gaoyifan/china-operator-ip)（MIT）。地理原料 powered by [IPLocate.io](https://www.iplocate.io)（CC BY-SA 4.0）与 [DB-IP Lite](https://db-ip.com/db/download/ip-to-country-lite)（CC BY 4.0）。数据经过地区映射、争议隔离及等价聚合，相应署名与衍生许可继续适用。

Anycast 参考 [LACeS](https://github.com/ut-dacs/anycast-census)（许可见上游）及 [Cloudflare](https://www.cloudflare.com/ips/) / [Google Public DNS](https://developers.google.com/speed/public-dns/docs/isp) 官方范围。域名边界使用 [Mozilla PSL](https://publicsuffix.org/list/)（MPL-2.0），公网/地理地址边界参考 IANA [IPv4](https://www.iana.org/assignments/iana-ipv4-special-registry/) / [IPv6](https://www.iana.org/assignments/iana-ipv6-special-registry/) 特殊地址注册表。维护侧使用 [RIPE RIS](https://ris.ripe.net/docs/ris-whois/) 与 [geofeed-finder](https://github.com/massimocandela/geofeed-finder) 提示；地区映射参考 [UN M49](https://unstats.un.org/unsd/methodology/m49/overview/)。

人工复核端点参考 [Apple 推送](https://support.apple.com/en-us/101555)、[Microsoft 推送](https://learn.microsoft.com/en-us/windows/apps/develop/notifications/push-notifications/firewall-allowlist-config)、[Microsoft 365](https://learn.microsoft.com/en-us/microsoft-365/enterprise/urls-and-ip-address-ranges)、[Windows Update](https://learn.microsoft.com/en-us/troubleshoot/windows-client/installing-updates-features-roles/windows-update-issues-troubleshooting) 与 [Google 搜索域名调整](https://blog.google/products-and-platforms/products/search/country-code-top-level-domains/)。这些是复核过的端点事实子集，不是完整连通性允许列表。最终目录只含本 README 与规则文件，完整配方在源代码仓库。
