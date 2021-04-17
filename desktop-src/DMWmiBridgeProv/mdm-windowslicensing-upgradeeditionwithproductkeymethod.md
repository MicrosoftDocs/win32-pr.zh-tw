---
title: MDM_WindowsLicensing 類別的 UpgradeEditionWithProductKeyMethod 方法
description: 輸入 Windows 10 桌面裝置版本升級的產品金鑰。 另請參閱 UpgradeEditionWithProductKey。
ms.assetid: 6576fb5c-210c-4979-8c01-ed8f78e72c2c
keywords:
- UpgradeEditionWithProductKeyMethod 方法
- UpgradeEditionWithProductKeyMethod 方法，MDM_WindowsLicensing 類別
- MDM_WindowsLicensing 類別，UpgradeEditionWithProductKeyMethod 方法
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85824fc6fac9e5a15bf2bc890215afcbd0958680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466192"
---
# <a name="upgradeeditionwithproductkeymethod-method-of-the-mdm_windowslicensing-class"></a>MDM WindowsLicensing 類別的 UpgradeEditionWithProductKeyMethod 方法 \_

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

輸入 Windows 10 桌面裝置版本升級的產品金鑰。 另請參閱 [UpgradeEditionWithProductKey](/windows/client-management/mdm/windowslicensing-csp)。

## <a name="syntax"></a>語法


```mof
uint32 UpgradeEditionWithProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*param* \[在\]
</dt> <dd>

產品金鑰。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                    |
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

 

