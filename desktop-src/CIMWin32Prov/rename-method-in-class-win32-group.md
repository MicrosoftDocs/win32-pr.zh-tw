---
description: 允許變更組名。
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Win32_Group 類別的重新命名方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c111a0c12d0fdc1ce3f6d6bcaa0e7b0f57831054
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970705"
---
# <a name="rename-method-of-the-win32_group-class"></a>Win32 群組類別的重新命名方法 \_

**重新命名** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法允許變更組名。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

此類別的 **domain** 屬性所指定之網域上的 Windows 使用者帳戶名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

**重新命名** 方法可以傳回下列清單所列的錯誤碼。 針對未列出的整數值，請參閱 [WMI 傳回 \_ 碼](/windows/desktop/WmiSdk/wmi-return-codes)。

<dl> <dt>

「成功」
</dt> <dd>

0

成功。

</dd> <dt>

**找不到實例**
</dt> <dd>

1

</dd> <dt>

**需要的實例**
</dt> <dd>

2

</dd> <dt>

**參數不正確**
</dt> <dd>

3

</dd> <dt>

**找不到群組**
</dt> <dd>

4

</dd> <dt>

**找不到網域**
</dt> <dd>

5

</dd> <dt>

**只允許在網域的主域控制站上執行操作**
</dt> <dd>

6

</dd> <dt>

**在指定的特殊群組上不允許操作;user、admin、local 或 guest。**
</dt> <dd>

7

</dd> <dt>

**其他 API 錯誤**
</dt> <dd>

8

</dd> <dt>

**內部錯誤**
</dt> <dd>

9

</dd> </dl>

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

[**Win32 \_ 群組**](win32-group.md)
</dt> <dt>

[**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

