---
description: 本主題說明如何使用 MFPlay 在播放期間搜尋。
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: 如何在播放期間搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16d7ad964335db100c84f0a396b7f13de7a270d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993008"
---
# <a name="how-to-seek-during-playback"></a>如何在播放期間搜尋

\[MFPlay 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 \]

本主題說明如何使用 MFPlay 在播放期間搜尋。

**在播放期間搜尋**

1.  將 **PROPVARIANT** 初始化為以 100-毫微秒單位來保存搜尋時間，以 **大 \_ 整數** (**VT \_ I8**) 類型。
2.  呼叫 [**IMFPMediaPlayer：： SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition)。 指定第一個參數的 **MFP \_ positiontype] \_ 100ns** ，然後傳入第二個參數的 **PROPVARIANT** 。

## <a name="requirements"></a>規格需求

MFPlay 需要 Windows 7。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 MFPlay 進行音訊/影片播放](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



