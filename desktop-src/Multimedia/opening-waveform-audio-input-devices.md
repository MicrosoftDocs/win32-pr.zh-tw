---
title: 開啟 Waveform-Audio 輸入裝置
description: 開啟 Waveform-Audio 輸入裝置
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- 波形音訊，開啟輸入裝置
- 波形-音訊介面，開啟輸入裝置
- 錄製波形音訊，開啟輸入裝置
- 開啟波形-音訊輸入裝置
- waveInOpen 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92b7f49b9d170ceb8ebce287025ce0e0c1c5530
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969702"
---
# <a name="opening-waveform-audio-input-devices"></a>開啟 Waveform-Audio 輸入裝置

使用 [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) 函式來開啟波形音訊輸入裝置以進行錄製。 此函式會開啟與指定裝置識別碼相關聯的裝置，並藉由撰寫指定記憶體位置的控制碼，傳回開啟裝置的控制碼。

有些多媒體電腦有多個波形音訊輸入裝置。 除非您知道要在系統中開啟特定的波形音訊輸入裝置，否則 \_ 當您開啟裝置時，您應該使用 WAVE 對應程式常數作為裝置識別碼。 [**WaveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)函式會在系統中選擇最能以指定的資料格式記錄的裝置。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錄製波形音訊](recording-waveform-audio.md)
</dt> </dl>

 

 