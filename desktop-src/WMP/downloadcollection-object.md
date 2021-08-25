---
title: DownloadCollection 物件
description: DownloadCollection 物件
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Windows Media Player 線上商店，DownloadCollection 物件
- 線上商店、DownloadCollection 物件
- 類型2線上商店，DownloadCollection 物件
- DownloadCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565ddce120d71ab9825c424fefb6f0e3ace9a6ac349e87e044e9c74e6da28789
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902018"
---
# <a name="downloadcollection-object"></a>DownloadCollection 物件

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**DownloadCollection** 物件包含用來處理下載專案集合的屬性和方法。 它可供在完整模式中裝載的網頁使用 Windows Media Player 而且可以存取 **外部** 物件，例如線上存放區。

**DownloadCollection** 物件支援下列屬性。



| 屬性                              | 描述                                  |
|---------------------------------------|----------------------------------------------|
| [計數](downloadcollection-count.md) | 抓取暫止的下載數目。   |
| [id](downloadcollection-id.md)       | 抓取下載集合的識別碼。 |



 

**DownloadCollection** 物件支援下列方法。



| 方法                                                | 描述                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [清除](downloadcollection-clear.md)                 | 從下載集合中移除所有專案。 |
| [item](downloadcollection-item.md)                   | 抓取暫止的下載物件。          |
| [removeItem](downloadcollection-removeitem.md)       | 從集合中移除下載專案。    |
| [startDownload](downloadcollection-startdownload.md) | 將下載排在佇列中。                            |



 

**DownloadCollection** 物件是透過下列方法來存取。



| Object                                        | 方法                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [DownloadManager](downloadmanager-object.md) | [createDownloadCollection](downloadmanager-createdownloadcollection.md) |
| [DownloadManager](downloadmanager-object.md) | [getDownloadCollection](downloadmanager-getdownloadcollection.md)       |



 

為了方便說明，請 **DownloadManager**。參考語法區段中使用了 **getDownloadCollection** (*collectionId*) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**類型 2 線上商店的參考**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




