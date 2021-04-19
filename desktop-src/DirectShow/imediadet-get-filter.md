---
description: Get \_ 篩選方法會抓取媒體偵測器目前所使用的來源篩選指標。
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: 'IMediaDet：： get_Filter 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f80b5d5021ca7f04cd56dc319fb5416c3361108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984387"
---
# <a name="imediadetget_filter-method"></a>IMediaDet：： get \_ Filter 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `get_Filter` 媒體偵測器目前所使用的來源篩選指標。

## <a name="syntax"></a>語法


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppVal* \[退出，retval\]
</dt> <dd>

接收篩選的 **IUnknown** 介面指標。 如果沒有來源篩選正在使用中，此值會設為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

當此方法傳回時，如果 *\* ppVal* 不是 **Null**，則 **IUnknown** 介面具有未處理的參考計數。 使用完畢後，請釋放介面。

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

 

 




