---
title: IBasicDevice remove_ConnectionStatusChanged 方法
description: 取消註冊 ConnectionStatusChanged 事件的事件處理常式。 |IBasicDevice remove_ConnectionStatusChanged 方法
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- remove_ConnectionStatusChanged 方法媒體串流 API
- remove_ConnectionStatusChanged 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，remove_ConnectionStatusChanged 方法
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c2bfa2886774ad637e66385a057c9d4e21efe0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997349"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a>IBasicDevice：： remove \_ ConnectionStatusChanged 方法

取消註冊 [**ConnectionStatusChanged**](connectionstatuschanged.md) 事件的事件處理常式。

## <a name="syntax"></a>語法


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*token* \[在\]
</dt> <dd>

註冊事件處理常式時，從 [**add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) 方法取得的標記參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





