---
description: 在下列範例程式碼中，監視器會設定只指定 IP 和要求的通訊協定資料的捕獲篩選器。
ms.assetid: 0945bceb-b5fe-4f07-866b-4e0468227610
title: 處理框架資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a103dd2fea564eb6eb93ffcb32d5c21acbe991d515b7e75f287786dbce976c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995428"
---
# <a name="processing-frame-data"></a>處理框架資料

在下列範例程式碼中，監視器會設定 **只指定 IP** 和要求的通訊協定資料的捕獲篩選器。


```C++
STDMETHODIMP CTestMon::OnFrames(UPDATE_EVENT Event)
{
    DWORD i;
    LPFRAMETABLE lpFrameTable = Event.lpFrameTable;

    // The frame table can wrap the indexes.
    for (
      i = lpFrameTable->StartIndex; 
      i != lpFrameTable->EndIndex; 
     (i == lpFrameTable->FrameTableLength ) ? i=0: i ++ )
    {
        LPFRAME_DESCRIPTOR lpFrameDesc = &lpFrameTable->Frames[i];
        
        // Cast the frame data to an unaligned pointer to an IP  
        // structure. A try/catch block could be a workaround, but
        // if the capture filter is set correctly, this is the
        // verifiable IP.
        ULPIP ulpIP = (ULPIP)(&lpFrameDesc->FramePointer[lpFrameDesc->LowProtocolOffset]);
        // Now examine the IP frame.
    }
    return NOERROR;
}
```



 

 



