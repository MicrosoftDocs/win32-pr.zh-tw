---
description: Msvm_Ps2Mouse 類別的 GetButtonState 方法-抓取指定裝置按鈕的目前狀態。
ms.assetid: 7772A3AC-1677-44A7-9E5E-D31E90988705
title: Msvm_Ps2Mouse 類別的 GetButtonState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 160134a2ae48bb23dc525eeded70b483484e0b71
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112196"
---
# <a name="getbuttonstate-method-of-the-msvm_ps2mouse-class"></a>Msvm Ps2Mouse 類別的 GetButtonState 方法 \_

抓取指定裝置按鈕的目前狀態。

## <a name="syntax"></a>語法


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean buttonState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*buttonIndex* \[在\]
</dt> <dd>

類型： **uint32**

要查詢之按鈕的索引（以1為基礎）。

</dd> <dt>

*buttonState* \[擴展\]
</dt> <dd>

類型： **布林值**

按鈕目前的關閉狀態。 **True** 值表示按鈕已關閉。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

傳回值為零表示成功。 非零值表示查詢失敗。

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

存取 [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md) 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)
</dt> </dl>

 

