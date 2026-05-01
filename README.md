# WCMC Lab Homepage

This repository hosts the official homepage of the **WCMC Wireless Communication and Intelligent Computing Laboratory** at **Central South University**.

本仓库用于维护 **中南大学 WCMC 无线通信与智能计算实验室** 官方主页。

Website: <https://csu-wcmc.github.io/LabHomePage/>

## Lab Information

**English name:** WCMC Wireless Communication and Intelligent Computing Laboratory  
**Chinese name:** WCMC 无线通信与智能计算实验室  
**Institution:** School of Electronic Information, Central South University  
**PI:** Prof. Xiaoheng Deng  
**PI email:** <dxh@csu.edu.cn>

WCMC Lab focuses on next-generation wireless communication, intelligent computing, and networked intelligent systems. Current research directions include wireless networks, edge computing, Internet of Things, intelligent vehicular networks, big data, software-defined networking, distributed systems, online social networks, AI-enabled networking, and related applications in intelligent transportation and cyber-physical systems.

WCMC 无线通信与智能计算实验室隶属于中南大学电子信息学院，由邓晓衡教授负责。实验室面向新一代无线通信、智能计算与网络化智能系统开展研究，主要方向包括无线网络、边缘计算、物联网、智能车联网、大数据、软件定义网络、分布式系统、在线社会网络、人工智能赋能网络，以及其在智能交通和信息物理系统中的应用。

## Main Faculty

The People page currently includes the following faculty members:

- Prof. Xiaoheng Deng
- Prof. Jinsong Gui
- Prof. Huamei Qi
- Prof. Hairong Lin
- Prof. Xuechen Chen
- Prof. Tao Ouyang
- Prof. Jingjing Luo
- Prof. Zhenxiao Zhang
- Prof. Shuo Li

人员页面当前包括以下教师：邓晓衡、桂劲松、戚华梅、林海蓉、陈雪晨、欧阳涛、罗静静、张振霄、李朔。

## Site Content

The site is a bilingual academic lab homepage based on Jekyll. English and Chinese pages are separated by `lang` metadata and shared `ref` identifiers.

主要栏目：

- `Home` / `首页`
- `PEOPLE` / `人员`
- `PUBLICATIONS` / `论文`
- `RESEARCH` / `研究`
- `GALLERY` / `相册`
- `NEWS` / `新闻`
- `POSITIONS` / `招生招聘`

Important directories:

- `_pages/`: top-level English and Chinese pages
- `_news/`: news items
- `_posts/`: blog posts
- `_projects/`: research/project entries
- `_layouts/` and `_includes/`: shared page templates
- `_sass/`: site styles
- `assets/img/`: images, icons, and faculty photos

## Development Workflow

Use the project Docker environment for validation before pushing changes.

```bash
# Build and validate the Jekyll site in Docker
docker compose run --rm jekyll bundle exec jekyll build
```

For Markdown, Liquid, SCSS, and related formatting checks, use Prettier:

```bash
npx prettier README.md _pages _includes _sass --check
```

If formatting is required:

```bash
npx prettier README.md _pages _includes _sass --write
```

Recommended update workflow:

1. Edit content locally.
2. Run Prettier checks or formatting.
3. Run the Docker Jekyll build.
4. Commit and push to GitHub.
5. Confirm GitHub Pages deployment succeeds.

## Deployment

The site is configured for GitHub Pages:

- `url`: `https://csu-wcmc.github.io`
- `baseurl`: `/LabHomePage`
- Repository: <https://github.com/CSU-WCMC/LabHomePage>

After pushing to `main`, GitHub Actions builds and deploys the site to GitHub Pages.

## Template Attribution

This website is customized from the **al-folio** academic Jekyll theme.

Original template:

- Repository: <https://github.com/alshedivat/al-folio>
- Demo: <https://alshedivat.github.io/al-folio/>
- Documentation: <https://github.com/alshedivat/al-folio/blob/main/README.md>

Please cite the original project when reusing this repository or derivative templates:

```bibtex
@software{al_folio,
  title = {al-folio: A beautiful, simple, clean, and responsive Jekyll theme for academics},
  author = {Al-Shedivat, Maruan and contributors},
  url = {https://github.com/alshedivat/al-folio},
  license = {MIT},
}
```

## License

This repository includes customized content for WCMC Lab and template code derived from al-folio. The upstream al-folio theme is released under the MIT License. See `LICENSE` and the upstream repository for details.

Unless otherwise stated, lab-specific text, images, faculty information, and research content are maintained by WCMC Lab.
