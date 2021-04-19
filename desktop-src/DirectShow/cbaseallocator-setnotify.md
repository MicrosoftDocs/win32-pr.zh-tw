---
description: SetNotify 方法會設定或移除配置器上的回呼。 配置器會在呼叫配置器的 IMemAllocator：： ReleaseBuffer 方法時呼叫回呼方法。
ms.assetid: ef9a6c66-d392-4130-b4fc-9eb6aecb6cbf
title: 'CBaseAllocator. SetNotify 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8269112325d470cae59cff6e615f04fbdfab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978466"
---
# <a name="cbaseallocatorsetnotify-method"></a>CBaseAllocator. SetNotify 方法

\[[**SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) 可能會在後續版本中變更或無法使用。\]

方法會在配置器 `SetNotify` 上設定或移除回呼。 配置器會在呼叫配置器的 [**IMemAllocator：： ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) 方法時呼叫回呼方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetNotify(
   IMemAllocatorNotifyCallbackTemp *pNotify
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNotify* 
</dt> <dd>

將用於回呼的 [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) 介面指標。 呼叫端必須執行介面。 使用 **Null** 值以移除回呼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會實 [**IMemAllocatorCallbackTemp：： SetNotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) 方法。 配置器不會公開 [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp)介面，除非 [**CBaseAllocator**](cbaseallocator.md)函式中的 *FEnableReleaseCallback* 旗標設為 **TRUE** 。

這個方法會設定等於 *pNotify* 的 [**CBaseAllocator：： m \_ pNotify**](cbaseallocator-m-pnotify.md)成員變數，並遞增介面上的參考計數。 如果 *m \_ pNotify* 為非 **Null**，配置器的 **ReleaseBuffer** 方法會呼叫 [**IMemAllocatorNotifyCallbackTemp：： NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease)。 請參閱該方法中的「備註」一節，以取得執行回呼的相關資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 




