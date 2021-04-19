---
title: HTML 字型回溯行為
description: HTML 字型回溯行為
ms.assetid: 5BDFBD58-0B34-4A58-BFAF-B8BB1DD569DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc7da95c46190fd348dda72edc8283ee6438b00
ms.sourcegitcommit: 80bac5863880f1bd4c1c3e06db27c5d8fb5232b4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "106969945"
---
# <a name="html-font-fallback-behavior"></a>HTML 字型回溯行為

## <a name="platform"></a>平台

用戶端-* * Windows 8。1  
**伺服器-** Windows Server 2012 R2  


## <a name="description"></a>Description

Microsoft 正在使用 HTML 更新 Windows Store 應用程式中數個語言的 UI 字型邏輯。 UI 字型現在會以每個語言為基礎來決定，而不是使用所有語言的單一字型。 例如，日文的 UI 字型現在會在使用 HTML 的應用程式中 Meiryo UI。

## <a name="manifestation"></a>表現

相依于舊字型的應用程式看起來可能不同;雖然您的應用程式外觀會因更多可讀取的字型而整體改善，但根據圖元內容大小的版面配置可能會有問題。 例如，某些內容行可能大於先前的內容，導致非預期的分行符號及/或調整大小的容器元素。 不過，實際上我們還沒注意到任何現有的應用程式有任何問題。

## <a name="solution"></a>解決方法

受影響的應用程式可透過 (CSS 指定指定字型來緩和這項行為，例如「font-family： Meiryo UI」 ) ，而不是依賴舊的預設字型。 下表提供每個腳本名稱的 UI 字型。



| 指令碼名稱        | UI 字型               |
|--------------------|-----------------------|
| 阿拉伯文             | Segoe UI              |
| 亞美尼亞文           | Segoe UI              |
| 孟加拉文            | Nirmala UI            |
| 符號           | Microsoft JhengHei UI |
| 盲文            | Segoe UI Symbol       |
| 布吉斯文           | Leelawadee UI         |
| 加拿大印第安方言 | Gadugi                |
| 卻洛奇文           | Gadugi                |
| 科普特文             | Segoe UI Symbol       |
| 簡 (簡)    | Microsoft YaHei UI    |
|  (傳統) 的漢字  | Microsoft JhengHei UI |
| 古斯拉夫文           | Segoe UI              |
| 梵文字母         | Nirmala UI            |
| 萊特            | Segoe UI Symbol       |
| 文           | Ebrima                |
| 喬治亞文           | Segoe UI              |
| 文         | Segoe UI Symbol       |
| 哥 特 式             | Segoe UI Symbol       |
| 希臘文              | Segoe UI              |
| 古吉拉特文           | Nirmala UI            |
| 古木基文           | Nirmala UI            |
| Hebrew             | Segoe UI              |
| 舊的斜體         | Segoe UI Symbol       |
| 爪哇文           | 爪哇文文字         |
| 日文           | Meiryo UI             |
| 坎那達文            | Mirmala UI            |
| 高棉文              | Leelawadee UI         |
| 韓文             | Malgun Gothic         |
| 寮文                | Leelawadee            |
| 拉丁文              | Segoe UI              |
| 馬來亞拉姆文          | Nirmala UI            |
| 蒙古文          | Mongolian Baiti       |
| 緬甸            | Myanmar Text          |
| 西非書面               | Ebrima                |
| 豎              | Segoe UI Symbol       |
| 桑塔爾文           | Nirmala UI            |
| 舊的土耳其文         | Segoe UI Symbol       |
| 歐利亞文              | Nirmala UI            |
| 文            | Ebrima                |
| 八位 pa           | Microsoft PhagsPa     |
| 符文              | Segoe UI Symbol       |
| Sora Sompeng       | Nirmala UI            |
| 僧伽羅文            | Nirmala UI            |
| 敘利亞文             | Estrangelo Edessa     |
| 泰 Le             | Microsoft Tai Le      |
| 新傣文        | Microsoft New Tai Lue |
| 坦米爾文              | Nirmala UI            |
| 泰盧固文             | Nirmala UI            |
| 納           | Ebrima                |
| 塔安那文             | MV Boli               |
| 泰文               | Leelawadee UI         |
| 西藏文            | Microsoft Himalaya    |
| 范文                | Ebrima                |
| 爨文                 | Microsoft Yi Baiti    |



 

 

 




