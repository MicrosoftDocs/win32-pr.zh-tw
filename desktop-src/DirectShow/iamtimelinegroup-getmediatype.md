---
description: GetMediaType 方法會抓取群組的未壓縮媒體類型。
ms.assetid: 129ed688-0f03-4ccb-b65f-d61f02cb94b2
title: 'IAMTimelineGroup：： GetMediaType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2122b5429ffa66d278ccfe59553ac85fb0dee562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983245"
---
# <a name="iamtimelinegroupgetmediatype-method"></a>IAMTimelineGroup：： GetMediaType 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `GetMediaType` 群組的未壓縮媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT GetMediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pmt* \[擴展\]
</dt> <dd>

以媒體類型填滿的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

呼叫端必須釋放傳回的媒體類型的格式區塊，指定于所傳回的 AM \_ 媒體類型結構的 pbFormat 成員中 \_ 。 您可以從基類庫使用 helper 函式 [**FreeMediaType**](freemediatype.md) 。

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

[**IAMTimelineGroup 介面**](iamtimelinegroup.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




