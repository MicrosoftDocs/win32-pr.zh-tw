---
description: 變更物件路徑中指定之裝置檔案的安全性許可權 (這個方法是) 的延伸版本 ChangeSecurityPermissions 方法。
ms.assetid: 5ad54470-6961-4c0d-9d2a-d3eaf81d75f4
ms.tgt_platform: multiple
title: CIM_DeviceFile 類別的 ChangeSecurityPermissionsEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c6d70c11077873154040e30cabfb460546f79b1088ff124884e35f3698aaf78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959137"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_devicefile-class"></a>CIM DeviceFile 類別的 ChangeSecurityPermissionsEx 方法 \_

**ChangeSecurityPermissionsEx** 方法會變更物件路徑中所指定之裝置檔案的安全性許可權， (這個方法是 [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md)方法的擴充版本) 。 如果邏輯檔案是目錄，則此方法會以遞迴方式運作，變更目錄所包含的所有檔案和子目錄的安全性許可權。 這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

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

指定安全性資訊。

> [!Caution]  
> [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)結構中的 **Null** ACL 會授與無限制的存取權。

 

</dd> <dt>

*選項* \[在\]
</dt> <dd>

要修改的安全性許可權。 例如，若要變更擁有者和 DACL 安全性，請使用

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

</dd> </dl> </dd> <dt>

*StopFileName* \[擴展\]
</dt> <dd>

字串，代表方法失敗 (或目錄) 的名稱。 如果方法成功，則此參數為 **null** 。

</dd> <dt>

*StartFileName* \[在中，選擇性\]
</dt> <dd>

要做為這個方法起點的子檔 (或目錄) 。 一般而言， *StartFileName* 參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。 如果這個參數是 **null**，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案 (或目錄) 上執行作業。

</dd> <dt>

*遞迴* \[在中，選擇性\]
</dt> <dd>

若 **為 TRUE**，則此方法也會以遞迴方式套用至 [**CIM \_ DeviceFile**](cim-devicefile.md) 實例所指定之目錄中的檔案和目錄。 若為檔案實例，則會忽略這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。

<dl> <dt>


</dt> <dd>

0

成功。

</dd> <dt>


</dt> <dd>

2

拒絕存取。

</dd> <dt>


</dt> <dd>

8

未指定的失敗。

</dd> <dt>


</dt> <dd>

9

不正確物件。

</dd> <dt>


</dt> <dd>

10

物件已存在。

</dd> <dt>


</dt> <dd>

11

檔案系統不是 NTFS。

</dd> <dt>


</dt> <dd>

12

平臺未 Windows。

</dd> <dt>


</dt> <dd>

13

磁片磁碟機不相同。

</dd> <dt>


</dt> <dd>

14

目錄未清空。

</dd> <dt>


</dt> <dd>

15

共用違規。

</dd> <dt>


</dt> <dd>

16

不正確啟動檔案。

</dd> <dt>


</dt> <dd>

17

未保留許可權。

</dd> <dt>


</dt> <dd>

21

無效的參數。

</dd> </dl>

## <a name="remarks"></a>備註

這個方法目前不是由 WMI 所執行。 若要使用這個方法，您必須在自己的提供者中加以執行。

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

[CIM \_ DeviceFile](changesecuritypermissionsex-method-in-class-cim-devicefile.md)
</dt> <dt>

[**CIM \_ DeviceFile**](cim-devicefile.md)
</dt> </dl>

 

