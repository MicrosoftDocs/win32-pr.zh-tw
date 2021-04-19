---
title: IBasicDevice add_ConnectionStatusChanged 方法
description: 註冊 ConnectionStatusChanged 事件的事件處理常式。 |IBasicDevice add_ConnectionStatusChanged 方法
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- add_ConnectionStatusChanged 方法媒體串流 API
- add_ConnectionStatusChanged 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，add_ConnectionStatusChanged 方法
topic_type:
- apiref
api_name:
- IBasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0028e6f3dad1670974178b0f07a59f74dffdc06f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992687"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a>IBasicDevice：： add \_ ConnectionStatusChanged 方法

註冊 [**ConnectionStatusChanged**](connectionstatuschanged.md) 事件的事件處理常式。

## <a name="syntax"></a>語法


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*處理常式* \[在\]
</dt> <dd>

[**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))事件處理常式函數。

</dd> <dt>

*token* \[退出，retval\]
</dt> <dd>

可以用來取消註冊事件處理常式之權杖的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

若要取消註冊這個方法所註冊的事件處理常式，請將 *權杖* 值傳遞給 [**remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) 方法。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

