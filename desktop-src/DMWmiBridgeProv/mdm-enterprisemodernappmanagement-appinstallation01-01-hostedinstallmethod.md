---
title: MDM_EnterpriseModernAppManagement_AppInstallation01_01 類別的 HostedInstallMethod 方法
description: 從託管位置（例如本機磁片磁碟機、UNC 或 HTTPS 資料來源）執行應用程式套件安裝的方法。 另請參閱 HostedInstall。
ms.assetid: 1ec16315-75ce-4613-804e-6b587c4071d6
keywords:
- HostedInstallMethod 方法
- HostedInstallMethod 方法，MDM_EnterpriseModernAppManagement_AppInstallation01_01 類別
- MDM_EnterpriseModernAppManagement_AppInstallation01_01 類別，HostedInstallMethod 方法
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.HostedInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60cd27419dce09b2a0e4aa7304bb53ac63e7d205b93cbaacbf832aa4a3501338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750628"
---
# <a name="hostedinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a>MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 類別的 HostedInstallMethod 方法

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

從託管位置（例如本機磁片磁碟機、UNC 或 HTTPS 資料來源）執行應用程式套件安裝的方法。 另請參閱 [HostedInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp)。

## <a name="syntax"></a>語法


```mof
uint32 HostedInstallMethod(
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

[**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01**](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

