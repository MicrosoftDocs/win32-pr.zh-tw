---
description: SetDefaultDestinationPosition 方法會將轉譯器設定回使用預設的目的地位置， (通常是整個視窗工作區) 。
ms.assetid: 228259d7-2f1f-4528-8c8a-d20d7542523c
title: 'CBaseControlVideo. SetDefaultDestinationPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d984370150ff069b31c99abd61456037e36d01121d3abc0ed9464c9e1071d020
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158781"
---
# <a name="cbasecontrolvideosetdefaultdestinationposition-method"></a>CBaseControlVideo. SetDefaultDestinationPosition 方法

方法會將轉譯器 `SetDefaultDestinationPosition` 設定回使用預設的目的地位置， (通常是整個視窗工作區) 。

## <a name="syntax"></a>語法


```C++
HRESULT SetDefaultDestinationPosition();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。



| 傳回碼                                                                                           | 描述                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ 失敗**</dt> </dl>                | 失敗。<br/>                                                              |
| <dl> <dt>**NOERROR**</dt> </dl>                | 成功。<br/>                                                              |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | 無法執行作業，因為沒有連接的釘選。<br/> |



 

## <a name="remarks"></a>備註

應用程式可以透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面變更影片的來源和目的地矩形。 來源矩形會影響原生影片來源的哪個區段會顯示在顯示上;目的地矩形會影響播放影片時的顯示位置。 目的地矩形相對於現正播放之視窗的工作區。 視窗的左上角是座標 (0，0) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




