---
title: RegisteredTask. GetSecurityDescriptor 方法
description: 針對腳本，取得用來作為已註冊工作之認證的安全描述項。
ms.assetid: 9b5985c5-c01a-4104-940f-1e0e79f18bb7
keywords:
- GetSecurityDescriptor 方法工作排程器
- GetSecurityDescriptor 方法工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器，GetSecurityDescriptor 方法
topic_type:
- apiref
api_name:
- RegisteredTask.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c7c0e6125bc848b361e4cc2d4515c32d797c57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934836"
---
# <a name="registeredtaskgetsecuritydescriptor-method"></a>RegisteredTask. GetSecurityDescriptor 方法

針對腳本，取得用來作為已註冊工作之認證的安全描述項。

## <a name="syntax"></a>語法


```VB
sddl = .GetSecurityDescriptor( _
  ByVal securityInformation _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*securityInformation* 
</dt> <dd>

[**安全性 \_**](/windows/desktop/SecAuthZ/security-information)資訊的安全性資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

已註冊工作的安全描述項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
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

 

