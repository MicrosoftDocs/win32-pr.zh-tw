---
title: IRDVTaskPluginNotifySink DeleteSchedule 方法
description: 由工作代理程式呼叫以刪除已排程的工作。
ms.assetid: 67a9493e-367a-48c9-8f94-276d696406b7
ms.tgt_platform: multiple
keywords:
- DeleteSchedule 方法遠端桌面服務
- DeleteSchedule 方法遠端桌面服務，IRDVTaskPluginNotifySink 介面
- IRDVTaskPluginNotifySink 介面遠端桌面服務，DeleteSchedule 方法
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.DeleteSchedule
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5674b3624edc102be6943e63b72444ec68f403fa1066e90a410f028008894d29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129140"
---
# <a name="irdvtaskpluginnotifysinkdeleteschedule-method"></a>IRDVTaskPluginNotifySink：:D eleteSchedule 方法

由工作代理程式呼叫以刪除已排程的工作。

## <a name="syntax"></a>語法


```C++
HRESULT DeleteSchedule(
  [in] BSTR bstrIdentifier
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrIdentifier* \[在\]
</dt> <dd>

排程工作的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------|
| 最低支援的用戶端<br/> | Windows 7 Enterprise<br/>   |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





