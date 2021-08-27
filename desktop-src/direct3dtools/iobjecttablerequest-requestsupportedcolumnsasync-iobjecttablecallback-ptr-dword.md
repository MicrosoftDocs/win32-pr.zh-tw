---
description: 要求取得此物件資料表要求類型所支援之資料行 (欄位) 的相關資訊。
MS-HAID: vspixengine.IObjectTableRequest\_RequestSupportedColumnsAsync\_IObjectTableCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IObjectTableRequest：： RequestSupportedColumnsAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0931C81A-65D5-493E-9F54-C7E98FA2FA6F
api_name:
- IObjectTableRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bfdf3b488296cf0092f59d4b944c39e00df45e31
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629581"
---
# <a name="span-idvspixengineiobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dwordspaniobjecttablerequestrequestsupportedcolumnsasync-method"></a><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>IObjectTableRequest：： RequestSupportedColumnsAsync 方法

要求取得此物件資料表要求類型所支援之資料行 (欄位) 的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT RequestSupportedColumnsAsync(
   IObjectTableCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a>參數

*requestCallback*   
用來通知主機結果的回呼位址。

*progressIntervalMsecs*   
未使用。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IObjectTableRequest**](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
