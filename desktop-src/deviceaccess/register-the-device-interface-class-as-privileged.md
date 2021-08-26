---
title: 將裝置介面註冊為受特殊許可權的應用程式限制
description: 本主題說明如何新增受限制的屬性，指出只有特殊許可權的應用程式可以存取裝置介面類別別。
ms.assetid: BCEB1FBF-3D3F-45B8-A92B-7C5FBF6745C0
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 62bca034a2edab9b31267f14672b4821ca6569dead0fd645d98c52c234c24cb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029048"
---
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a>將裝置介面註冊為受特殊許可權的應用程式限制

除非應用程式被簽署的裝置中繼資料授與許可權，否則會拒絕應用程式存取自訂驅動程式功能。 本主題說明如何新增 **受限制** 的屬性，指出只有特殊許可權的應用程式可以存取裝置介面類別別。 自訂設備磁碟機必須有這個屬性。

## <a name="instructions"></a>指示

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a>在資訊 (INF) 檔中設定受限制的屬性

在 `InterfaceInstall32` 區段中，會註冊裝置介面類別別的 GUID。

**AddProperty** 指示詞底下的行會設定裝置類別屬性。 第二行則是在自訂屬性分類中設定自訂屬性。 屬性類別 GUID 是 **14c83a99-0b3f-44b7-be4c-a178d3990564**，而屬性識別碼是 **2**。 選擇性的 `Flags` 專案值不存在，且類型為 **17** (**DEVPROP_TYPE_BOOLEAN**) 。 屬性的值為 **1**。

```Text
; Below, {11111111-0000-1111-0000-111111111111} is the GUID of the
; new device interface class in an AddInterface directive



; -- Interface installation
[InterfaceInstall32]
{11111111-0000-1111-0000-111111111111}=NewInterfaceInstall

[NewInterfaceInstall]
AddProperty=PrivilegedProperties

[PrivilegedProperties]
; DEVPKey_DeviceInterfaceClass_Restricted
{14c83a99-0b3f-44b7-be4c-a178d3990564}, 2, 17,,1 ; -- non-zero indicates privileged
```

## <a name="remarks"></a>備註

驅動程式也可以呼叫 [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata)常式來註冊裝置介面類別別，而不是 **AddInterface** 指示詞。

您也可以藉由呼叫 [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) 常式來設定受限制的介面屬性。

## <a name="related-topics"></a>相關主題

[自訂驅動程式存取範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)、[適用于內部裝置的 UWP 裝置應用程式](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices)、[硬體開發人員中心](/windows-hardware/drivers/)
