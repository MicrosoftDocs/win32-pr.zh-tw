---
title: Win32_RDMSDesktopAssignment 類別的 RemoveDesktopAssignment 方法
description: 移除桌面指派。
ms.assetid: e1a8cf03-1d21-4bf4-a868-3da4d5bbf43b
ms.tgt_platform: multiple
keywords:
- RemoveDesktopAssignment 方法遠端桌面服務
- RemoveDesktopAssignment 方法遠端桌面服務，Win32_RDMSDesktopAssignment 類別
- Win32_RDMSDesktopAssignment 類別遠端桌面服務，RemoveDesktopAssignment 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.RemoveDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6645a79efc970cf7c3288d0765e9aac8cac68a89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965118"
---
# <a name="removedesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Win32 RDMSDesktopAssignment 類別的 RemoveDesktopAssignment 方法 \_

移除桌面指派

## <a name="syntax"></a>語法


```mof
uint32 RemoveDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CollectionAlias* \[在\]
</dt> <dd>

集合別名。

</dd> <dt>

*DesktopName* \[在\]
</dt> <dd>

桌面的名稱。

</dd> <dt>

*UserDomain* \[在\]
</dt> <dd>

使用者帳戶功能變數名稱。

</dd> <dt>

使用者 *名稱* \[在\]
</dt> <dd>

使用者帳戶名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                              |
| 命名空間<br/>                | 根 \\ cimv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RDMSDesktopAssignment**](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





