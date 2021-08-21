---
title: BasicDevice.remove_ConnectionStatusChanged 方法
description: 取消註冊 ConnectionStatusChanged 事件的事件處理常式。 |BasicDevice.remove_ConnectionStatusChanged 方法
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- remove_ConnectionStatusChanged 方法媒體串流 API
- remove_ConnectionStatusChanged 方法媒體串流 API，BasicDevice 介面
- BasicDevice 介面媒體串流 API，remove_ConnectionStatusChanged 方法
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89057195c23aa917c7338a8abb740817bb6af7896261cf1d31bcb37d5d5d5ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972497"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a>BasicDevice。移除 \_ ConnectionStatusChanged 方法

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

註冊事件處理常式時，從 [**add \_ ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) 方法取得的標記參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

