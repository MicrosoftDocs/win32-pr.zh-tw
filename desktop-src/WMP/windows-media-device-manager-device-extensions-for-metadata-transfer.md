---
title: 適用于中繼資料傳輸的 Windows Media 裝置管理員裝置擴充功能
description: 適用于中繼資料傳輸的 Windows Media 裝置管理員裝置擴充功能
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Windows Media Player、裝置擴充功能
- Windows Media Player、延伸模組
- Windows Media Player，中繼資料
- Windows Media Player，加速中繼資料傳輸
- Windows Media Player，中繼資料加速傳送
- 中繼資料，裝置延伸模組
- 中繼資料，延伸模組
- 裝置延伸模組，中繼資料傳輸
- 延伸模組，中繼資料傳輸
- 加速中繼資料傳輸
- 中繼資料，加速傳送
- 裝置延伸模組，加速中繼資料傳輸
- 延伸模組，加速中繼資料傳輸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d85ff7026e3395338fdf048c54b8ff7401c9ee7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462305"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a>適用于中繼資料傳輸的 Windows Media 裝置管理員裝置擴充功能

若要啟用加速中繼資料傳送，不支援 MTP 的裝置製造商必須在原始程式碼中執行下列作業：

-   定義 **WMP \_ WMDM \_ 裝置 \_ 支援**。
-   包含 wmpdevices，它會安裝為 Windows Media Player SDK 的一部分。

Wmpdevices 會定義下列結構。



| 結構                                                                                 | Description                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [WMP \_ WMDM \_ 中繼資料 \_ 來回 \_ 行程 \_ PC2DEVICE](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | Windows Media Player 用來向不支援 MTP 的可攜式裝置要求加速元資料同步處理資訊的結構。 |
| [WMP \_ WMDM \_ 中繼資料 \_ 來回 \_ 行程 \_ DEVICE2PC](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | Windows Media Player 用來從不支援 MTP 的可攜式裝置接收加速元資料同步處理資訊的結構。 |



 

若要向裝置要求已變更中繼資料的資訊，Windows Media Player 10 或更新版本會呼叫 Windows Media 裝置管理員方法 **IWMDMDevice3：:D eviceiocontrol**。 進行此呼叫時，播放玩家會遵循特定的步驟，如下所示：

-   第一個參數 *dwIoControlCode* 包含常數 **IOCTL \_ WMP \_ 中繼資料 \_ 來回 \_ 行程**。 這個常數定義于 wmpdevices 中。
-   第二個參數 *lpInBuffer* 會指向 **WMP \_ WMDM \_ 中繼資料 \_ 來回 \_ 行程 \_ PC2DEVICE** 結構。
-   第三個參數 *nInBufferSize* 包含輸入緩衝區的大小。
-   第四個參數 *lpOutBuffer* 會指向 **WMP \_ WMDM \_ 中繼資料 \_ 來回 \_ 行程 \_ DEVICE2PC** 結構。 裝置必須在此結構中填入變更的相關資訊。
-   第五個參數 *pnOutBufferSize* 會接收輸出緩衝區的大小。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**加速中繼資料傳輸的裝置擴充功能**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




