---
title: Win32_RDMSDesktopAssignment 類別的 AddDesktopAssignment 方法
description: 新增桌面指派。
ms.assetid: 3690f70e-d0c3-444a-a0b7-cec6994eb3b8
ms.tgt_platform: multiple
keywords:
- AddDesktopAssignment 方法遠端桌面服務
- AddDesktopAssignment 方法遠端桌面服務，Win32_RDMSDesktopAssignment 類別
- Win32_RDMSDesktopAssignment 類別遠端桌面服務，AddDesktopAssignment 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.AddDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0d8145318cfd749772d2dcf417b71c6a1862ee31ec363957554e06b3aa6257
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868218"
---
# <a name="adddesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Win32 RDMSDesktopAssignment 類別的 AddDesktopAssignment 方法 \_

新增桌面指派

## <a name="syntax"></a>語法


```mof
uint32 AddDesktopAssignment(
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

 

 





