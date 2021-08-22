---
description: 產生一組全球通訊埠名稱 (WWPNs) 。
ms.assetid: 36f393eb-6f34-4ae3-a976-c5da60211f3e
title: Msvm_VirtualSystemManagementService 類別的 GenerateWwpn 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GenerateWwpn
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1952954d107185fdcc31634b9d0e19bd4cd3450db5a63d78aa3ef823cdf38afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532518"
---
# <a name="generatewwpn-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 GenerateWwpn 方法 \_

產生一組全球通訊埠名稱 (WWPNs) 。 WWPNs 是從 [**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md)類別的 **MinimumWWPNAddress** 和 **MaximumWWPNAddress** 屬性所定義的預先設定範圍內產生的。 如果可以產生的有效 WWPNs 數目小於所要求的數目，則 *GeneratedWwpn* 陣列中的其餘專案將會有不正確 "0000000000000000" 專案，而且傳回值會指出成功 (0) 。

## <a name="syntax"></a>語法


```mof
uint32 GenerateWwpn(
  [in]  uint32 NumberOfWwpns,
  [out] string GeneratedWwpn[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NumberOfWwpns* \[在\]
</dt> <dd>

要產生的 WWPNs 數目。

</dd> <dt>

*GeneratedWwpn* \[擴展\]
</dt> <dd>

字串陣列，其中每個字串都包含產生的 WWPN。 它會以字串形式格式化為 "01：23：45：67：89： ab： cd： ef"。

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
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




