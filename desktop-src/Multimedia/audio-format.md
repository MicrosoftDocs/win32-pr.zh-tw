---
title: 音訊格式
description: 音訊格式
ms.assetid: a65dbd3f-1539-4f02-8573-c527c4e3c58d
keywords:
- WM_CAP_GET_AUDIOFORMAT 訊息
- capGetAudioFormat 宏
- capGetAudioFormatSize 宏
- WM_CAP_SET_AUDIOFORMAT 訊息
- capSetAudioFormat 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5891e8c244487895c51d68dd92fc4935f8981a36cf67d81437ff45f58950527b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375697"
---
# <a name="audio-format"></a>音訊格式

您可以藉由將 [**WM \_ CAP \_ GET \_ AUDIOFORMAT**](wm-cap-get-audioformat.md) 訊息 (或 [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) 和 [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) 宏) 傳送至捕獲視窗，來取得音訊資料的目前捕捉格式或音訊格式結構的大小。 預設音訊捕捉格式為 mono、8位、11 kHz PCM (脈衝程式碼調製) 。 當您使用 WM CAP GET AUDIOFORMAT 來取出格式時 \_ \_ \_ ，請一律使用 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) 結構。

您可以藉由將 [**WM \_ CAP \_ set \_ AUDIOFORMAT**](wm-cap-set-audioformat.md) message (或 [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) 宏) 傳送至 capture 視窗，來設定音訊資料的捕捉格式。 設定音訊格式時，您可以根據指定的音訊格式，將指標傳遞至 [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat)、 **WAVEFORMATEX** 或 [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) 結構。

 

 