---
title: 播放清單物件喜好設定的裝置擴充功能
description: 播放清單物件喜好設定的裝置擴充功能
ms.assetid: 33b3dd18-fda2-4bf9-a893-5d77cdde6b80
keywords:
- Windows Media Player、裝置擴充功能
- Windows Media Player、延伸模組
- Windows Media Player，播放清單物件喜好設定
- 裝置延伸模組，播放清單物件喜好設定
- 延伸模組，播放清單物件喜好設定
- 播放清單物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2acb01de41b753a85fee1c69e0bf015c687da04f50a10531ee5c67b0a13cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340917"
---
# <a name="device-extensions-for-playlist-object-preferences"></a>播放清單物件喜好設定的裝置擴充功能

在同步處理過程中，Windows Media Player 10 或更新版本會將播放清單物件複製到已啟用 MTP 的可攜式裝置。 Windows Media Player 11 引進了新功能，可讓可攜式裝置限制複製的播放清單物件類型。  (Windows Media Player 一律會將同步處理規則所指定的播放清單內容同步處理。 這項功能只會影響播放清單物件的同步處理。 ) Windows Media Player 會將三種類型的播放清單物件從電腦複製到裝置：

-   **一般播放清單。** 這些是在 Windows Media Player 的連結 **庫** 功能中可見的播放清單。 這些包括使用者建立的播放清單、線上商店新增至媒體櫃的播放清單，以及隨播放程式一起安裝的範例播放清單。 Windows Media Player 只會在使用者選取這些播放程式進行同步處理時，將這些播放清單複製到裝置。
-   **股票同步播放清單。** 這些是隨 Windows Media Player 安裝的特殊播放清單，只能用於同步處理。 這些播放清單只會顯示在 Windows Media Player 裝置設定向導中。
-   **隱含建立的播放清單。** 當使用者在列出要同步處理之專案的窗格上時，會建立這些播放清單，例如 **演出者** 或 **專輯** 等類別目錄資料夾。

名為 wmpdevices 的標頭檔會在此版本中更新，定義支援 Windows Media Player 的裝置延伸模組所需的結構和常數。

若要透過 Windows Media Player MTP 裝置延伸模組，將裝置辨識為支援播放清單物件喜好設定，它必須在 DeviceInfo 資料集中包含下列資訊。  (如需此資料集的詳細資訊，請參閱 MTP 規格的4.6.1 一節。 ) 



| 資料集欄位          | 欄位順序 | 資料類型  | 值                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                 |
| VendorExtensionDesc    | 4           | **String** | "microsoft.com/WMPPD： 11.0" |



 

下表提供有關播放清單物件喜好設定的 MTP 作業詳細資料。



| 項目                  | 描述                                                                                                                                                                                                                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 操作程式碼        | 0x9203                                                                                                                                                                                                                                                                                          |
| Operation 參數1 | 0                                                                                                                                                                                                                                                                                               |
| Operation 參數2 | 0                                                                                                                                                                                                                                                                                               |
| Operation 參數3 | 0                                                                                                                                                                                                                                                                                               |
| Operation 參數4 | 0                                                                                                                                                                                                                                                                                               |
| Operation 參數5 | 0                                                                                                                                                                                                                                                                                               |
| 資料                  | 裝置會傳迴響應參數1中的值，以指出播放清單物件同步處理喜好設定。                                                                                                                                                                                      |
| 資料方向        | R->I                                                                                                                                                                                                                                                                                         |
| 回應碼選項 | MTP \_ 回應 \_ 正常 (0x2001) 或有效的錯誤回應碼。                                                                                                                                                                                                                                        |
| 回應參數1  | 0 或 1。 0值表示 Windows Media Player 必須只同步處理一般播放清單物件。 值為1時，表示 Windows Media Player 必須同步處理一般播放清單物件、存貨和隱含建立的同步播放清單物件（這是預設行為）。 |
| 回應參數2  | 0                                                                                                                                                                                                                                                                                               |
| 回應參數3  | 0                                                                                                                                                                                                                                                                                               |
| 回應參數4  | 0                                                                                                                                                                                                                                                                                               |
| 回應參數5  | 0                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>備註

針對可攜式裝置，執行這項功能是選擇性的。 Windows Media Player 預設會同步處理一般播放清單物件、股票同步播放清單物件，以及隱含建立的播放清單物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




