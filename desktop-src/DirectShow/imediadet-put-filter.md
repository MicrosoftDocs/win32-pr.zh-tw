---
description: Put \_ 篩選方法會指定要使用之媒體偵測器的來源篩選。
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: 'IMediaDet：:p ut_Filter 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd07ee3e2a18dcceae752e3923fd5fbdc88c0313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992171"
---
# <a name="imediadetput_filter-method"></a>IMediaDet：:p 的 ui \_ 篩選方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`put_Filter`方法會指定要使用之媒體偵測器的來源篩選。

> [!IMPORTANT]
> 請勿將來源篩選新增至您自己的篩選圖形，或使用已在篩選圖形中的篩選。 媒體偵測器物件會自動建立內部篩選圖形，並將篩選準則放在另一個圖表中，可能會導致非預期的結果。

 

## <a name="syntax"></a>語法


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*newVal* \[在\]
</dt> <dd>

來源篩選的 **IUnknown** 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下：



| 傳回碼                                                                                   | Description                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                             |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | *newVal* 不會指向篩選。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | **Null** 指標引數。<br/>           |



 

## <a name="remarks"></a>備註

對於大部分的應用程式而言，使用原始程式檔的名稱呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md) 的檔案名稱方法會比較簡單。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMediaDet 介面**](imediadet.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




