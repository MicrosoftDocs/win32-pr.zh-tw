---
title: DownloadManager 物件
description: DownloadManager 物件
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Windows Media Player 線上商店，DownloadManager 物件
- 線上商店、DownloadManager 物件
- 類型2線上商店，DownloadManager 物件
- DownloadManager
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3555ee7b99c97e85ce856766bd9f670aac4229b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840231"
---
# <a name="downloadmanager-object"></a>DownloadManager 物件

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**DownloadManager** 物件是 Windows Media Player 下載管理員的根物件。 它可供裝載于線上商店服務工作窗格的網頁使用。

**DownloadManager** 物件支援下列方法。



| 方法                                                                   | 描述                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [createDownloadCollection](downloadmanager-createdownloadcollection.md) | 建立空的下載集合。        |
| [getDownloadCollection](downloadmanager-getdownloadcollection.md)       | 抓取指定的下載集合。 |



 

**DownloadManager** 物件是使用 external 來存取的 **。DownloadManager**。 為了方便說明，我們假設這個值已指派給名為 "DownloadManager" 的變數，此變數將用來識別參考語法區段中的這個物件。

在 Windows Media Player 10 或更新版本中， **DownloadManager** 屬性和物件只能從 [線上商店服務] 工作窗格存取。 您無法使用 **外部** 物件可用之其他功能的 **DownloadManager** ，例如 HTMLView、資訊中心視圖和專輯資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**類型 2 線上商店的參考**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




