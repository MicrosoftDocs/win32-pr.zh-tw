---
description: 模擬金鑰版本。
ms.assetid: EAE84BD5-ECEA-44E7-A7AB-CD18299DF2FE
title: Msvm_Keyboard 類別的 ReleaseKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.ReleaseKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1038838ad7ab0c483dd23e77a716da3ffd2474f7a9e8b4fb311b4a141c1ababb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980128"
---
# <a name="releasekey-method-of-the-msvm_keyboard-class"></a>Msvm 鍵盤類別的 ReleaseKey 方法 \_

模擬金鑰版本。 成功時，金鑰會處於啟動狀態。

## <a name="syntax"></a>語法


```mof
uint32 ReleaseKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*keyCode* \[在\]
</dt> <dd>

類型： **uint32**

要釋放之金鑰的虛擬按鍵碼。 如需虛擬機器碼的清單，請參閱 [**虛擬金鑰代碼**](../inputdev/virtual-key-codes.md)。

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

**ReleaseKey** 方法會將 [VK] **\_ 功能表** 的參考（ (18) 、 **VK \_ CONTROL** (17) 和 **VK \_ SHIFT** (16) 分別對應至 **VK \_ LMENU** (164) 、 **VK \_ LCONTROL** (162) 和 **VK \_ LSHIFT** (160) ，因為 **VK \_ 功能表**、 **VK \_ 控制項** 和 **VK \_ SHIFT** 虛擬按鍵代碼不代表鍵盤上的實際按鍵。

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

 

