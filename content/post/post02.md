+++
title = "XNA"
description = "XNA, make game with c#"
date = "2006-07-09"
aliases = ["about-us","about-hugo","contact"]
author = "Parkpoom Maneeyod"
+++

Written in Go, Hugo is an open source static site generator available under the [Apache Licence 2.0.](https://github.com/gohugoio/hugo/blob/master/LICENSE) Hugo supports TOML, YAML and JSON data file types, Markdown and HTML content files and uses shortcodes to add rich content. Other notable features are taxonomies, multilingual mode, image processing, custom output formats, HTML/CSS/JS minification and support for Sass SCSS workflows.

Hugo makes use of a variety of open source projects including:

* https://github.com/yuin/goldmark
* https://github.com/alecthomas/chroma
* https://github.com/muesli/smartcrop
* https://github.com/spf13/cobra
* https://github.com/spf13/viper

Hugo is ideal for blogs, corporate websites, creative portfolios, online magazines, single page applications or even a website with thousands of pages.

Hugo is for people who want to hand code their own website without worrying about setting up complicated runtimes, dependencies and databases.

Websites built with Hugo are extremelly fast, secure and can be deployed anywhere including, AWS, GitHub Pages, Heroku, Netlify and any other hosting provider.

Learn more and contribute on [GitHub](https://github.com/gohugoio).





เมื่อวันที่ [30/สิงหา/2006] รอ download กันทั่วโลก สนุกดีครับ ตอนแรก link error ซัก 2-3 ชม.จึงสามารถ download ได้....


เท่าที่ลองใช้ดูแล้ว ค่อนข้างจะแตกต่างกับการเขียนโดยใช้ DirectX กับ VS ต่างๆน่ะครับเพราะมันเป็น XNA Framework แต่ถ้าอ่าน help ดูแล้วทำตามที่ล่ะ step ก็จะเข้าใจง่ายขึ้น โดยภาพรวมแล้ว XNA Game Studio Express (BETA) ถือว่าสอบผ่านเลยทีเดียวเชียว ผมค่อนข้างจะประทับใจน่ะ ถ้าเทียบกับสมัยที่ยังใช้ DirectX 5 กับ VC++ ทำความเข้าใจได้ไม่ยาก เพียงแต่ XNA นั้นต้องอาศัยพื้นฐานของ VC# , game logic, game programming ต่างๆ เข้าไปในเกมส์ และส่วนที่ผมประทับใจอีกอย่างก็คือ การติดต่อกับ hardware ทำได้ดีในระดับเยี่ยมเลย (ยังไม่ได้ลองเล่นกับ display card) เท่าที่ได้ลองทดสอบกับ joy stick XBOX 360 น่ะแต่ว่าต้องเสียเงินซื้อของ PC นี้สิ (ถ้าไม่ใช้ keyboard น่ะ) ผมพึ่งซื้อมาจากแถวๆ หลักสี่ 1,800 กว่าบาท ซึ่งตอบสนองได้ดีมากๆ เลยโดยเฉพาะการสั่งให้ motor หมุนเนี้ยสนุกมากเลย.


ส่วนการเขียนโปรแกรมเนี้ยก็รู้สึกว่าจับต้อง เห็นภาพได้มากกว่า DirectX น่ะ (จากประสบการณ์ส่วนตัวที่ผ่านมาของผมน่ะครับ) อาจจะเป็นเพราะว่า VC# ก็ได้เพราะงานที่ทำประจำนั้นผมก็ใช้ VC# .NET เป็นหลัก (ส่วน VC++ .NETจะได้ใช้ก็ต่อเมื่อต้องติดต่อกับ hardware เท่านั้นน่ะครับ) ก็เลยทำให้รู้(ไปเอง) ว่ามันเห็นภาพมากขึ้นกว่า Win32 API + DirectX ส่วนเรื่องความเร็วนั้นผมว่าก็จัดอยู่ใน rate ที่ค่อนข้างดีน่ะครับรึเป็นเพราะว่า application ยังตัวเล็กอยู่ (??)

จะไม่มีข้อเสียก็ไม่ได้ ถ้าคนที่ไม่ได้ติดตาม XNA Technology ก็จะงงเหมือนกันว่าอะไร เป็นอะไร มันไม่ได้เป็น drag & drop อย่างที่หลายคนใน XNA Forums เดาไว้ (ถ้าอยาก drag & drop คงต้องไปหา engine อื่นมาใช้ดูน่ะครับ) XNA ก็ยังคงใช้การเขียน code อยู่ แต่มีจุดเด่นตรงที่ Game Components นี้ล่ะที่เจ๋งมาก ลอง d/l ตาม link นี้ดูครับ

* http://xnateam.members.winisp.net/Videos/gamecomponentsdemo.wmv

ถ้าคนมีพื้นฐาน game programming ก็จะสามารถใช้งานได้ไม่ยาก ยังมี ERROR แปลกๆให้เห็นบ้าง, อ๋ออีกเรื่องนึงครับบาง displaycard ไม่สนับสนุน พวก programmable pipeline หรือ Shader Model 2.0 ก็จำเป็นต้อง เพิ่ม/แก้ตรง

...graphics.AllowMultiSampling = true; // เปลี่ยนเป็น false ซะน่ะครับ
ซึ่งถ้า display card ของใครเก่ามากๆ ก็จำเป็นต้องหาของใหม่แล้วล่ะครับ หรือไม่งั้นก็เพิ่ม code ที่ว่าลงไปด้วยล่ะครับ ใน XNA FORUMS โดนกันเยอะ เผอิญ display card ผมก็ไม่มีเหมือนกันก็เลยโดนด้วย แต่อ่านเจอ error code ตรงนี้แล้วถึงเข้าใจแต่ผมเห็นหลายๆคนใน XNA FORUMS บอกว่าเข้าขั้น run ได้อืดมากๆๆ แม้จะใส่ code ตรงนี้แล้วก็ตาม โดยเฉพาะตอน run โปรแกรม Spacewar Starter Kit ในส่วนนี้ Template (Spacewar Starter Kit) มันไม่น่า generate code ออกมาสักเท่าไหร่น่าจะเป็น option ให้ใส่น่ะ

สรุปโดยรวมแล้ว XNA เป็น Technology ที่สนุกมากเวลาเขียนและน่าสนใจตัวนึงเช่นกัน ไม่แน่ครับคนไทยทุนน้อยๆ อย่างเราอาจจะดังกับ XBOX 360 ก็ได้ครับ ไว้มีโอกาศยังไงจะลอง preview หรือไม่ก็ tutorial ให้ครับ แต่ยังไงซะผู้ที่เป็นมือใหม่ หัดเขียนโปรแกรมก็น่าจะหา C# Programming หรือไม่ก็พื้นฐานการเขียนโปรแกรมอ่านก่อนก็จะดีมากๆครับจ ะได้ไม่งงไปซะก่อน

ปล. แล้วอย่าลืมไป d/l Visual C# 2005 Express Edition ก่อนน่ะครับเพราะ XNA BETA ตัวนี้ support แค่ Epress Edition เท่านั้น และ ต่อไปก็ DirectX SDK ตัวล่าสุดน่ะครับ แล้วจึงค่อยลง XNA น่ะครับ

Visual C# Express 2005
Microsoft DirectX9 SDK (August version)
XNA Game Studio Express 

Happy Coding
cookievirus@hotmail.com