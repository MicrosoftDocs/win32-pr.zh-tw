---
description: SetStartStop 方法會設定物件的開始和停止時間，相對於物件的父系。
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: 'IAMTimelineObj：： SetStartStop 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e2806d926c9842f5900f46f923f4cbdf8caa47f112e1832077ab7d2b80a9341c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052448"
---
# <a name="iamtimelineobjsetstartstop-method"></a>IAMTimelineObj：： SetStartStop 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetStartStop`方法會設定物件的開始和停止時間，相對於物件的父系。

## <a name="syntax"></a>語法


```C++
HRESULT SetStartStop(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*開始* 
</dt> <dd>

新的開始時間（以 100-毫微秒單位），或-1 會保留現有的開始時間。

</dd> <dt>

*停止* 
</dt> <dd>

新的停止時間（100-毫微秒單位）或-1，以保留現有的停止時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值：



| 傳回碼                                                                                  | 描述                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 無效引數。<br/> |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>    | 未實作。<br/>  |



 

## <a name="remarks"></a>備註

追蹤、組合和群組都不會執行此方法。 針對這些物件，開始時間一律為零，而停止時間是其所包含物件的最大停止時間。

請勿在相同的播放軌內的來源物件上設定重迭的時間。這樣做可能會導致未定義的行為。

針對來源物件，開始和停止時間與媒體開始和媒體停止時間無關。 變更一對值並不會變更另一個值。 若要設定媒體的開始和停止時間，請呼叫 [**IAMTimelineSrc：： SetMediaTimes**](iamtimelinesrc-setmediatimes.md) 方法。 如需詳細資訊，請參閱[DirectShow 編輯服務中的時間](time-in-directshow-editing-services.md)。

若要取得幀精確的剪下和轉換，請將 *Start* 和 *Stop* 參數設定為框架界限。 您可以使用 [**IAMTimelineObj：： FixTimes**](iamtimelineobj-fixtimes.md) 方法，將時間值轉換為最接近的框架界限，或使用下列函式，從畫面格編號轉換為參考時間：


```C++
REFERENCE_TIME inline FrameNumToTime(LONGLONG frame, double fps)
{
    double dt = (frame * 10000000 / fps);
    if (frame >= 0) 
    {
        dt += 0.5;    }
    else
    {
        dt -= 0.5;
    }
    return (REFERENCE_TIME)dt;
}
```



> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimelineObj 介面**](iamtimelineobj.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




