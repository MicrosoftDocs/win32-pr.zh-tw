---
description: GetCurrentImage 方法會在轉譯器上抓取目前影像的複本。
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: 'CBaseControlVideo. GetCurrentImage 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetCurrentImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 782f540959b134f7ca00c2bc674a64ce60ccb4f6ddf166c79f2597e582ca9fc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087568"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a>CBaseControlVideo. GetCurrentImage 方法

方法會在轉譯器 `GetCurrentImage` 上抓取目前影像的複本。

## <a name="syntax"></a>語法


```C++
HRESULT GetCurrentImage(
   long *pBufferSize,
   long *pVideoImage
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pBufferSize* 
</dt> <dd>

輸出緩衝區大小的指標。

</dd> <dt>

*pVideoImage* 
</dt> <dd>

影像輸出緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。



| 傳回碼                                                                                        | 描述                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ 失敗**</dt> </dl>             | 失敗。<br/>                                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>       | 無效引數。<br/>                                                      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>      | 記憶體不足。 當 *pVideoInfo* 參數為 **Null** 時傳回。<br/>   |
| <dl> <dt>**NOERROR**</dt> </dl>             | 成功。<br/>                                                               |
| <dl> <dt>**VFW \_ E \_ 未 \_ 暫停**</dt> </dl> | 無法執行操作，因為篩選未暫停。<br/> |



 

## <a name="remarks"></a>備註

此成員函式會從範例抓取影像，並將它複製到輸出緩衝區。 複製到輸出緩衝區的影片區段會反映透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面設定的來源矩形。 它不會反映目的地矩形。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




