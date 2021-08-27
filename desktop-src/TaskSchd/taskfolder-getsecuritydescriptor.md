---
title: TaskFolder. GetSecurityDescriptor 屬性
description: 針對腳本，取得資料夾的安全描述項。
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- GetSecurityDescriptor 屬性工作排程器
- GetSecurityDescriptor 屬性工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器、GetSecurityDescriptor 屬性
topic_type:
- apiref
api_name:
- TaskFolder.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851565299b7e6d1c29e2e53d87fb27aa30297921cc194f3cce753fc8d22a6bc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080318"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a>TaskFolder. GetSecurityDescriptor 屬性

針對腳本，取得資料夾的安全描述項。

## <a name="syntax"></a>Syntax


```VB
TaskFolder.GetSecurityDescriptor( _
  ByVal securityInformation, _
  ByRef pSddl _
)
```



## <a name="property-value"></a>屬性值

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TaskFolder.SetSecurityDescriptor**](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





