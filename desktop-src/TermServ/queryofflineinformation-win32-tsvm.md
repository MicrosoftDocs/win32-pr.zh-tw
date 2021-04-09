---
title: Win32_TSVm 類別的 QueryOfflineInformation 方法
description: )  (的虛擬桌面伺服器的屬性，但是只有在伺服器離線時，才會加以抓取。
ms.assetid: f6ce74cb-a4a4-4e05-a0a7-bac0b7f52c45
ms.tgt_platform: multiple
keywords:
- QueryOfflineInformation 方法遠端桌面服務
- QueryOfflineInformation 方法遠端桌面服務，Win32_TSVm 類別
- Win32_TSVm 類別遠端桌面服務，QueryOfflineInformation 方法
topic_type:
- apiref
api_name:
- Win32_TSVm.QueryOfflineInformation
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4750ebdb82b08ae1ed0350e1ac448d9aca4003b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843844"
---
# <a name="queryofflineinformation-method-of-the-win32_tsvm-class"></a>Win32 TSVm 類別的 QueryOfflineInformation 方法 \_

)  (的虛擬桌面伺服器的屬性，但是只有在伺服器離線時，才會加以抓取。

## <a name="syntax"></a>語法


```mof
uint32 QueryOfflineInformation(
  [out] string  Build,
  [out] string  CurrentVersion,
  [out] string  InstallationType,
  [out] string  EditionId,
  [out] string  SysPrepImageState,
  [out] string  SysPrepMode,
  [out] sint32  ProcArch,
  [out] boolean fIsVmbusCapable,
  [out] boolean fIsRdvIcInstalled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*組建* \[擴展\]
</dt> <dd>

成功時，會傳回 VDS 的組建版本。

</dd> <dt>

*CurrentVersion* \[擴展\]
</dt> <dd>

成功時，會傳回 VDS 的目前版本。

</dd> <dt>

*InstallationType* \[擴展\]
</dt> <dd>

成功時，會傳回 VDS 的安裝類型。

</dd> <dt>

*EditionId* \[擴展\]
</dt> <dd>

成功時，會傳回 VDS 的版本識別碼。

</dd> <dt>

*SysPrepImageState* \[擴展\]
</dt> <dd>

成功時，會傳回 VDS 的系統準備映射狀態。

</dd> <dt>

*SysPrepMode* \[擴展\]
</dt> <dd>

成功時，會傳回 VDS 的系統準備模式。

</dd> <dt>

*ProcArch* \[擴展\]
</dt> <dd>

成功時，會傳回表示處理器架構的值。

<dt>

0
</dt> <dd>

x86

</dd> <dt>

1
</dt> <dd>

amd64

</dd> </dl> </dd> <dt>

*fIsVmbusCapable* \[擴展\]
</dt> <dd>

成功時，會指出系統是否支援 VMBus。

</dd> <dt>

*fIsRdvIcInstalled* \[擴展\]
</dt> <dd>

成功時，表示是否已安裝 RDVIC。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                             |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSVm**](win32-tsvm.md)
</dt> </dl>

 

 





