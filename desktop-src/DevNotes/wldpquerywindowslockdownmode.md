---
description: 抓取目前的 Windows 安全模式。 Windows 可以處於鎖定模式、已解除鎖定的一般模式或試用模式。
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: 'WldpQueryWindowsLockdownMode 函式 (Wldp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryWindowsLockdownMode
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 94dc1665dcfa98b27fc15f68a799792b57f428875fefb88c6d35de57bad71b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911288"
---
# <a name="wldpquerywindowslockdownmode-function"></a>WldpQueryWindowsLockdownMode 函式

抓取目前的 Windows 安全模式。 Windows 可以處於鎖定模式、已解除鎖定的一般模式或試用模式。

## <a name="syntax"></a>語法


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lockdownMode* \[擴展\]
</dt> <dd>

成功時，會傳回 [**PWLDP 的 \_ WINDOWS \_ 鎖定 \_ 模式**](wldp-windows-lockdown-mode.md)，指出目前 Windows 10 裝置的安全模式。

</dd> </dl>

## <a name="return-value"></a>傳回值

**如果成功，則 \_ 此** 方法會傳回，否則會傳回失敗碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1803版桌面應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wldp。h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




