---
title: 裝置 i/o 控制碼
description: 裝置 i/o 控制碼
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Windows Media Player、裝置 i/o 控制碼
- Windows Media Player，控制代碼
- Windows媒體裝置管理員
- 裝置 i/o 控制碼
- 控制代碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d610b396125cf190764b53106ca6535a214e2c8166f4e69de884c113fd77ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935847"
---
# <a name="device-io-control-codes"></a>裝置 i/o 控制碼

Windows Media Player 10 或更新版本會定義 Windows 媒體裝置管理員裝置 i/o 控制碼。 下表包含控制碼及其描述。



| I/o 控制項程式碼                      | 值      | 描述                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IOCTL \_ WMP \_ 中繼資料 \_ 來回 \_ 行程** | 0x31504d57 | 管理有關中繼資料值發生之變更的資訊傳輸。 請參閱 [用於加速中繼資料傳輸的裝置延伸](device-extensions-for-accelerated-metadata-transfer.md)模組。                                                                                                                                                                          |
| **IOCTL \_ WMP \_ 裝置 \_ 可 \_ 同步**     | 0x32504d57 | 指出可攜式裝置是否支援自動同步處理。 Windows Media Player 10 或更新版本不會提供任何輸入緩衝區。輸出緩衝區必須傳回 **DWORD** 值。 1值表示裝置支援同步處理。 值為0表示裝置不支援自動同步處理。<br/> 如需詳細資訊，請參閱「備註」。<br/> |



 

## <a name="remarks"></a>備註

這些控制項代碼定義于 wmpdevices 中。

如果裝置不支援 **\_ \_ \_ 可 \_ 同步的 IOCTL WMP 裝置**，Windows Media Player 10 或更新版本會假設裝置支援自動同步處理。 請注意，雖然這個值可能不允許自動同步處理，但是還有其他準則用來判斷裝置是否支援自動同步處理。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**加速中繼資料傳輸的裝置擴充功能**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 





