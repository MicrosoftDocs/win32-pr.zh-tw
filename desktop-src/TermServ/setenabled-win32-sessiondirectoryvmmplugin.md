---
title: Win32_SessionDirectoryVMMPlugin 類別的 SetEnabled 方法
description: 啟用或停用外掛程式。
ms.assetid: 25ce0614-5c3b-4a79-9174-1a9de1eb6c33
ms.tgt_platform: multiple
keywords:
- SetEnabled 方法遠端桌面服務
- SetEnabled 方法遠端桌面服務，Win32_SessionDirectoryVMMPlugin 類別
- Win32_SessionDirectoryVMMPlugin 類別遠端桌面服務，SetEnabled 方法
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetEnabled
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d33b7a5255e5dc59624e7aa540246ed08e56003b1e9917b86dfe90137db5b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118851475"
---
# <a name="setenabled-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Win32 SessionDirectoryVMMPlugin 類別的 SetEnabled 方法 \_

啟用或停用外掛程式。

## <a name="syntax"></a>語法


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

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

 

 





