---
title: MCIERR 傳回值
description: MCIERR 傳回值
ms.assetid: 61f7b128-b4f7-4385-9daf-e2bc9fb36e24
keywords:
- Windows 多媒體、MCIERR 傳回值
- 多媒體、MCIERR 傳回值
- 多媒體參考，MCIERR 傳回值
- 多媒體的參考，MCIERR 傳回值
- MCIERR 傳回值，關於
- mciSendCommand 函式
- mciSendString 函式
- Windows 多媒體，錯誤
- 多媒體，錯誤
- 多媒體參考，錯誤
- 多媒體的參考，錯誤
- 媒體控制介面 (MCI) 、MCIERR 傳回值
- MCI (媒體控制介面) ，MCIERR 傳回值
- MCI 的參考，MCIERR 傳回值
- MCI 參考，MCIERR 傳回值
- 媒體控制介面 (MCI) ，錯誤
- MCI (媒體控制介面) ，錯誤
- MCI 的參考，錯誤
- MCI 參考，錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fc8426b264f68d7a6ab793e365d529774c931e72d89536b40b22592728a2ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783408"
---
# <a name="mcierr-return-values"></a>MCIERR 傳回值

如果成功， [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 和 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函數會傳回零;否則，它們會傳回 **DWORD** 值，其中包含低字組中的下列其中一個錯誤值。

-   [一般 MCI 錯誤](general-mci-errors.md)
-   [mciSendString 錯誤](mcisendstring-errors.md)
-   [數位影片錯誤](digital-video-errors.md)
-   [Sequencer 錯誤](sequencer-errors.md)
-   [波形-音訊錯誤](waveform-audio-errors.md)

您可以藉由將傳回值傳遞至 [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) 函式，來取得個別傳回值的描述。

 

 