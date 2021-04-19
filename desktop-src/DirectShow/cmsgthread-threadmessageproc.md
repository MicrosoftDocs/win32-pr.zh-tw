---
description: 處理要求。 這是單純的虛擬成員函式。
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: 'CMsgThread. ThreadMessageProc 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ThreadMessageProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf47eb63a6f9d8fe4921985bb64567de6678b44c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990700"
---
# <a name="cmsgthreadthreadmessageproc-method"></a>CMsgThread. ThreadMessageProc 方法

處理要求。 這是單純的虛擬成員函式。

## <a name="syntax"></a>語法


```C++
virtual LRESULT ThreadMessageProc(
   UINT     uMsg,
   DWORD    dwFlags,
   LPVOID   lpParam,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*uMsg* 
</dt> <dd>

要求代碼。

</dd> <dt>

*dwFlags* 
</dt> <dd>

要要求的選擇性旗標參數。

</dd> <dt>

*lpParam* 
</dt> <dd>

額外資料或傳回資料區塊的選擇性指標。

</dd> <dt>

*pEvent* 
</dt> <dd>

事件物件的選擇性指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

任何非零傳回都會導致執行緒結束。 除非最近處理過結束要求，否則會傳回零。

## <a name="remarks"></a>備註

您必須在衍生類別中覆寫此純虛擬函式。 針對 [**CMsgThread：:P utthreadmsg**](cmsgthread-putthreadmsg.md) 成員函式的呼叫所排入佇列的每個要求，都會呼叫此函式一次。

成員函式會定義四個參數。 通常，使用 *uMsg* 參數來表示要求，而其他三個參數將會是選擇性的額外參數。 如果您的應用程式需要，呼叫應用程式可以在 *pEvent* 參數中提供 [**CAMEvent**](camevent.md)物件的指標。 您必須在處理事件之後設定這個事件，方法是使用如下的運算式：


```C++
pEvent->SetEvent
```



您必須在旁邊設定一個要求碼，告知工作者執行緒結束。 收到此要求時，從這個成員函式傳回1。 如果您不想讓背景工作執行緒結束，則傳回0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Msgthrd (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMsgThread 類別**](cmsgthread.md)
</dt> </dl>

 

 




