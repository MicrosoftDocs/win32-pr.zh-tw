---
title: Win32_SessionDirectoryVMMPlugin 類別的 SetServiceLocation 方法
description: 設定外掛程式的服務位置。
ms.assetid: e886a40b-9ea9-4159-a2ea-776160559410
ms.tgt_platform: multiple
keywords:
- SetServiceLocation 方法遠端桌面服務
- SetServiceLocation 方法遠端桌面服務，Win32_SessionDirectoryVMMPlugin 類別
- Win32_SessionDirectoryVMMPlugin 類別遠端桌面服務，SetServiceLocation 方法
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetServiceLocation
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 437de0ab08b5735c1a981e5d04e8958a930d6eab1bfef79ccd7befa844a499dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349399"
---
# <a name="setservicelocation-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Win32 SessionDirectoryVMMPlugin 類別的 SetServiceLocation 方法 \_

設定外掛程式的服務位置。

## <a name="syntax"></a>語法


```mof
uint32 SetServiceLocation(
  [in] string sServiceLocation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sServiceLocation* \[在\]
</dt> <dd>

外掛程式應聯絡的服務位置。

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

 

 





