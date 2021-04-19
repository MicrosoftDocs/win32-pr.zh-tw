---
title: 範例影片 DSP 外掛程式中的 DoProcessOutput
description: 範例影片 DSP 外掛程式中的 DoProcessOutput
ms.assetid: 67536e35-a049-49c8-bd89-fad1fab37e6c
keywords:
- Windows Media Player 外掛程式、影片 DSP
- 外掛程式、視頻 DSP
- 數位信號處理外掛程式，DoProcessOutput
- DSP 外掛程式，DoProcessOutput
- 影片 DSP 外掛程式，DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3bc844890930209a1c6007213d3c466f0cd15b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967812"
---
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a>範例影片 DSP 外掛程式中的 DoProcessOutput

由於影片 DSP 外掛程式通常支援數種影片格式，因此將處理常式程式碼分隔為每個格式的個別函式是很方便的。 這表示影片 DSP 外掛程式的 **DoProcessOutput** 執行相當簡單。

範例外掛程式中的實首會先測試使用者是否已啟用外掛程式。 如果已停用外掛程式，程式碼就會將輸入緩衝區中提供的資料複製到輸出緩衝區，而不會變更它，如下列程式碼所示：


```C++
// Test whether the plug-in has been disabled by the user.
if (!m_bEnabled)
{
    // Just copy the data without changing it. You should
    // also do any necessary format conversion here.
    memcpy(pbOutputData, pbInputData, m_dwBufferSize);
    *cbBytesProcessed = m_dwBufferSize;

    return S_OK;
}

```



如果已啟用外掛程式，則程式碼只會在輸入媒體類型的 **子** 類型成員上執行一系列檢查，以判斷目前的影片格式。 找到相符的程式碼時，程式碼就會呼叫適當的處理函式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行 Video DSP 外掛程式**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




