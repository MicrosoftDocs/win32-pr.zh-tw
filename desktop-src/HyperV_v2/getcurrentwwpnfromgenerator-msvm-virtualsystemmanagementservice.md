---
description: 提供在不保留 WWPN 的情況下，預覽目前全球埠名稱 (WWPN) 的功能。
ms.assetid: 7fc02099-744e-4a56-ae4b-1f5fd6a1eb45
title: Msvm_VirtualSystemManagementService 類別的 GetCurrentWwpnFromGenerator 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetCurrentWwpnFromGenerator
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 88e1fd8f19b4a0542744cbfff7058ed7e69a421d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943522"
---
# <a name="getcurrentwwpnfromgenerator-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 GetCurrentWwpnFromGenerator 方法 \_

提供在不保留 WWPN 的情況下，預覽目前全球埠名稱 (WWPN) 的功能。 WWPN 是從 [**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md)類別的 **MinimumWWPNAddress** 和 **MaximumWWPNAddress** 屬性所定義的預先設定範圍內產生的。 如果這些屬性所定義的範圍已用盡，則產生的 WWPN 將會有不正確專案 "0000000000000000"，且傳回值會指出成功 (0) 。

## <a name="syntax"></a>語法


```mof
uint32 GetCurrentWwpnFromGenerator(
  [out] string CurrentWwpn
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CurrentWwpn* \[擴展\]
</dt> <dd>

具有 WWPN 產生器所使用之目前 WWPN 值的字串。 這將會是與後續呼叫 [**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)所產生的第一個 WWPN 相同的值。 它會以字串形式格式化為 "01：23：45：67：89： ab： cd： ef"。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**無法** (32768) 
</dt> <dt>

**拒絕存取** (32769) 
</dt> <dt>

**不支援** (32770) 
</dt> <dt>

**狀態未知** (32771) 
</dt> <dt>

**Timeout** (32772) 
</dt> <dt>

**不正確參數** (32773) 
</dt> <dt>

**系統正在使用中** (32774) 
</dt> <dt>

**此操作的狀態無效** (32775) 
</dt> <dt>

**不正確的資料類型** (32776) 
</dt> <dt>

**系統無法使用** (32777) 
</dt> <dt>

**記憶體不足** (32778) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




