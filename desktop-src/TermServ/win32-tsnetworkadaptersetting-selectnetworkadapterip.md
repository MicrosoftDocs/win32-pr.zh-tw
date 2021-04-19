---
title: Win32_TSNetworkAdapterSetting 類別的 SelectNetworkAdapterIP 方法
description: 選取以介面卡的 IP 位址為基礎的網路介面卡。
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- SelectNetworkAdapterIP 方法遠端桌面服務
- SelectNetworkAdapterIP 方法遠端桌面服務，Win32_TSNetworkAdapterSetting 類別
- Win32_TSNetworkAdapterSetting 類別遠端桌面服務，SelectNetworkAdapterIP 方法
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectNetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9590bab26b3cda2e20a3dc74c5e201a2f7f86f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969578"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a>Win32 TSNetworkAdapterSetting 類別的 SelectNetworkAdapterIP 方法 \_

選取以介面卡的 IP 位址為基礎的網路介面卡。

## <a name="syntax"></a>語法


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NetworkAdapterIP* \[在\]
</dt> <dd>

要設定之網路介面卡的 IP 位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果指定的 IP 位址有效，則傳回零，如果 IP 位址無效或不存在，則傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。

## <a name="remarks"></a>備註

您可以藉由列舉 [**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md) 類別的屬性，來取得網路介面卡的 IP 位址。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

