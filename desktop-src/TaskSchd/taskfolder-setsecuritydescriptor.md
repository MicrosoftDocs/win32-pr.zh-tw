---
title: TaskFolder. SetSecurityDescriptor 屬性
description: 針對腳本，設定資料夾的安全描述項。
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- SetSecurityDescriptor 屬性工作排程器
- SetSecurityDescriptor 屬性工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器、SetSecurityDescriptor 屬性
topic_type:
- apiref
api_name:
- TaskFolder.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0854ee6485007e1465dd0a264c908d67443f248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934143"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a>TaskFolder. SetSecurityDescriptor 屬性

針對腳本，設定資料夾的安全描述項。

## <a name="syntax"></a>Syntax


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

您可以在工作資料夾的安全描述項中指定存取控制清單 (ACL) ，以便允許或拒絕特定使用者和群組存取工作資料夾。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[**TaskFolder. GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





