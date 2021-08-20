---
title: 裝置的自訂映射支援
description: 裝置的自訂映射支援
ms.assetid: 0ccc327c-e953-4348-9802-705331b574ac
keywords:
- Windows Media Player，適用于裝置的自訂映射支援
- Windows Media Player，適用于裝置的映射支援
- 裝置自訂映射支援
- 裝置的自訂映射支援
- 裝置的映射支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2105693f207d2c7f91a9e93b1570a9bd13aac317cfa74d0d8d5674a199a5e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117936279"
---
# <a name="custom-image-support-for-devices"></a>裝置的自訂映射支援

> [!Note]  
> 本節說明使用 Windows XP 作業系統時可用 Windows Media Player 10 的功能。 它可能在後續版本中無法使用。

 

裝置製造商可以提供兩個特殊的影像檔案，以自訂裝置在 Windows Media Player 10 使用者介面中的呈現方式。 這兩個檔案是：

-   DevIcon. fil。 代表裝置硬體的 Windows 圖示格式檔案。 此影像會顯示在 Windows Media Player 10 的任何位置，圖示會用來代表裝置，例如 **同步** 處理功能中的裝置清單。
-   DevLogo. fil。 PNG 格式檔案，代表裝置製造商的公司標誌。 此影像會顯示在使用 Windows Media Player 10 位公司商標的位置，例如 [**裝置設定**] 對話方塊。

## <a name="general-guidelines-for-images"></a>影像的一般方針

下列指導方針一般適用于自訂映射支援：

-   此功能是選擇性的。 未提供映射的裝置將會以預設影像表示。
-   只有已啟用 MTP 的裝置才支援這項功能。
-   若要防止變更檔案，建議將影像檔儲存在固件或受保護的儲存媒體中，而不是使用使用者建立的檔案。
-   這些檔案不應該傳回給 Windows 媒體裝置管理員用戶端列舉裝置的根儲存體。 此外，刪除、移動或重新命名檔案都應該會失敗。
-   如果裝置提供一個以上的儲存媒體，則裝置應該會傳回影像檔案，以回應來自任何媒體的檔案開啟要求。 每個儲存媒體可能會傳回不同的裝置圖示。
-   針對 Windows 媒體裝置管理員啟用1.2 的用戶端，這些映射會優先于 Windows 設定機制（例如裝置節點屬性）所提供的圖示屬性。
-   映射不得包含任何需要當地語系化的資訊。
-   針對多函式裝置，只有 Windows XP 的音樂播放功能會使用這些映射。

## <a name="creating-the-device-icon-image"></a>建立裝置圖示影像

裝置圖示影像檔 DevIcon （fil）必須包含 Windows 圖示格式的檔案。 [Win32 中](/previous-versions/ms997538(v=msdn.10))的 MSDN 文章圖示說明如何建立這類檔案。 [建立 Windows xp 圖示](/previous-versions/ms997636(v=msdn.10))的 MSDN 文章提供 Windows xp 圖示的樣式指導方針。 裝置圖示影像檔藉由提供四種不同的大小，每個都有三個不同的色彩深度，以將12個影像併入單一檔案中。

請務必特別注意下列指導方針：

-   建議的大小 (以圖元為單位) 為16x16、32x32、48x48 和256x256。
-   建議的色彩深度為24位、8位 Alpha 色板、具有1位透明度的8位，以及具有1位透明度的4位。
-   使用先前所述 MSDN 文章中所述的透視圖角度和投影建議。

一旦您建立了圖示檔，只要將它重新命名為 DevIcon. fil。

## <a name="creating-the-corporate-logo-image"></a>建立公司標誌影像

公司標誌影像檔（DevLogo. fil）必須包含 PNG 格式的檔案。 建立映射時，請使用下列指導方針：

-   影像的大小上限為150x32 圖元。
-   影像應該支援 Alpha 混色，以啟用 Windows Media Player 10 使用者介面和標誌之間的平滑轉換。

一旦您建立了公司標誌檔案，只要將它重新命名為 DevLogo. fil。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 