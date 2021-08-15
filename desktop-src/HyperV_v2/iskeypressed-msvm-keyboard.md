---
description: 捕獲索引鍵的索引鍵狀態。
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: Msvm_Keyboard 類別的 IsKeyPressed 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.IsKeyPressed
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb8b4e2da0a6f1cd3c30e3d65404ecf308c71e88483e322193497216586b20b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392441"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a>Msvm 鍵盤類別的 IsKeyPressed 方法 \_

捕獲索引鍵的索引鍵狀態。

## <a name="syntax"></a>語法


```mof
uint32 IsKeyPressed(
  [in]  uint32  keyCode,
  [out] boolean keyState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*keyCode* \[在\]
</dt> <dd>

類型： **uint32**

要查詢之索引鍵的虛擬按鍵碼。 如需虛擬機器碼的清單，請參閱 [**虛擬金鑰代碼**](../inputdev/virtual-key-codes.md)。

</dd> <dt>

*keyState* \[擴展\]
</dt> <dd>

類型： **布林值**

機碼目前的關閉狀態。 **True** 值表示金鑰已關閉。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

傳回值為零表示成功。 非零值表示無法查詢索引鍵狀態。

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

**IsKeyPressed** 方法一律會針對 [ **VK] \_ 功能表** (18) 、 **VK \_ CONTROL** (17) 和 **VK \_ SHIFT** (16) 傳回 **False** ，因為這些不是鍵盤上的實際按鍵。 這些虛擬機器碼程式碼一律會分別對應到 **VK \_ LMENU** (164) 、 **VK \_ LCONTROL** (162) 和 **VK \_ LSHIFT** (160) ，方法是 [**PressKey**](presskey-msvm-keyboard.md) 和 [**ReleaseKey**](releasekey-msvm-keyboard.md) 方法。

[**Msvm \_ 鍵盤**](msvm-keyboard.md)類別的存取權可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**Msvm \_ 鍵盤**](msvm-keyboard.md)
</dt> <dt>

[**虛擬金鑰碼**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

