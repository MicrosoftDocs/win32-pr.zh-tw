---
title: Win32_TSSessionDirectory 類別的 SetServerWeight 方法
description: 設定遠端桌面連線代理人 (RD 連線代理人) 負載平衡的伺服器加權值。
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- SetServerWeight 方法遠端桌面服務
- SetServerWeight 方法遠端桌面服務，Win32_TSSessionDirectory 類別
- Win32_TSSessionDirectory 類別遠端桌面服務，SetServerWeight 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetServerWeight
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d8c9af7995f2d42f02075fde8ae43f4b5f5e9a5ccb7d3fa6f4635cb9645464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604627"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a>Win32 TSSessionDirectory 類別的 SetServerWeight 方法 \_

設定遠端桌面連線代理人 (RD 連線代理人) 負載平衡的伺服器加權值。

## <a name="syntax"></a>語法


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ServerWeightValue* \[在\]
</dt> <dd>

類型： **uint32**

伺服器加權值。 有效範圍是1至10000。

</dd> </dl>

## <a name="remarks"></a>備註

依預設，在遠端桌面服務設定的使用者介面中，伺服器權數值是100。 伺服器權數是相對的。 因此，如果您為一部伺服器指派的值為100，而其中一個值為200，則相對權數為200的伺服器將會收到會話數目的兩倍。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

