---
title: Win32_TSNetworkAdapterSetting 類別的 SetNetworkAdapterLanaID 方法
description: 指定要設定之網路介面卡的局域網路介面卡 (LANA) 號碼。
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- SetNetworkAdapterLanaID 方法遠端桌面服務
- SetNetworkAdapterLanaID 方法遠端桌面服務，Win32_TSNetworkAdapterSetting 類別
- Win32_TSNetworkAdapterSetting 類別遠端桌面服務，SetNetworkAdapterLanaID 方法
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SetNetworkAdapterLanaID
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5ffe976da794714f01e711913c01216d6b9bfad30c8c337da1fbd4c796e5f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008958"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a>Win32 TSNetworkAdapterSetting 類別的 SetNetworkAdapterLanaID 方法 \_

**SetNetworkAdapterLanaID** 方法會指定要設定之網路介面卡的局域網路介面卡 (LANA) 號碼。 如果指定的 LANA 識別碼無效或不存在，就會傳回錯誤。 可透過列舉 [**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)類別中的屬性 **DeviceIDList** 來取得 LANA 識別碼的可用清單。

## <a name="syntax"></a>語法


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NetworkAdapterLanaID* \[在\]
</dt> <dd>

要設定的網路介面卡的 LANA 號碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。

## <a name="remarks"></a>備註

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

 

