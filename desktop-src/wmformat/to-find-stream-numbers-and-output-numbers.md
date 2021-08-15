---
title: 尋找資料流程號碼和輸出編號
description: 尋找資料流程號碼和輸出編號
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- Advanced Systems Format (ASF) 、串流號碼
- ASF (Advanced Systems Format) ，建立數位
- Advanced Systems Format (ASF) ，尋找輸出數位
- ASF (Advanced Systems Format) ，尋找輸出數位
- 同步讀取器，資料流程編號
- 同步讀取器，尋找輸出數位
- 串流，尋找數位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4349bc98214d61a1529fe4a64dd142a9695d909f9e2a650162a8e4f8ac618177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699586"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a>尋找資料流程號碼和輸出編號

同步讀取器支援更簡化的資料流程和輸出數目切換，而不是非同步讀取器的播放。 因此，更重要的是，能夠找出哪些串流號碼等於哪些輸出數位，或相反的方式。

若要尋找對應于資料流程號碼的輸出編號，請呼叫 [**IWMSyncReader：： GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream)。

若要尋找對應到輸出編號的資料流程號碼，請呼叫 [ **IWMSyncReader：： GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMSyncReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**輸入、串流和輸出**](inputs-streams-and-outputs.md)
</dt> <dt>

[**使用同步讀取器讀取檔案**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




