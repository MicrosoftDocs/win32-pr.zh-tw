---
title: MDM_WindowsLicensing 類別的 CheckApplicabilityMethod 方法
description: 檢查輸入的產品金鑰是否可用於版本升級、啟用或變更桌面裝置 Windows 10 的產品金鑰。 另請參閱 CheckApplicability。
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- CheckApplicabilityMethod 方法
- CheckApplicabilityMethod 方法，MDM_WindowsLicensing 類別
- MDM_WindowsLicensing 類別，CheckApplicabilityMethod 方法
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.CheckApplicabilityMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db236e05ffe7b5b6273e7cba594266c31720932b43a7df2de751a0fa66cced5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750148"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a>MDM WindowsLicensing 類別的 CheckApplicabilityMethod 方法 \_

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

檢查輸入的產品金鑰是否可用於版本升級、啟用或變更桌面裝置 Windows 10 的產品金鑰。 另請參閱 [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp)。

## <a name="syntax"></a>語法


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*param* \[在\]
</dt> <dd>

產品金鑰。

</dd> </dl>

## <a name="return-value"></a>傳回值

TRUE 或 FALSE

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

 

