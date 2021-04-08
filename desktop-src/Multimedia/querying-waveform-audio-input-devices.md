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
ms.openlocfilehash: 91b915b3f39ad417a3d92396d887e5fb66092119
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933177"
---
# <a name="querying-waveform-audio-input-devices"></a>查詢 Waveform-Audio 輸入裝置

錄製波形音訊之前，您應該呼叫 [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) 函式來判斷系統的波形音訊輸入功能。 此函式會以指定裝置功能的相關資訊填入 [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) 結構。 這項資訊包括製造商和產品識別碼、裝置的產品名稱，以及設備磁碟機的版本號碼。 此外， **WAVEINCAPS** 結構會提供裝置所支援之標準波形-音訊格式的相關資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錄製波形音訊](recording-waveform-audio.md)
</dt> </dl>

 

 