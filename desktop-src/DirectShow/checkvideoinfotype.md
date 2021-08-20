---
description: CheckVideoInfoType 函式會針對可能造成緩衝區溢位或整數溢位的某些常見錯誤，檢查包含 VIDEOINFOHEADER 格式結構的媒體類型。
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: 'CheckVideoInfoType 函式 (Checkbmi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfoType
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 4463a1edb2002f64e983a38eb4a0ace5b5289b4d47ac43c8ea27bf165138ff95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539538"
---
# <a name="checkvideoinfotype-function"></a>CheckVideoInfoType 函式

此函式會 `CheckVideoInfoType` 檢查包含可能造成緩衝區溢位或整數溢位之特定常見錯誤的 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 格式結構的媒體類型。

> [!Note]  
> 此函式不保證媒體類型有效，或使用結構的程式碼是安全的。

 

## <a name="syntax"></a>語法


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pmt* 
</dt> <dd>

要驗證的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構指標

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值。



| 傳回碼                                                                                                | 描述                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 成功。<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl>                  | **Null** 指標值。<br/> |
| <dl> <dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt> </dl> | 媒體類型無效。<br/>     |



 

## <a name="remarks"></a>備註

此函數會呼叫 [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) 來驗證媒體類型中的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構。 如果格式類型不是 VideoInfo 格式 \_ ，則函式會傳回 \_ 不接受的 VFW E \_ 類型 \_ \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Checkbmi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片和影像函式](video-and-image-functions.md)
</dt> </dl>

 

 




