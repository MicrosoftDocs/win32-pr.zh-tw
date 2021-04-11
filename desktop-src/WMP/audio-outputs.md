---
title: 音訊輸出
description: 音訊輸出
ms.assetid: 2bedf804-c9fd-4a44-9289-e36a50517b7f
keywords:
- Windows Media Player，音訊輸出
- Windows Media Player，預設 DirectSound 裝置
- Windows Media Player、eConsole
- Windows Media Player、eMultimedia
- Windows Media Player、eCommunications
- 音訊輸出
- 預設 DirectSound 裝置
- eConsole
- eMultimedia
- eCommunications
- Windows Media Player ActiveX 控制項、音訊輸出
- Windows Media Player ActiveX 控制項，預設 DirectSound 裝置
- Windows Media Player ActiveX 控制項，eConsole
- Windows Media Player ActiveX 控制項，eMultimedia
- Windows Media Player ActiveX 控制項，eCommunications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb5ebefb3b2bb72e8314c843ce0fe7632f09652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372047"
---
# <a name="audio-outputs"></a>音訊輸出

Windows XP 中的主控台可讓使用者將名稱預設 DirectSound 裝置指派給特定音訊輸出裝置。 在 Windows Vista 中，主控台可讓使用者將三個名稱 (eConsole、eMultimedia 和 eCommunications) 指派給音訊輸出裝置。 這些名稱都可以指派給不同的裝置，或多個名稱可以指派給相同的裝置。 下表顯示 Windows Media Player 和 Windows Media Player ActiveX 控制項如何選擇預設音訊輸出裝置。



|                                      | Windows XP                                                                                                                                                                                | Windows Vista                                                                                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Player                 | 根據預設，播放程式會使用指定為預設 DirectSound 裝置的音訊裝置。 播放程式會提供一個對話方塊，讓使用者將播放機切換到不同的音訊裝置。 | 根據預設，播放程式會使用指定為 eMultimedia 的音訊裝置。 播放程式會提供一個對話方塊，讓使用者將播放機切換到不同的音訊裝置。 |
| Windows Media Player ActiveX 控制項 | 根據預設，播放程式控制項會使用指定為預設 DirectSound 裝置的音訊裝置。 音訊輸出裝置無法以程式設計方式變更。                                | 根據預設，播放程式控制項會使用指定為 eMultimedia 的音訊裝置。 音訊輸出裝置無法以程式設計方式變更。                                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




