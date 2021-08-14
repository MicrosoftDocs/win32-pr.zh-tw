---
description: 針對指定的內嵌 Msvm 錯誤實例陣列，傳回格式化的錯誤訊息字串 \_ 。
ms.assetid: 477EF4AE-00A8-4F2D-A335-E41A2EF620BB
title: Msvm_VirtualSystemManagementService 類別的造成 stringbuilder.formaterror 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.FormatError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31b7f2ba03c21c08af3b9249c0ee3099291fdd190d22516ed503c012dae63f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253948"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的造成 stringbuilder.formaterror 方法 \_

針對指定的內嵌 [**Msvm \_ 錯誤**](msvm-error.md) 實例陣列，傳回格式化的錯誤訊息字串。

## <a name="syntax"></a>語法


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*錯誤* \[在\]
</dt> <dd>

類型：**字串 \[ \]**

字串陣列，其中包含用來產生輸出錯誤訊息的 [**Msvm \_ 錯誤**](msvm-error.md) 實例。

</dd> <dt>

*ErrorMessage* \[擴展\]
</dt> <dd>

類型： **字串**

在輸出中，包含由 *錯誤* 參數中傳遞的 [**Msvm \_ 錯誤**](msvm-error.md)實例所代表之串連錯誤訊息的字串。 每個錯誤字串都會以一對換行字元分隔 ( ' \\ n ' ) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
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

## <a name="remarks"></a>備註

存取 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**造成 stringbuilder.formaterror (V1)**](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

