---
description: CheckVideoInfo2Type 函式會針對可能造成緩衝區溢位或整數溢位的某些常見錯誤，檢查包含 VIDEOINFOHEADER2 格式結構的媒體類型。
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: 'CheckVideoInfo2Type 函式 (Checkbmi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfo2Type
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 48d9deab4d87868cbc9e5418ccd6b7e2c7e9ecf93350ad70cb6c934d365e4655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074182"
---
# <a name="checkvideoinfo2type-function"></a>CheckVideoInfo2Type 函式

此函式會 `CheckVideoInfo2Type` 檢查包含可能造成緩衝區溢位或整數溢位之特定常見錯誤的 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式結構的媒體類型。

> [!Note]  
> 此函式不保證媒體類型有效，或使用結構的程式碼是安全的。

 

## <a name="syntax"></a>語法


```C++
HRESULT CheckVideoInfo2Type(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pmt* 
</dt> <dd>

要驗證的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值。



| 傳回碼                                                                                                | 描述                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | Success<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl>                  | **Null** 指標值<br/> |
| <dl> <dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt> </dl> | 不正確媒體類型<br/>     |



 

## <a name="remarks"></a>備註

此函數會呼叫 [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) 來驗證媒體類型中的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構。 如果格式類型不是 **\_ VideoInfo2 格式**，則函式會 **傳回 \_ \_ \_ 不 \_ 接受的 VFW E 類型**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Checkbmi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片和影像函式](video-and-image-functions.md)
</dt> </dl>

 

 




