---
title: Win32_TSVirtualIP 類別的 SetVirtualizeLoopbackAddressesEnabled 方法
description: 設定 VirtualizeLoopbackAddressesEnabled 屬性值。
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- SetVirtualizeLoopbackAddressesEnabled 方法遠端桌面服務
- SetVirtualizeLoopbackAddressesEnabled 方法遠端桌面服務，Win32_TSVirtualIP 類別
- Win32_TSVirtualIP 類別遠端桌面服務，SetVirtualizeLoopbackAddressesEnabled 方法
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5168ddd271dcf013a7595be1e1bdf32cde91e8f9f3ce8cfebc3b9f39af1fa109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000487"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a>Win32 TSVirtualIP 類別的 SetVirtualizeLoopbackAddressesEnabled 方法 \_

設定 **VirtualizeLoopbackAddressesEnabled** 屬性值。

## <a name="syntax"></a>語法


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VirtualizeLoopbackAddressesEnabled* \[在\]
</dt> <dd>

指定是否啟用回送位址虛擬化。 這可以是下列其中一個值。

<dt>

0
</dt> <dd>

請勿啟用回送位址虛擬化。

</dd> <dt>

1
</dt> <dd>

啟用回送位址虛擬化。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。 如果設定位於群組原則控制之下，則方法會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 





