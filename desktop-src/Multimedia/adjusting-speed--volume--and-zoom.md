---
title: 調整速度、音量和縮放比例
description: 調整速度、音量和縮放比例
ms.assetid: 16cfbf86-911e-4cf3-9640-69fffc09c1ed
keywords:
- MCIWndSetSpeed 宏
- MCIWndGetSpeed 宏
- MCIWndSetVolume 宏
- MCIWndGetVolume 宏
- MCIWndSetZoom 宏
- MCIWndGetZoom 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbed63549683a92d457b9b91ac967ff9098235bf8d9cbd60b1ea332624886d9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808568"
---
# <a name="adjusting-speed-volume-and-zoom"></a>調整速度、音量和縮放比例

[速度]、[音量] 和 [縮放] 宏可提供 [MCIWnd] 功能表上的 **View**、 **volume** 和 **speed** 命令功能。 本節所述的宏一般會搭配影片和其他裝置使用，這些裝置會在播放期間顯示影像。

某些裝置支援多種播放速度變更。 您可以使用 [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) 宏來設定這些裝置的播放速度。 此宏會將播放速度定義為1000。 較高的值表示速度更快。 較低的值表示速度較慢。

您可以使用 [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) 宏來取得目前的播放速度。 這個宏使用的值和範圍與 **MCIWndSetSpeed** 所使用的相同。

某些裝置支援磁片區變更。 您可以使用 [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) 宏來調整或設定磁片區。 此宏將一般磁片區層級定義為1000。 較高的值表示較大的磁片區。 較低的值表示更安靜的磁片區。

您可以使用 [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) 宏來取得目前的磁片區層級。 這個宏使用的數值和範圍與 **MCIWndSetVolume** 所使用的數值和範圍相同。

針對使用播放視窗的裝置，MCIWnd 支援可設定播放映射大小的縮放功能。 您可以使用 [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) 宏來設定播放映射大小。 宏會重新定義播放影像大小，同時維持影像的固定外觀比例。 縮放值會以原始影像大小的百分比來定義。 因此，100代表原始影像大小，50表示顯示的影像是其原始大小的一半，而200表示顯示的影像是其原始大小的兩倍。

您可以使用 [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) 宏來取得目前的縮放值。 這個宏使用的值和範圍與 **MCIWndSetZoom** 所使用的相同。

> [!Note]  
> 標準 MCI CD 音訊和波形音訊驅動程式不支援磁片區或速度變更。

 

 

 




