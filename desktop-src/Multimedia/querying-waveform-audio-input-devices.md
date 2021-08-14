---
title: 查詢 Waveform-Audio 輸入裝置
description: 查詢 Waveform-Audio 輸入裝置
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- 波形音訊，查詢輸入裝置
- 波形-音訊介面，查詢輸入裝置
- 錄製波形音訊，查詢輸入裝置
- 查詢波形音訊輸入裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd22a2b65746202a831d475fcde38b31259619dbc645a5cbca3b91d03ff6e0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371920"
---
# <a name="querying-waveform-audio-input-devices"></a>查詢 Waveform-Audio 輸入裝置

錄製波形音訊之前，您應該呼叫 [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) 函式來判斷系統的波形音訊輸入功能。 此函式會以指定裝置功能的相關資訊填入 [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) 結構。 這項資訊包括製造商和產品識別碼、裝置的產品名稱，以及設備磁碟機的版本號碼。 此外， **WAVEINCAPS** 結構會提供裝置所支援之標準波形-音訊格式的相關資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錄製波形音訊](recording-waveform-audio.md)
</dt> </dl>

 

 