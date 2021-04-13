---
title: MDM_WindowsLicensing 類別的 ChangeProductKeyMethod 方法
description: 這個方法會安裝 Windows 10 桌面裝置的產品金鑰。 點不會重新開機。 另請參閱 ChangeProductKey。
ms.assetid: 1d9e3243-2ca4-427b-bda2-d33e1e70c80d
keywords:
- ChangeProductKeyMethod 方法
- ChangeProductKeyMethod 方法，MDM_WindowsLicensing 類別
- MDM_WindowsLicensing 類別，ChangeProductKeyMethod 方法
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.ChangeProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e00345fb0e23655b457e0540c70289a169c54ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466193"
---
# <a name="changeproductkeymethod-method-of-the-mdm_windowslicensing-class"></a>MDM WindowsLicensing 類別的 ChangeProductKeyMethod 方法 \_

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

這個方法會安裝 Windows 10 桌面裝置的產品金鑰。 點不會重新開機。 另請參閱 [ChangeProductKey](/windows/client-management/mdm/windowslicensing-csp)

## <a name="syntax"></a>語法


```mof
uint32 ChangeProductKeyMethod(
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
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MDM \_ WindowsLicensing**](mdm-windowslicensing.md)
</dt> </dl>

 

