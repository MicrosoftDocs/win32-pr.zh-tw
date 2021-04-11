---
title: XAudio2 介面
description: 本節包含 Microsoft XAudio2 API 所提供介面的相關資訊。
ms.assetid: 96691e00-9ed0-b31c-fbe9-4daaba0daf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d9f2c777a7b98c5cbc78a130c0a1431be5971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195303"
---
# <a name="xaudio2-interfaces"></a>XAudio2 介面

本節包含 Microsoft XAudio2 API 所提供介面的相關資訊。

## <a name="in-this-section"></a>本節內容



| 主題                                                               | 描述                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)<br/>                             | IXAudio2 是 [XAudio2](xaudio2-apis-portal.md) 物件的介面，可管理所有音訊引擎狀態、音訊處理執行緒、聲音圖形等等。 <br/>                                                                                                                                                |
| [**IXAudio2Voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice)<br/>                   | [**IXAudio2Voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice) 代表從中衍生 [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)、 [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) 和 [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) 的基底介面。 以下列出的方法通用於所有語音子類別。<br/> |
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)<br/>       | 使用來源聲音將音訊資料提交至 XAudio2 處理管線。<br/>                                                                                                                                                                                                                                                   |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)<br/>       | Submix 語音主要用於效能改進和效果處理。 <br/>                                                                                                                                                                                                                                        |
| [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)<br/> | 用來代表音訊輸出裝置的主控聲音。<br/>                                                                                                                                                                                                                                                               |
| [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)<br/> | IXAudio2EngineCallback 介面包含在 [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) 引擎中發生特定事件時通知用戶端的方法。<br/>                                                                                                                                                                           |
| [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback)<br/>   | [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback)介面包含在特定 [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)中發生特定事件時通知用戶端的方法。 <br/>                                                                                                                       |
| [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)<br/>                                   | XAudio2 效果鏈中所使用之音訊處理物件的介面。<br/>                                                                                                                                                                                                                                        |
| [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)<br/>               | 選擇性的介面，可讓 XAPO 使用效果特定的參數。<br/>                                                                                                                                                                                                                                                  |
| [**IXAPOHrtfParameters**](/windows/win32/api/hrtfapoapi/nn-hrtfapoapi-ixapohrtfparameters)<br/>       | 介面，用來設定參數，以控制如何將前端相關的傳送函數 (HRTF) 套用至音效。<br/>                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計參考](programming-reference.md)
</dt> <dt>

[程式設計參考](./programming-reference.md)
</dt> </dl>

 

 
