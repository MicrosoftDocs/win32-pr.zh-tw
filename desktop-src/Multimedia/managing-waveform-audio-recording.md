---
title: 管理 Waveform-Audio 記錄
description: 管理 Waveform-Audio 記錄
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- 波形音訊，錄製
- 波形-音訊介面，錄製
- 錄製波形音訊，關於
- WAVEHDR 結構
- waveInAddBuffer 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539f722a705d489064d38eccdf6d89e80ccb1518
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314773"
---
# <a name="managing-waveform-audio-recording"></a>管理 Waveform-Audio 記錄

開啟波形音訊輸入裝置之後，您就可以開始錄製波形音訊資料。 波形-音訊資料會記錄到 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) 結構所指定的應用程式提供的緩衝區中。 這些資料區塊必須在使用之前先備妥;如需詳細資訊，請參閱 [音訊資料區塊](audio-data-blocks.md)。

Windows 提供下列功能來管理波形音訊錄製。



| 函式                                   | 描述                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | 將緩衝區傳送到設備磁碟機，讓它可以填滿錄製的波形音訊資料。 |
| [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | 停止波形-音訊錄製，並將所有暫止的緩衝區標示為已完成。                      |
| [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | 開始波形-音訊錄製。                                                           |
| [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | 停止波形-音訊錄製。                                                            |



 

使用 [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) 函式將緩衝區傳送到設備磁碟機。 當緩衝區填滿錄製的波形音訊資料時，會根據開啟裝置時所指定的旗標，以視窗訊息、回呼訊息、執行緒訊息或事件來通知應用程式。

使用 [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)開始錄製之前，您應該至少將一個緩衝區傳送至驅動程式，否則可能會遺失傳入的資料。

使用 [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)來關閉裝置之前，請先呼叫 [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) ，將任何擱置中的資料區塊標示為已完成。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錄製波形音訊](recording-waveform-audio.md)
</dt> </dl>

 

 