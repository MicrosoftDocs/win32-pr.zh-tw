---
title: Win32_TSVirtualIP 類別的 SetVirtualIPMode 方法
description: 設定 VirtualIPMode 屬性值。
ms.assetid: d4b39566-ad2a-493b-8022-c006a857043d
ms.tgt_platform: multiple
keywords:
- SetVirtualIPMode 方法遠端桌面服務
- SetVirtualIPMode 方法遠端桌面服務，Win32_TSVirtualIP 類別
- Win32_TSVirtualIP 類別遠端桌面服務，SetVirtualIPMode 方法
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250633f5d41f5a4a7cb06a17ba9ae45bb444a018
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106979685"
---
# <a name="setvirtualipmode-method-of-the-win32_tsvirtualip-class"></a>Win32 TSVirtualIP 類別的 SetVirtualIPMode 方法 \_

設定 **VirtualIPMode** 屬性值。

## <a name="syntax"></a>語法


```mof
uint32 SetVirtualIPMode(
  [in] uint32 VirtualIPMode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VirtualIPMode* \[在\]
</dt> <dd>

類型： **uint32**

指定要在伺服器上使用的 IP 虛擬化模式。 這可以是下列其中一個值。

<dt>

0
</dt> <dd>

IP 虛擬化模式為每個會話。

</dd> <dt>

1
</dt> <dd>

IP 虛擬化模式為每位使用者。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。 如果設定位於群組原則控制之下，則方法會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                       |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 





