---
description: 要求傳回泛型物件資料，此資料會針對指定的事件和指定的格式來描述 vsglog 檔中的物件。
MS-HAID: vspixengine.IGenericBufferDataRequest\_RequestAsync\_DumperType\_EventID\_DWORD\_IGenericBufferDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IGenericBufferDataRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 542E20F9-B91D-4A05-AEE8-9DD2E80B76DB
api_name:
- IGenericBufferDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1859c5527480f018223933603a2dedb0af54cfe009194a170d537f10e124d35a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117722065"
---
# <a name="span-idvspixengineigenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dwordspanigenericbufferdatarequestrequestasync-method"></a><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>IGenericBufferDataRequest：： RequestAsync 方法

要求傳回泛型物件資料，此資料會針對指定的事件和指定的格式來描述 vsglog 檔中的物件。

## <a name="syntax"></a>語法


```C++
HRESULT RequestAsync(
   DumperType                   dumperType,
   EventID                      eventID,
   DWORD                        RequestedDataUID,
   IGenericBufferDataCallback * requestCallback,
   DWORD                        requestCookie,
   DWORD                        progressIntervalMsecs
);
```

## <a name="parameters"></a>參數

*dumperType*   
物件的文字表示格式指定的格式 (HTML、XML 等等 ) 

*eventID*   
指定要比對緩衝區內容的事件 (例如，轉譯目標可能會隨著時間而變更) 。

*RequestedDataUID*   
指定之物件的位址。

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

[**IGenericBufferDataRequest**](/windows/desktop/direct3dtools/igenericbufferdatarequest)

 

 
