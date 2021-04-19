---
title: Win32_RDMSVirtualDesktop 類別的 SetUserAssignment 方法
description: 將虛擬桌面指派給使用者。
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- SetUserAssignment 方法遠端桌面服務
- SetUserAssignment 方法遠端桌面服務，Win32_RDMSVirtualDesktop 類別
- Win32_RDMSVirtualDesktop 類別遠端桌面服務，SetUserAssignment 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f02e1cc935e344edd6a9c52016052e082e08d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106972689"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Win32 RDMSVirtualDesktop 類別的 SetUserAssignment 方法 \_

將虛擬桌面指派給使用者。

## <a name="syntax"></a>語法


```mof
uint32 SetUserAssignment(
  [in] string UserName,
  [in] string UserDomain
);
```



## <a name="parameters"></a>參數

<dl> <dt>

使用者 *名稱* \[在\]
</dt> <dd>

使用者的使用者名稱。

</dd> <dt>

*UserDomain* \[在\]
</dt> <dd>

使用者的功能變數名稱。

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

 

 





