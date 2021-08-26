---
title: MDM_RemoteWipe 類別的 doWipeMethod 方法
description: 觸發裝置以啟動遠端清除。
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- doWipeMethod 方法
- doWipeMethod 方法，MDM_RemoteWipe 類別
- MDM_RemoteWipe 類別，doWipeMethod 方法
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cff9cb831931c96fa8df1b376f96ea4c20b05bafdb12a85dec00b4f505af4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045638"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a>MDM RemoteWipe 類別的 doWipeMethod 方法 \_

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

觸發裝置以啟動遠端清除。 另請參閱 [doWipe](/windows/client-management/mdm/remotewipe-csp)。

## <a name="syntax"></a>語法


```mof
uint32 doWipeMethod(
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
| 命名空間<br/>                | 根 \\ CIMv2 \\ MDM \\ DMMap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MDM \_ RemoteWipe**](mdm-remotewipe.md)
</dt> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

