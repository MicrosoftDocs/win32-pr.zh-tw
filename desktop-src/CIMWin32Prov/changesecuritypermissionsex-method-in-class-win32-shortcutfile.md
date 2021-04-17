---
description: 變更物件路徑中指定之邏輯快速鍵檔的安全性許可權 (這個方法是) 的 ChangeSecurityPermissions 方法擴充版本。
ms.assetid: 9a5c9fa9-ccd9-4792-969f-28f52ab9bc52
ms.tgt_platform: multiple
title: Win32_ShortcutFile 類別的 ChangeSecurityPermissionsEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 124f8d883b89379e4b36c5dd33b029718fbbd469
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510537"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_shortcutfile-class"></a>Win32 ShortcutFile 類別的 ChangeSecurityPermissionsEx 方法 \_

**ChangeSecurityPermissionsEx** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會變更物件路徑中所指定之邏輯快速鍵檔的安全性許可權， (這個方法是 [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md)方法的擴充版本) 。 如果邏輯檔案是目錄，則這個方法是遞迴的，並且會變更目錄包含的所有檔案和子目錄的安全性許可權。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SecurityDescriptor* \[在\]
</dt> <dd>

解析為 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例的運算式。 此參數包含 [**Win32 \_ 分頁檔**](win32-pagefile.md)實例的新安全性許可權。

</dd> <dt>

*選項* \[在\]
</dt> <dd>

要修改的安全性許可權。 例如，若要變更擁有者和任意存取控制清單 (DACL) 安全性，請使用下列程式：

`Option = 1 + 4`

或

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**變更 \_擁有者 \_ 安全性 \_ 資訊** (1) 


</dt> <dd>

變更邏輯檔案的擁有者。

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**變更 \_將 \_ 安全性 \_ 資訊群組** (2) 


</dt> <dd>

變更邏輯檔案的群組。

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**變更 \_DACL \_ 安全性 \_ 資訊** (4) 


</dt> <dd>

變更邏輯檔案 (DACL) 的任意存取控制清單。

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**變更 \_SACL \_ 安全性 \_ 資訊** (8) 


</dt> <dd>

變更邏輯檔案 (SACL) 的系統存取控制清單。

</dd> </dl> </dd> <dt>

*StopFileName* \[擴展\]
</dt> <dd>

**ChangeSecurityPermissionsEx** 方法失敗之檔案或目錄的名稱。 如果方法成功，則此參數為 **Null** 。

</dd> <dt>

*StartFileName* \[在中，選擇性\]
</dt> <dd>

將子檔案或目錄命名為 **ChangeSecurityPermissionsEx** 的起點。 一般而言， *StartFileName* 參數是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。 如果這個參數是 **Null**，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案或目錄上執行作業。

</dd> <dt>

*遞迴* \[在中，選擇性\]
</dt> <dd>

若 **為 true**，則會將擁有權變更以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。

> [!Note]  
> 若為檔案實例，則會忽略 *遞迴* 參數。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值 0 (零) 如果許可權變更，則傳回不同的數位來表示錯誤。

<dl> <dt>

「成功」
</dt> <dd>

0

要求成功。

</dd> <dt>

**拒絕存取**
</dt> <dd>

2

存取遭到拒絕。

</dd> <dt>

**未指定的失敗**
</dt> <dd>

8

發生未指定的失敗。

</dd> <dt>

**不正確物件**
</dt> <dd>

9

指定的名稱無效。

</dd> <dt>

**物件已存在**
</dt> <dd>

10

指定的物件已存在。

</dd> <dt>

**檔案系統非 NTFS**
</dt> <dd>

11

檔案系統不是 NTFS 檔案系統。

</dd> <dt>

**平臺非 NT/Windows 2000**
</dt> <dd>

12

平臺不是 Windows。

</dd> <dt>

**磁片磁碟機不相同**
</dt> <dd>

13

磁片磁碟機不相同。

</dd> <dt>

**目錄非空白**
</dt> <dd>

14

目錄不是空的。

</dd> <dt>

**共用違規**
</dt> <dd>

15

發生共用違規。

</dd> <dt>

**不正確開機檔案**
</dt> <dd>

16

指定的起始檔無效。

</dd> <dt>

**未保留許可權**
</dt> <dd>

17

不會保留操作所需的許可權。

</dd> <dt>

**參數不正確**
</dt> <dd>

21

指定的參數無效。

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

[**Win32 \_ ShortcutFile**](win32-shortcutfile.md)
</dt> </dl>

 

