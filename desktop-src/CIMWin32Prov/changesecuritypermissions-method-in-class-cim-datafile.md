---
description: 變更物件路徑中所指定之邏輯資料檔案的安全性許可權。
ms.assetid: b0a66411-f973-42ce-a3fe-25c31234a964
ms.tgt_platform: multiple
title: CIM_DataFile 類別的 ChangeSecurityPermissions 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faa2e3ce2f2454d76ff9e55cc10cf09e9b5f715e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111005"
---
# <a name="changesecuritypermissions-method-of-the-cim_datafile-class"></a>CIM \_ 資料檔案類別的 ChangeSecurityPermissions 方法

**ChangeSecurityPermissions** 方法會變更物件路徑中所指定之邏輯資料檔案的安全性許可權。 如果邏輯檔案是目錄，則此方法會以遞迴方式運作，以變更目錄所包含的所有檔案和子目錄的安全性許可權。 這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SecurityDescriptor* \[在\]
</dt> <dd>

指定安全性資訊。

> [!Note]  
> 在 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)結構中 (ACL) 的 **Null** 存取控制清單會授與無限制的存取權。 如需無限制存取之含意的詳細資訊，請參閱 [建立新物件的安全描述項](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)。

 

</dd> <dt>

*選項* \[在\]
</dt> <dd>

要修改的安全性許可權。 例如，若要變更擁有者和 DACL 安全性，請使用：

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

變更邏輯檔案的 ACL。

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**變更 \_SACL \_ 安全性 \_ 資訊** (8) 


</dt> <dd>

變更邏輯檔案的系統 ACL。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

在成功時傳回0的值，並傳回任何其他數位以表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

「成功」
</dt> <dd>

0

成功。

</dd> <dt>

**拒絕存取**
</dt> <dd>

2

拒絕存取。

</dd> <dt>

**未指定的失敗**
</dt> <dd>

8

未指定的失敗。

</dd> <dt>

**不正確物件**
</dt> <dd>

9

不正確物件。

</dd> <dt>

**物件已存在**
</dt> <dd>

10

物件已存在。

</dd> <dt>

**檔案系統非 NTFS**
</dt> <dd>

11

</dd> <dt>

**平臺非 NT/Windows 2000**
</dt> <dd>

12

平臺不是以 Windows NT 為基礎。

</dd> <dt>

**磁片磁碟機不相同**
</dt> <dd>

13

磁片磁碟機不相同。

</dd> <dt>

**目錄非空白**
</dt> <dd>

14

目錄未清空。

</dd> <dt>

**共用違規**
</dt> <dd>

15

共用違規。

</dd> <dt>

**不正確開機檔案**
</dt> <dd>

16

不正確啟動檔案。

</dd> <dt>

**未保留許可權**
</dt> <dd>

17

未保留許可權。

</dd> <dt>

**參數不正確**
</dt> <dd>

21

無效的參數。

</dd> </dl>

## <a name="remarks"></a>備註

[**CIM \_ 資料檔案**](cim-datafile.md)中的 **CHANGESECURITYPERMISSIONS** 方法是由 WMI 所執行。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

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

[**CIM \_ 資料檔案**](changesecuritypermissions-method-in-class-cim-datafile.md)
</dt> <dt>

[**CIM \_ 資料檔案**](cim-datafile.md)
</dt> <dt>

[WMI 工作：檔案和資料夾](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**檔案和目錄存取權限常數**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

