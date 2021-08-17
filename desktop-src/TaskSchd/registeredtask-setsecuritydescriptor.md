---
title: RegisteredTask. SetSecurityDescriptor 方法
description: 針對腳本，設定用來作為已註冊工作認證的安全描述項。
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- SetSecurityDescriptor 方法工作排程器
- SetSecurityDescriptor 方法工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器，SetSecurityDescriptor 方法
topic_type:
- apiref
api_name:
- RegisteredTask.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ac6845624ab2032b9b90d742c1346081c3ba4719d0814cfd257d3787c2bf70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759589"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a>RegisteredTask. SetSecurityDescriptor 方法

針對腳本，設定用來作為已註冊工作認證的安全描述項。

## <a name="syntax"></a>語法


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*sddl* \[在\]
</dt> <dd>

用來作為已註冊工作之認證的安全描述項。

> [!Note]  
> 如果本機系統帳戶拒絕存取某項工作，工作排程器服務可能會產生非預期的結果。

 

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

指定如何設定安全描述項的旗標。 您 \_ \_ \_ \_ 可以指定工作 [**\_ 建立**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) 列舉 (0x10) 的工作不新增主體 ACE 旗標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

您可以在工作的安全描述項中指定 (ACL) 的存取控制清單，以允許或拒絕特定使用者和群組對工作的存取。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> <dt>

[**TaskFolder. GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





