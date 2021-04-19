---
title: DownloadItem 物件
description: DownloadItem 物件
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Windows Media Player 線上商店，DownloadItem 物件
- 線上商店、DownloadItem 物件
- 類型2線上商店，DownloadItem 物件
- DownloadItem
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c367eee37f2f4d8329d71f3d42a3c78771a50a6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967225"
---
# <a name="downloaditem-object"></a>DownloadItem 物件

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**DownloadItem** 物件代表檔案下載要求。 它可供在完整模式中裝載的網頁使用 Windows Media Player 而且可以存取 **外部** 物件，例如 premium services。

**DownloadItem** 物件支援下列屬性。



| 屬性                                        | 描述                                      |
|-------------------------------------------------|--------------------------------------------------|
| [downloadState](downloaditem-downloadstate.md) | 捕獲下載的狀態。             |
| [進展](downloaditem-progress.md)           | 抓取下載的進度（以位元組為單位）。 |
| [size](downloaditem-size.md)                   | 抓取下載的大小。              |
| [sourceURL](downloaditem-sourceurl.md)         | 抓取下載的來源 URL。        |
| [type](downloaditem-type.md)                   | 抓取下載的類型。              |



 

**DownloadItem** 物件支援下列方法。



| 方法                                      | 描述                                                |
|---------------------------------------------|------------------------------------------------------------|
| [cancel](downloaditem-cancel.md)           | 取消下載。                                      |
| [getItemInfo](downloaditem-getiteminfo.md) | 抓取下載專案的屬性值。 |
| [pause](downloaditem-pause.md)             | 暫停下載。                                       |
| [恢復](downloaditem-resume.md)           | 繼續進行下載。                                      |



 

**DownloadItem** 物件是透過下列屬性來存取。



| Object                                              | 屬性                            |
|-----------------------------------------------------|-------------------------------------|
| [DownloadCollection](downloadcollection-object.md) | [item](downloadcollection-item.md) |



 

為了方便說明，請 **DownloadManager**。**getDownloadCollection** (*collectionId*) 。在參考語法區段中，會使用 (*itemId*) 的 **專案**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**類型 2 線上商店的參考**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




