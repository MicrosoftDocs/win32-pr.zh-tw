---
title: 音訊緩衝區
description: 音訊緩衝區
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7993e3dc89abda520c0f1c5bda90f3eb209aca31e36071a304af01fb420d821e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692098"
---
# <a name="audio-buffers"></a>音訊緩衝區

您可以用三種方式控制捕捉作業的音訊部分：

-   從捕捉作業中包含或排除音訊。
-   要求特定數目的音訊緩衝區。
-   要求音訊緩衝區是特定的大小。

您可以使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息 (] 或 [ [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) ，來取得音訊緩衝區的設定。 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **fCaptureAudio** 成員會指定是否要在捕捉作業中包含或排除音訊。 目前要求的音訊緩衝區數目會儲存在 **wNumAudioRequested** 成員中，而目前的音訊緩衝區大小會儲存在 **dwAudioBufferSize** 成員中。 您可以指定是否要包含音訊捕捉、透過更新這些成員來指定音訊緩衝區的大小和數目，並使用 [ [**WM \_ CAP \_ SET \_ SEQUENCE 設定 \_**](wm-cap-set-sequence-setup.md)訊息 (] 或 [ [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ] 宏) ，將更新的 **CAPTUREPARMS** 結構傳送至 [捕獲] 視窗。

根據預設，音訊會包含在捕獲操作中，並配置四個音訊緩衝區。 **FCaptureAudio** 的預設值為 **TRUE**。 預設的緩衝區大小 (**dwAudioBufferSize**) 的值可以包含0.5 秒的音訊資料或10k （以較大者為准）。

 

 




