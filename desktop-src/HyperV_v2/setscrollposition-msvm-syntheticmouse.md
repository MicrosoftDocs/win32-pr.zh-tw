---
description: 設定指向指標裝置之滾輪控制項的 z 座標。
ms.assetid: 02349957-6BAA-42E7-B3D4-F39E748615E6
title: Msvm_SyntheticMouse 類別的 SetScrollPosition 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetScrollPosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6d82ad2cd75b41ca914d0db49d5de4709790ea6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115761"
---
# <a name="setscrollposition-method-of-the-msvm_syntheticmouse-class"></a>Msvm SyntheticMouse 類別的 SetScrollPosition 方法 \_

設定指向指標裝置之滾輪控制項的 z 座標。 寫入這個屬性的值一律為相對座標位移。

## <a name="syntax"></a>語法


```mof
uint32 SetScrollPosition(
  [in] sint32 scrollPositionDelta
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*scrollPositionDelta* \[在\]
</dt> <dd>

類型： **sint32**

捲軸位置的差異。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

傳回值為零表示成功。 非零值表示無法改變捲軸位置。

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

存取 [**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md) 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md)
</dt> </dl>

 

