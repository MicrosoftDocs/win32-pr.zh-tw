---
title: IReferenceClock AdviseTime 方法
description: AdviseTime 方法會要求經過一段時間的非同步通知。
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- AdviseTime 方法 windows Media 格式
- AdviseTime 方法 windows Media Format，IReferenceClock 介面
- IReferenceClock 介面 windows Media Format，AdviseTime 方法
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fa91338b4bff8f925f00e7159a36089e0de0aa8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106968465"
---
# <a name="ireferenceclockadvisetime-method"></a>IReferenceClock：： AdviseTime 方法

**AdviseTime** 方法會要求經過一段時間的非同步通知。

## <a name="syntax"></a>語法


```C++
HRESULT AdviseTime(
  [in]  REFERENCE_TIME rtBaseTime,
  [in]  REFERENCE_TIME rtStreamTime,
  [in]  HEVENT         hEvent,
  [out] DWORD          *pdwAdviseCookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rtBaseTime* \[在\]
</dt> <dd>

基底參考時間，以 100-毫微秒單位表示。

</dd> <dt>

*rtStreamTime* \[在\]
</dt> <dd>

資料流程位移時間，以 100-毫微秒單位表示。

</dd> <dt>

*hEvent* \[在\]
</dt> <dd>

事件的控制碼，由呼叫端建立。 當指定的時間結束時，將會通知此事件。

</dd> <dt>

*pdwAdviseCookie* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收要求的識別碼。 這是用來識別未來對 **AdviseTime** 的呼叫，例如取消要求。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                               | Description                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 此方法已成功。<br/>                        |
| <dl> <dt>**E \_ 指標**</dt> </dl> | *PdwAdviseCookie* 參數為 **Null**。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>    | 未指定的失敗。<br/>                         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IReferenceClock 介面**](ireferenceclock.md)
</dt> </dl>

 

 





