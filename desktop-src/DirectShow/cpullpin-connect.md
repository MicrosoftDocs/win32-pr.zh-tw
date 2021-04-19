---
description: Connect 方法會完成輸出釘選的連接。
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: 'CPullPin 連接方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97e3b0b676e02dee0e3ebd82de9def56edc2ea28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980151"
---
# <a name="cpullpinconnect-method"></a>CPullPin 方法

`Connect`方法會完成輸出釘選的連接。

## <a name="syntax"></a>語法


```C++
HRESULT Connect(
   IUnknown      *pUnk,
   IMemAllocator *pAlloc,
   BOOL          bSync
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*朋 克* 
</dt> <dd>

輸出釘選的 **IUnknown** 介面指標。

</dd> <dt>

*pAlloc* 
</dt> <dd>

輸入釘選配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的指標，或 **Null**。

</dd> <dt>

*bSync* 
</dt> <dd>

指定是否要使用同步讀取的布林值。 若 **為 TRUE**，則 pin 會在輸出釘選上執行同步讀取作業。 如果 **為 FALSE**，則表示 pin 會發出非同步讀取要求。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT**。 可能的值如下。



| 傳回碼                                                                                               | Description                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                      | 成功。<br/>                                                             |
| <dl> <dt>**VFW \_ E \_ 已 \_ 連線**</dt> </dl> | 輸入 pin 已連線。<br/>                                  |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>             | 輸出 pin 不會公開 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)。<br/> |



 

## <a name="remarks"></a>備註

在輸入 pin 的連接進程期間，呼叫這個方法。 如果方法失敗，則 pin 應會使連接失敗。

這個方法會查詢 **IAsyncReader** 介面的輸出圖釘。 如果成功，則會呼叫 [**CPullPin：:D ecideallocator**](cpullpin-decideallocator.md) 來協調連接的配置器。 如果您的輸入 pin 有慣用的配置器，請在 *pAlloc* 參數中指定它; **DecideAllocator** 方法會將這個指標傳遞給輸出釘選的 [**IAsyncReader：： RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) 方法。 否則，請將 *pAlloc* 設定為 **Null**。

如果 *bSync* 的值為 **TRUE**， **CPullPin** 物件會藉由呼叫輸出釘選的 [**IAsyncReader：： SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)，來建立同步讀取要求。 否則，它會呼叫 [**IAsyncReader：： Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) 方法來產生重迭的讀取要求。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin。h</dt> </dl>                                                                                                       |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPullPin 類別**](cpullpin.md)
</dt> </dl>

 

 




