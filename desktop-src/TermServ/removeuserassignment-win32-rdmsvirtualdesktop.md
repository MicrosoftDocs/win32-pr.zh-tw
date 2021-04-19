---
title: Win32_RDMSVirtualDesktop 類別的 RemoveUserAssignment 方法
description: 從虛擬桌面移除使用者指派。
ms.assetid: 7ebb34b4-94f6-4a00-87a9-44ad28d103cb
ms.tgt_platform: multiple
keywords:
- RemoveUserAssignment 方法遠端桌面服務
- RemoveUserAssignment 方法遠端桌面服務，Win32_RDMSVirtualDesktop 類別
- Win32_RDMSVirtualDesktop 類別遠端桌面服務，RemoveUserAssignment 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.RemoveUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01675c777603f0eab2d22c0136b1ef6cc3522b7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106984960"
---
# <a name="removeuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Win32 RDMSVirtualDesktop 類別的 RemoveUserAssignment 方法 \_

從虛擬桌面移除使用者指派。

## <a name="syntax"></a>語法


```mof
uint32 RemoveUserAssignment(
  [in] string VMName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VMName* \[在\]
</dt> <dd>

虛擬桌面的虛擬機器名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                              |
| 命名空間<br/>                | 根 \\ CIMv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





