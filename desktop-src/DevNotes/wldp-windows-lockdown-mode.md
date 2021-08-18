---
description: 說明 Windows 裝置) 的安全模式 (S 模式。
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: 'WLDP_WINDOWS_LOCKDOWN_MODE 列舉 (Wldp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_WINDOWS_LOCKDOWN_MODE
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 93a3ae8ef00c306d93995a3a97236fc9086185147144c4314726c507d8b52e57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911338"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a>WLDP \_ WINDOWS \_ 鎖定 \_ 模式列舉

說明 Windows 裝置) 的安全模式 (S 模式。 主要用於 [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md)。

## <a name="syntax"></a>Syntax


```C++
typedef enum _WLDP_WINDOWS_LOCKDOWN_MODE { 
  WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED  = 0,
  WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL     = 1,
  WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED    = 2,
  WLDP_WINDOWS_LOCKDOWN_MODE_MAX       = 3
} WLDP_WINDOWS_LOCKDOWN_MODE, *PWLDP_WINDOWS_LOCKDOWN_MODE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**WLDP \_ WINDOWS \_ 鎖定 \_ 模式已 \_ 解除鎖定**
</dt> <dd>

解 鎖。 主要用於沒有 S 模式的 Windows 裝置。

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**WLDP \_ WINDOWS \_ 鎖定 \_ 模式 \_ 試用版**
</dt> <dd>

試驗。 主要用於具有 S 模式的 Windows 10 試用版裝置。 試用模式是以 S 模式 Windows 10 裝置的特殊案例：原則會強制執行，但沒有強制執行原則的復原保護。

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP \_ WINDOWS \_ 鎖定 \_ 模式已 \_ 鎖定**
</dt> <dd>

鎖。 主要用於具有 S 模式的 Windows 10 裝置。 鎖定的裝置將會強制執行以 S 模式隨附 Windows 10 OS 映射的已簽署 device Guard 原則。

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP \_ WINDOWS \_ 鎖定 \_ 模式 \_ 最大值**
</dt> <dd>

最大的列舉值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wldp。h</dt> </dl> |



 

 




