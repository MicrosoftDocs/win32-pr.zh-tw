---
title: Win32_RDMSVirtualDesktop 類別的 GetUserAssignment 方法
description: 抓取指派給虛擬桌面使用者的使用者名稱和功能變數名稱。
ms.assetid: 1887c49d-85df-4fb4-9b40-42fb7763bf95
ms.tgt_platform: multiple
keywords:
- GetUserAssignment 方法遠端桌面服務
- GetUserAssignment 方法遠端桌面服務，Win32_RDMSVirtualDesktop 類別
- Win32_RDMSVirtualDesktop 類別遠端桌面服務，GetUserAssignment 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87293a471bb4f69b3f4c57de0f964fa0daa043cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384901"
---
# <a name="getuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Win32 RDMSVirtualDesktop 類別的 GetUserAssignment 方法 \_

抓取指派給虛擬桌面使用者的使用者名稱和功能變數名稱。

## <a name="syntax"></a>語法


```mof
uint32 GetUserAssignment(
  [out] string UserName,
  [out] string UserDomain
);
```



## <a name="parameters"></a>參數

<dl> <dt>

使用者 *名稱* \[擴展\]
</dt> <dd>

接收使用者名稱。

</dd> <dt>

*UserDomain* \[擴展\]
</dt> <dd>

接收功能變數名稱。

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

 

 





