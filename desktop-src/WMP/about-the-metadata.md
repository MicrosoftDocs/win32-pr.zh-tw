---
title: 關於中繼資料
description: 關於中繼資料
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Windows Media Player，中繼資料
- 中繼資料，關於
- 中繼資料，屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcccda2af46e60e4bb0733d17e35e1a50d1fe923e9775fa6b10d2c06e3a972a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865358"
---
# <a name="about-the-metadata"></a>關於中繼資料

Windows Media Player 10 或更新版本會嘗試同步處理下列中繼資料屬性。



| Player 屬性 | WMDM 全域常數  | 描述                                                                                                 | 所需的版本                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| AlbumArtist      | g \_ wszWMDMAlbumArtist | 以 Null 終止的 **字串** ，其中包含專輯之主要演出者的名稱。                         | Windows Media Player 11 或更新版本。 |
| 專輯            | g \_ wszWMDMAlbumTitle  | 以 Null 終止的 **字串** ，其中包含最初發行內容的專輯標題。  | Windows Media Player 11 或更新版本。 |
| 作者           | g \_ wszWMDMAuthor      | 以 Null 終止的 **字串** ，包含與內容相關聯之媒體演出者或動作專案的名稱。    | Windows Media Player 11 或更新版本。 |
| BuyNow           | g \_ wszWMDMBuyNow      | 指出使用者是否已選擇購買內容的 **布林值**。                                 | Windows Media Player 10 或更新版本。 |
| WM/內容類型         | g \_ wszWMDMGenre       | 以 Null 終止的 **字串** ，其中包含內容的內容類型。                                             | Windows Media Player 11 或更新版本。 |
| UserPlayCount    | g \_ wszWMDMPlayCount   | **DWORD** ，包含使用者播放數位媒體檔案的次數。                        | Windows Media Player 10 或更新版本。 |
| ReleaseDate      | g \_ wszWMDMYear        | 專案原始版本的日期。                                                               | Windows Media Player 11 或更新版本。 |
| 標題            | g \_ wszWMDMTitle       | 包含標題的以 Null 結尾的 **字串** 。                                                            | Windows Media Player 11 或更新版本。 |
| WM/TrackNumber   | g \_ wszWMDMTrack       | **DWORD** ，其中包含原始釋出的專輯上專案的曲目編號。         | Windows Media Player 11 或更新版本。 |
| UserRating       | g \_ wszWMDMUserRating  | **DWORD** 包含值，表示使用者為數字媒體檔案指定的星級評等。 | Windows Media Player 10 或更新版本。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**加速中繼資料傳輸的裝置擴充功能**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




