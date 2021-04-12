---
title: Win32_SessionDirectoryVMMPlugin 類別的 RegisterVMMPlugin 方法
description: 註冊新的 VMM 外掛程式。
ms.assetid: 8fa6109e-6320-4ad1-b313-f100d8383f85
ms.tgt_platform: multiple
keywords:
- RegisterVMMPlugin 方法遠端桌面服務
- RegisterVMMPlugin 方法遠端桌面服務，Win32_SessionDirectoryVMMPlugin 類別
- Win32_SessionDirectoryVMMPlugin 類別遠端桌面服務，RegisterVMMPlugin 方法
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.RegisterVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381be34f9398147b323fa99093479da48adfd480
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384278"
---
# <a name="registervmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Win32 SessionDirectoryVMMPlugin 類別的 RegisterVMMPlugin 方法 \_

註冊新的 VMM 外掛程式。

## <a name="syntax"></a>語法


```mof
uint32 RegisterVMMPlugin(
  [in] string  sName,
  [in] string  sProvider,
  [in] string  sServiceLocation,
  [in] string  sClassID,
  [in] sint32  Priority = ,
  [in] boolean Enabled = 
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sName* \[在\]
</dt> <dd>

外掛程式的名稱。

</dd> <dt>

*sProvider* \[在\]
</dt> <dd>

外掛程式提供者的名稱。

</dd> <dt>

*sServiceLocation* \[在\]
</dt> <dd>

外掛程式應聯絡的服務位置。

</dd> <dt>

*sClassID* \[在\]
</dt> <dd>

外掛程式的類別識別碼。

</dd> <dt>

*優先順序* \[在\]
</dt> <dd>

外掛程式的優先順序。 值愈高，外掛程式的優先順序愈高。

</dd> <dt>

*已啟用* \[在\]
</dt> <dd>

指出外掛程式是否已啟用或停用。 如果外掛程式已啟用則 **為 True** ，否則為 **false** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                      |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ SessionDirectoryVMMPlugin**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





