---
description: 回呼，會通知主機 assocaited 要求所傳回的泛型緩衝區資訊。
MS-HAID: vspixengine.IGenericBufferDataCallback\_ResultCallback\_DWORD\_BYTE\_arr\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IGenericBufferDataCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5627A93E-8BE8-4413-BFB4-724AF2DDFEB6
api_name:
- IGenericBufferDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0035b0546b863c87c54fbd09bbc62897ab581bfe
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622324"
---
# <a name="span-idvspixengineigenericbufferdatacallback_resultcallback_dword_byte_arr_bstrspanigenericbufferdatacallbackresultcallback-method"></a><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>IGenericBufferDataCallback：： ResultCallback 方法

回呼，會通知主機 assocaited 要求所傳回的泛型緩衝區資訊。

## <a name="syntax"></a>語法


```C++
HRESULT ResultCallback(
   DWORD   size,
   BYTE [] count0_buffer,
   BSTR    type
);
```

## <a name="parameters"></a>參數

*大小*   
緩衝區內容的大小（以位元組為單位）。

*count0 \_ 緩衝區*   
緩衝區內容。 在大部分的情況下，這是 XML 資料。

*類型*   
COM 字串，表示緩衝區中傳回的內容類型。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IGenericBufferDataCallback**](/windows/desktop/direct3dtools/igenericbufferdatacallback)

 

 
