---
title: IRDVTaskPlugin StartTask 方法
description: 呼叫以啟動虛擬機器上的更新工作。
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- StartTask 方法遠端桌面服務
- StartTask 方法遠端桌面服務，IRDVTaskPlugin 介面
- IRDVTaskPlugin 介面遠端桌面服務，StartTask 方法
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51c499549378700a90d8fc78d075bc07c1f874cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465781"
---
# <a name="irdvtaskpluginstarttask-method"></a>IRDVTaskPlugin：： StartTask 方法

呼叫以啟動虛擬機器上的更新工作。

## <a name="syntax"></a>語法


```C++
HRESULT StartTask(
  [in] BSTR            Label,
  [in] BSTR            Identifier,
  [in] SAFEARRAY(BYTE) *Context
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*標籤* \[在\]
</dt> <dd>

工作的標籤。 這是在 [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) 方法中傳遞給觸發程式代理程式的標籤。

</dd> <dt>

*識別碼* \[在\]
</dt> <dd>

工作的識別碼。 這是在 [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) 方法中傳遞給觸發程式代理程式的識別碼。

</dd> <dt>

*內容* \[在\]
</dt> <dd>

工作的選擇性資料。 這是在 [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) 方法中傳遞給觸發程式代理程式的資料。

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

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





