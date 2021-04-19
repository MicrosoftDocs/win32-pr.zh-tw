---
description: GetImageSize 方法會捕獲影片影像大小資訊。
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: 'CBaseControlVideo. GetImageSize 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed7795e3998bc101e907bce87c9981e86f51fcb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978526"
---
# <a name="cbasecontrolvideogetimagesize-method"></a>CBaseControlVideo. GetImageSize 方法

`GetImageSize`方法會捕獲影片影像大小資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetImageSize(
   VIDEOINFOHEADER *pVideoInfo,
   long            *pBufferSize,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

要填入之 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構的指標。

</dd> <dt>

*pBufferSize* 
</dt> <dd>

影片緩衝區大小的指標。

</dd> <dt>

*pSourceRect* 
</dt> <dd>

來源影片的矩形維度指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。



| 傳回碼                                                                                  | Description                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**E \_ 失敗**</dt> </dl>       | 失敗。<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 無效引數。 資料格式不相容。<br/>           |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl> | 發生未預期的錯誤。 一或多個引數為 **Null**。<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>       | 成功。<br/>                                                       |



 

## <a name="remarks"></a>備註

此成員函式是用來建立 DIB 映射之記憶體影像轉譯的 helper 函式。 當 **Null**_pVideoImage_ 參數傳遞至該成員函式時，它會從 [**CBaseControlVideo：： GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md)的基類實作為呼叫。 如此一來，這個成員函式會使用 *pBufferSize* 和 *pSourceRect* 中的資訊來建立並傳回 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




