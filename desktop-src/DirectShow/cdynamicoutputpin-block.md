---
description: Block 方法會封鎖或解除封鎖來自釘選的資料流程。 這個方法會實 IPinFlowControl：： Block 方法。
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: 'CDynamicOutputPin： Block 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Block
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6cc0a601ee1adbff9254baeff029c26d0cea359c7b2770b4d518bad916aca09f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074282"
---
# <a name="cdynamicoutputpinblock-method"></a>CDynamicOutputPin Block 方法

`Block`方法會封鎖或解除封鎖來自釘選的資料流程。 這個方法會實 [**IPinFlowControl：： Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Block(
   DWORD  dwBlockFlags,
   HANDLE hEvent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwBlockFlags* 
</dt> <dd>

指出是否要封鎖或解除封鎖 pin 的旗標。 必須為下列其中一個值：

零：解除封鎖來自 pin 的資料流程。

AM \_ 釘選 \_ 流程 \_ 控制 \_ 區塊：封鎖來自 PIN 的資料流程。

</dd> <dt>

*hEvent* 
</dt> <dd>

事件物件的控制碼，或 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                                                    | 描述                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                                        | Pin 已解除封鎖。<br/>                     |
| <dl> <dt>**S \_ 確定**</dt> </dl>                                           | 成功。<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                   | 無效引數。<br/>                             |
| <dl> <dt>**VFW \_ E \_ PIN \_ 已 \_ 封鎖**</dt> </dl>                   | Pin 已在另一個執行緒上遭到封鎖。<br/>     |
| <dl> <dt>**\_ \_ \_ \_ \_ \_ 此執行緒上已封鎖 \_ VFW E PIN**</dt> </dl> | 呼叫執行緒上已封鎖 Pin。<br/> |



 

## <a name="remarks"></a>備註

如需此方法的詳細資訊，請參閱 [**IPinFlowControl：： Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block)。 就內部而言，這個方法會呼叫下列其中一種受保護的方法：

-   區塊 (非同步) ： [ **CDynamicOutputPin：： AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)
-   封鎖 (同步) ： [ **CDynamicOutputPin：： SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)
-   解除封鎖： [ **CDynamicOutputPin：： UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)

解除封鎖一律會以同步方式執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




