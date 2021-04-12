---
title: Win32_RDMSVirtualDesktopCollection 類別的 GetPatchProperties 方法
description: 抓取虛擬桌面集合中虛擬機器的軟體更新布建作業屬性。
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- GetPatchProperties 方法遠端桌面服務
- GetPatchProperties 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，GetPatchProperties 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetPatchProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f0ca45c97512818aa5f8a9ea851d18fa5554c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508847"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Win32 RDMSVirtualDesktopCollection 類別的 GetPatchProperties 方法 \_

抓取虛擬桌面集合中虛擬機器的軟體更新布建作業屬性。

## <a name="syntax"></a>語法


```mof
uint32 GetPatchProperties(
  [out] DATETIME StartTime,
  [out] DATETIME ForceLogOffTime,
  [out] string   JobGuid,
  [out] uint32   State
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartTime* \[擴展\]
</dt> <dd>

安裝更新的日期和時間。

</dd> <dt>

*ForceLogOffTime* \[擴展\]
</dt> <dd>

系統將登出虛擬機器使用者的日期和時間。

</dd> <dt>

*JobGuid* \[擴展\]
</dt> <dd>

可唯一識別布建作業的 **GUID** 。

</dd> <dt>

*狀態* \[擴展\]
</dt> <dd>

布建作業的狀態。

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

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





