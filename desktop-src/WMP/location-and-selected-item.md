---
title: 位置和選取的專案
description: 位置和選取的專案
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Windows Media Player 線上商店、位置
- 線上商店、位置
- 輸入1個線上商店、位置
- Windows Media Player 線上商店、程式庫位置
- 線上商店、程式庫位置
- 輸入1個線上商店、程式庫位置
- Windows Media Player 線上商店，選取的專案
- 線上商店、選取的專案
- 輸入1個線上商店、選取的專案
- Windows Media Player 程式庫，位置
- Windows Media Player 程式庫，選取的專案
- 程式庫，位置
- 程式庫，選取的專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d665b11e7509e369224d3e85db30dddb4a988a14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183418"
---
# <a name="location-and-selected-item"></a>位置和選取的專案

Windows Media Player 使用下列五個專案來描述其目前線上商店內容的觀點：

-   工作 (task)
-   程式庫位置類型
-   程式庫位置識別碼
-   選取的專案類型
-   選取的專案識別碼

一般來說，您可以將 Windows Media Player 中的 view 視為專案的容器。 容器具有類型，而專案具有類型。 容器中的所有專案都有相同的類型。 位置類型和專案類型都是由連結 [庫位置常數](library-location-constants.md)指定。 例如，如果目前的視圖顯示個別的專輯，則程式庫位置類型為 CPAlbumID，而且因為專輯包含曲目，所以選取的專案類型為 CPTrackID。

下表顯示數個容器的位置和專案類型。



| 容器的描述                              | 程式庫位置類型 | 選取的專案類型 |
|-------------------------------------------------------|-----------------------|--------------------|
| 作為追蹤容器的專輯                | CPAlbumID             | CPTrackID          |
| 作為追蹤容器的清單                  | CPListID              | CPTrackID          |
| 是專輯容器的清單                  | CPListID              | CPAlbumID          |
| 作為清單容器的電臺電臺          | CPRadioID             | CPListID           |
| 所有專輯的集合，也就是專輯的容器 | AllCPAlbumIDs         | CPAlbumID          |
| 所有內容的集合，也就是內容的容器 | AllCPGenreIDs         | CPGenreID          |



 

Windows Media Player 中的索引標籤代表不同的工作。 Player 會在三個不同的工作窗格中顯示線上商店內容： **媒體** 櫃、 **燒錄** 和 **同步**。[程式庫] 工作窗格也稱為 [ **流覽** 工作窗格]。 有時，工作窗格稱為 *功能*，因此您可能會在此檔中看到 [ *燒錄功能* 與 *同步* 處理] 等詞彙。

下列範例顯示 Windows Media Player 如何使用五項資訊， (工作、程式庫位置類型、程式庫位置識別碼、選取的專案類型、選取的專案識別碼) 來描述不同的視圖。

在 [ **燒錄** 工作] 窗格中，播放程式會將專輯顯示為曲目的容器。 專輯的識別碼為250。 在此視圖中，選取的專案是識別碼為800的軌跡。 請注意，800是線上商店目錄中的曲目識別碼，不是專輯的曲目編號。



| Item                  | 值     |
|-----------------------|-----------|
| 工作 (task)                  | 燒錄      |
| 程式庫位置類型 | CPAlbumID |
| 程式庫位置識別碼   | 250       |
| 選取的專案類型    | CPTrackID |
| 選取的專案識別碼      | 800       |



 

在 [ **同步** 處理工作] 窗格中，播放程式會顯示所有專輯的集合，也就是專輯的容器。 在此視圖中，選取的專案是識別碼為300的專輯。 請注意，程式庫位置識別碼不適用於此視圖。



| Item                  | 值         |
|-----------------------|---------------|
| 工作 (task)                  | 同步          |
| 程式庫位置類型 | AllCPAlbumIDs |
| 程式庫位置識別碼   | N/A           |
| 選取的專案類型    | CPAlbumID     |
| 選取的專案識別碼      | 300           |



 

在樹狀檢視控制項中，會選取線上商店的根節點。 在此情況下，沒有任何容器，因此沒有任何專案。 整個 [ **媒體** 櫃] 工作窗格都會顯示 [探索] 頁面。



| Item                  | 值           |
|-----------------------|-----------------|
| 工作 (task)                  | 瀏覽          |
| 程式庫位置類型 | RootLocation    |
| 程式庫位置識別碼   | N/A             |
| 選取的專案類型    | Unknownlocation.xsd |
| 選取的專案識別碼      | N/A             |



 

在 [ **同步** 處理工作] 窗格中，播放程式會將2002年份顯示為追蹤的容器。 在此視圖中，選取的專案是識別碼為450的軌跡。



| Item                  | 值           |
|-----------------------|-----------------|
| 工作 (task)                  | 同步            |
| 程式庫位置類型 | ReleaseDateYear |
| 程式庫位置識別碼   | 2002            |
| 選取的專案類型    | CPTrackID       |
| 選取的專案識別碼      | 450             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於類型1線上商店**](about-type-1-online-stores.md)
</dt> <dt>

[**探索頁面**](discovery-pages.md)
</dt> </dl>

 

 




