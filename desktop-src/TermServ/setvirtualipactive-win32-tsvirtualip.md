---
title: Win32_TSVirtualIP 類別的 SetVirtualIPActive 方法
description: 設定 VirtualIPActive 屬性值。
ms.assetid: e485aeb1-afdf-4572-bac7-daa80d903edc
ms.tgt_platform: multiple
keywords:
- SetVirtualIPActive 方法遠端桌面服務
- SetVirtualIPActive 方法遠端桌面服務，Win32_TSVirtualIP 類別
- Win32_TSVirtualIP 類別遠端桌面服務，SetVirtualIPActive 方法
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06534c967c5d86a7a19c060254b3b988ff98b17e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934572"
---
# <a name="setvirtualipactive-method-of-the-win32_tsvirtualip-class"></a>Win32 TSVirtualIP 類別的 SetVirtualIPActive 方法 \_

設定 **VirtualIPActive** 屬性值。

## <a name="syntax"></a>語法


```mof
uint32 SetVirtualIPActive(
  [in] uint32 VirtualIPActive
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VirtualIPActive* \[在\]
</dt> <dd>

類型： **uint32**

指定伺服器上的 IP 虛擬化是否為作用中狀態。 這可以是下列其中一個值。

<dt>

零
</dt> <dd>

IP 虛擬化未啟用。

</dd> <dt>

零
</dt> <dd>

IP 虛擬化處於作用中狀態。

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

 

 





