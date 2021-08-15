---
description: 從指定的事件取得網格資料的非同步要求。
MS-HAID: vspixengine.IPipeLineStagesRequest3\_RequestMeshAsync\_EventID\_BSTR\_IPipeLineStagesCallback3\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesRequest3：： RequestMeshAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CAA36C96-3622-4D26-AB26-AD7960700B2A
api_name:
- IPipeLineStagesRequest3.RequestMeshAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 39177109630feb09231616173cd8ccc498c9e7f54b99aff7d4ac6b75aa946123
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721630"
---
# <a name="span-idvspixengineipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dwordspanipipelinestagesrequest3requestmeshasync-method"></a><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>IPipeLineStagesRequest3：： RequestMeshAsync 方法

從指定的事件取得網格資料的非同步要求。

## <a name="syntax"></a>語法


```C++
HRESULT RequestMeshAsync(
   EventID                    eventID,
   BSTR                       meshFilename,
   IPipeLineStagesCallback3 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>參數

*eventID*   
指定的事件。

*meshFilename*   
COM 字串，其中包含用來寫入網格資料之檔案的路徑名稱。

*requestCallback*   
用來通知主機結果的回呼位址。

*requestCookie*   
可唯一識別要求的 cookie，而且可用來指示它被取消。

*progressIntervalMsecs*   
未使用。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IPipeLineStagesRequest3**](/windows/desktop/direct3dtools/ipipelinestagesrequest3)

 

 
