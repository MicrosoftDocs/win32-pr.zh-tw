---
title: 'Windows Media 下載套件的運作方式 (已淘汰) '
description: 'Windows Media 下載套件的運作方式 (已淘汰) '
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Windows Media 中繼檔，Windows Media 下載套件
- Windows Media Player，Windows Media 下載套件
- 中繼檔，Windows Media 下載套件
- Windows Media、Windows Media 下載套件
- Windows Media 下載套件，關於
- Windows Media 下載套件，封裝的運作方式
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1db477791bb93cd599dcef38a90b230c6cd7ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092252"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a>Windows Media 下載套件的運作方式 (已淘汰) 

本頁記載了未來版本的 Windows Media Player 和 Windows Media Player SDK 可能無法使用的功能。

當使用者按一下網頁瀏覽器中的連結（例如 Microsoft Internet Explorer）時，就會從網站啟動 Windows Media 下載套件。 此動作會開啟 Windows Media Player 然後在使用者的硬碟上，下載並取消封裝 Windows Media 下載套件（預設資料夾）。

從 Windows Media 下載套件解壓縮檔案之後，Windows Media Player 會在封裝的檔案之間找到副檔名為 .asx 的 Windows Media 中繼檔播放清單。 如果找到一個，播放清單會根據內含的中繼檔建立播放清單。 接著會將包含多媒體內容的檔案新增至程式庫。

Windows Media Player 也會尋找中繼檔中的 **外觀** 元素。 如果面板 **元素包含** 副檔名為 wmz 的 border 檔案的參考，則播放機會將框線載入至 [ **現正播放** ] 窗格中。 然後，玩家會開始播放套件中提供的內容。

下圖顯示如何將內容封裝在 Windows Media 下載檔案中、張貼至網站、在用戶端電腦上使用 Windows Media Player 進行下載及播放。

![如何取得並播放 windows media 下載檔案。](images/wmd-image.png) Windows Media 下載

下表說明組成 Windows Media 下載套件的三個元素。



| Package 元素    | 函式                                                                                                                                                                                                                                        | 副檔名                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| 框線             | 由內容擁有者所建立的固定自訂使用者介面，可顯示、連結及播放 Windows Media 下載套件中封裝的所有媒體。 用來建立框線的技巧，類似于用來建立外觀的技巧。 | .wmz                                     |
| 中繼檔播放清單  | Windows Media 中繼檔，其中包含 **專案專案** 、播放清單資訊，以及內容檔案的 **外觀** 元素識別。                                                                                                             | .asx                                     |
| 多媒體內容 | 包含 Windows Media Player 所支援之任何音訊或影片格式的檔案。                                                                                                                                                          | .wma、.wmv、.asf、.wav、.avi、. mpg、mp3 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**(淘汰的 Windows Media 下載套件)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




