---
title: Win32_TSClientSetting 類別的 SetAllowDwm 方法
description: 設定 AllowDwm 屬性。
ms.assetid: c70d3dc9-c109-4d77-be50-20a0352282d6
ms.tgt_platform: multiple
keywords:
- SetAllowDwm 方法遠端桌面服務
- SetAllowDwm 方法遠端桌面服務，Win32_TSClientSetting 類別
- Win32_TSClientSetting 類別遠端桌面服務，SetAllowDwm 方法
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetAllowDwm
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e48373859e59464986aab85bf00d16a76a066bad12e3e38bf7b07275257016
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009028"
---
# <a name="setallowdwm-method-of-the-win32_tsclientsetting-class"></a>Win32 TSClientSetting 類別的 SetAllowDwm 方法 \_

設定 **AllowDwm** 屬性。

## <a name="syntax"></a>語法


```mof
uint32 SetAllowDwm(
  [in] uint32 AllowDwm
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AllowDwm* \[在\]
</dt> <dd>

新的 **AllowDwm** 屬性值。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。 如果伺服器已覆寫使用者的連接設定，此方法會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                       |
| 用戶端支援結束<br/>    | 都不支援<br/>                                                               |
| 伺服器支援結束<br/>    | Windows Server 2008 R2<br/>                                                       |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

 





