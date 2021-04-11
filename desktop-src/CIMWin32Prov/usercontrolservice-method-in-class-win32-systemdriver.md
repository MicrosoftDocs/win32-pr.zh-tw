---
description: 嘗試傳送使用者定義的控制項程式碼至系統驅動程式所管理的服務。
ms.assetid: 62e66c35-f264-43d0-9e94-fb5e85f936e0
ms.tgt_platform: multiple
title: Win32_SystemDriver 類別的 UserControlService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99974206f6487d90e1660f5a64c1d00904912c66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936457"
---
# <a name="usercontrolservice-method-of-the-win32_systemdriver-class"></a>Win32 >systemdriver 類別的 UserControlService 方法 \_

**UserControlService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會嘗試將使用者定義的控制項程式碼傳送至系統驅動程式所管理的服務。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ControlCode* \[在\]
</dt> <dd>

指定從128到 255) 的定義值，這些 (值會提供使用者特定的控制項命令。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果已接受 **UserControlService** 要求，則傳回 0 (零) 的值，如果要求不受支援則為 1 (一個) ，以及表示錯誤的其他任何數位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ >systemdriver**](win32-systemdriver.md)
</dt> </dl>

 

