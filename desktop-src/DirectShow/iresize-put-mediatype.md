---
description: Put 媒體 \_ 型方法會在調整器篩選器上設定輸出媒體類型。
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: 'IResize：:p ut_MediaType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aedaced5033c229131f548e298217e3c77ff70c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978683"
---
# <a name="iresizeput_mediatype-method"></a>IResize：:p 的 ui \_ 媒體方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`put_MediaType`方法會在調整器篩選器上設定輸出媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pmt* \[在\]
</dt> <dd>

包含媒體類型的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

DES 會先呼叫這個方法，然後再連接篩選器的輸出圖釘。 使用媒體類型作為輸出釘選的媒體類型。 在 [**CTransformFilter：： GetMediaType**](ctransformfilter-getmediatype.md) 方法中傳回此媒體類型，並在 [**CTransformFilter：： CheckTransform**](ctransformfilter-checktransform.md) 方法中檢查 agsint 此類型。 在輸出連接之後，DES 永遠不會呼叫這個方法。

目前，DES 一律會將輸出媒體類型設定為 **VIDEOINFOHEADER** 格式區塊的未壓縮 RGB 格式， (格式類型等於 format \_ VideoInfo) 。 子類型可能是 MEDIASUBTYPE \_ ARGB32，表示具有 Alpha 色板的32位 RGB。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | DirectX 9.0 或更新版本<br/>                                                         |
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> <dt>

[**IResize 介面**](iresize.md)
</dt> </dl>

 

 




