---
description: 本主題說明如何使用 MFPlay 在播放期間搜尋。
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: 如何在播放期間搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47e035ff8cc3764a9080698e8596660ce61907319bda70ac019b4cba1f8c27f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974417"
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

 

 



