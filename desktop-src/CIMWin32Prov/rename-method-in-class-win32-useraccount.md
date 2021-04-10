---
description: 重新命名使用者帳戶名稱。
ms.assetid: 90258256-7470-4ec8-afce-bea0f64b90fb
ms.tgt_platform: multiple
title: Win32_UserAccount 類別的重新命名方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27d495804fb68bc74eda269c2dd7921540f05f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111248"
---
# <a name="rename-method-of-the-win32_useraccount-class"></a>Win32 UserAccount 類別的重新命名方法 \_

**重新命名** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會重新命名使用者帳戶名稱。

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

新的帳戶名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

「成功」
</dt> <dd>

0

成功。

</dd> <dt>

**找不到實例**
</dt> <dd>

1

找不到實例。

</dd> <dt>

**需要的實例**
</dt> <dd>

2

需要實例。

</dd> <dt>

**參數不正確**
</dt> <dd>

3

無效的參數。

</dd> <dt>

**找不到使用者**
</dt> <dd>

4

找不到使用者。

</dd> <dt>

**找不到網域**
</dt> <dd>

5

找不到網域。

</dd> <dt>

**只允許在網域的主域控制站上執行操作**
</dt> <dd>

6

只允許在網域的主域控制站上執行操作。

</dd> <dt>

**最後一個系統管理帳戶上不允許操作。**
</dt> <dd>

7

</dd> <dt>

**在指定的特殊群組上不允許操作;user、admin、local 或 guest。**
</dt> <dd>

8

在指定的特殊群組上不允許操作： user、admin、local 或 guest。

</dd> <dt>

**其他 API 錯誤**
</dt> <dd>

9

其他 API 錯誤。

</dd> <dt>

**內部錯誤**
</dt> <dd>

10

內部錯誤。

</dd> </dl>

## <a name="remarks"></a>備註

這項功能會實作為一種方法，為新名稱提供不同的內容，而此名稱與要修改之實例相關聯之名稱的索引鍵屬性值可區別。

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

[**Win32 \_ UserAccount**](win32-useraccount.md)
</dt> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

