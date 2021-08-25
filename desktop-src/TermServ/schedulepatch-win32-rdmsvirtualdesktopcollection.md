---
title: Win32_RDMSVirtualDesktopCollection 類別的 SchedulePatch 方法
description: 排程軟體更新布建作業，此作業會在虛擬桌面集合中的虛擬機器上安裝軟體更新。
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- SchedulePatch 方法遠端桌面服務
- SchedulePatch 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，SchedulePatch 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SchedulePatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb29eb42f0f1d13ff1bf234c6fb41b8f414317a4b723af9a6d215cf25fa2ec95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865508"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Win32 RDMSVirtualDesktopCollection 類別的 SchedulePatch 方法 \_

排程軟體更新布建作業，此作業會在虛擬桌面集合中的虛擬機器上安裝軟體更新。

## <a name="syntax"></a>語法


```mof
uint32 SchedulePatch(
  [in] DATETIME StartTime,
  [in] DATETIME ForceLogOffTime,
  [in] string   JobInputXml
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartTime* \[在\]
</dt> <dd>

> [!Note]  
> 系統將不會登出虛擬機器的使用者，直到 *ForceLogOffTime* 參數中指定的時間為止。

 

安裝更新的日期和時間。

</dd> <dt>

*ForceLogOffTime* \[在\]
</dt> <dd>

系統將登出虛擬機器使用者的日期和時間。

</dd> <dt>

*JobInputXml* \[在\]
</dt> <dd>

XML 格式的字串，其中包含軟體更新作業資訊。

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

 

 





