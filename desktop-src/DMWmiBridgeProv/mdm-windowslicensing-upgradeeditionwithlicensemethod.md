---
title: MDM_WindowsLicensing 類別的 UpgradeEditionWithLicenseMethod 方法
description: 為 Windows 10 行動裝置的版本升級提供授權的方法。 另請參閱 UpgradeEditionWithLicense。
ms.assetid: 1a57fb71-eea6-41bf-bc44-6d3a816096a4
keywords:
- UpgradeEditionWithLicenseMethod 方法
- UpgradeEditionWithLicenseMethod 方法，MDM_WindowsLicensing 類別
- MDM_WindowsLicensing 類別，UpgradeEditionWithLicenseMethod 方法
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithLicenseMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26329c98bc73919d374787deea21841a2912a9df3fded8fdcde0637d8798c92f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913258"
---
# <a name="upgradeeditionwithlicensemethod-method-of-the-mdm_windowslicensing-class"></a>MDM WindowsLicensing 類別的 UpgradeEditionWithLicenseMethod 方法 \_

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

為 Windows 10 行動裝置的版本升級提供授權的方法。 另請參閱 [UpgradeEditionWithLicense](/windows/client-management/mdm/windowslicensing-csp)。

## <a name="syntax"></a>語法


```mof
uint32 UpgradeEditionWithLicenseMethod(
  [in] string param
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*param* \[在\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MDM \_ WindowsLicensing**](mdm-windowslicensing.md)
</dt> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

