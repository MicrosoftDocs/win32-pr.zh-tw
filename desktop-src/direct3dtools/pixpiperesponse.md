---
description: 用來將回應從捕捉引擎傳送至圖形診斷的列舉。
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixPipeResponse 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5BFEE25D-3E03-493E-AFEF-DD8C70C53FC5
api_name:
- PixPipeResponse
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ad00d7bada935dd27f711499e5975d31709b9940
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631686"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span id="vspixengine.pixpiperesponse"></span>PixPipeResponse 列舉

用來將回應從捕捉引擎傳送至圖形診斷的列舉。

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>常數

<span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**可用的新 \_ 資料 \_**  
指出新資料已寫入圖形記錄檔並可供讀取的回應。

<span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**實驗 \_ 資料**  
指出有關 capture 會話設定資訊的回應。

<span id="ERRORCODE"></span><span id="errorcode"></span>**錯誤碼**  
表示捕獲引擎發生錯誤的回應。

<span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**  
表示 capture 引擎已開始捕獲圖形資訊的回應。 這並不表示資料仍可供檢查。

<span id="PARTIAL_DATA"></span><span id="partial_data"></span>**部分 \_ 資料**  
指出部分資料已寫入圖形記錄檔的回應。

<span id="READY"></span><span id="ready"></span>**準備**  
表示 capture 引擎已準備好開始捕獲圖形資訊的回應。

<span id="DONE"></span><span id="done"></span>**做**  
內部

<span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**  
表示已啟動框架捕獲的回應。

<span id="STATUS"></span><span id="status"></span>**地位**  
指出所要捕捉之應用程式狀態資訊的回應;例如，以畫面播放速率表示。

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



