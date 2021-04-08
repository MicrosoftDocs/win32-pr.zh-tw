---
description: 模擬電子報按鍵序列。
ms.assetid: 4166BA71-315D-41BD-857C-48AFB702911E
title: Msvm_Keyboard 類別的 TypeKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1b978da48600cc52472ab8bdec011ddbaa5ff624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945068"
---
# <a name="typekey-method-of-the-msvm_keyboard-class"></a>Msvm 鍵盤類別的 TypeKey 方法 \_

模擬電子報按鍵序列。 這相當於呼叫 [**PressKey**](presskey-msvm-keyboard.md) ，後面接著 [**ReleaseKey**](releasekey-msvm-keyboard.md)。

## <a name="syntax"></a>語法


```mof
uint32 TypeKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*keyCode* \[在\]
</dt> <dd>

類型： **uint32**

要按下之按鍵的虛擬按鍵碼。 如需虛擬機器碼的清單，請參閱 [**虛擬金鑰代碼**](../inputdev/virtual-key-codes.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

傳回值為零表示成功。 非零值表示無法修改金鑰狀態。

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

**System 使用** (32774) 
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

[**Msvm \_ 鍵盤**](msvm-keyboard.md)類別的存取權可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**Msvm \_ 鍵盤**](msvm-keyboard.md)
</dt> <dt>

[**虛擬金鑰碼**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

