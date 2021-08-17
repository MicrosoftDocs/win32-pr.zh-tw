---
description: 在磁片上叫用 chkdsk 操作。
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: Win32_LogicalDisk 類別的 Chkdsk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.Chkdsk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 24d7052cd7d36da8a9464cbbef142904a70f83767872dadf25fda2033fa66fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959107"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a>Win32 LogicalDisk 類別的 Chkdsk 方法 \_

**Chkdsk** 實例方法會叫用磁片上的 **chkdsk** 操作。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Chkdsk(
  [in] boolean FixErrors = ,
  [in] boolean VigorousIndexCheck = ,
  [in] boolean SkipFolderCycle = ,
  [in] boolean ForceDismount = ,
  [in] boolean RecoverBadSectors = ,
  [in] boolean OKToRunAtBootUp = 
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FixErrors* \[在\]
</dt> <dd>

指出在磁片上找到的錯誤應完成的工作。 若 **為 true**，則會修正錯誤。 預設值為 **false**。

</dd> <dt>

*VigorousIndexCheck* \[在\]
</dt> <dd>

若 **為 true**，則應該執行較不加強的索引項目檢查。 預設值為 **false**。

</dd> <dt>

*SkipFolderCycle* \[在\]
</dt> <dd>

若 **為 true**，則應略過資料夾迴圈檢查。 預設值為 **True**。

</dd> <dt>

*ForceDismount* \[在\]
</dt> <dd>

若 **為 true**，則應該在檢查之前強制卸載磁片磁碟機。 預設值為 **false**。

</dd> <dt>

*RecoverBadSectors* \[在\]
</dt> <dd>

若 **為 true**，則應該找出不正確的磁區，而且應該從這些磁區復原可讀取的資訊。 預設值為 **false**。

</dd> <dt>

*OKToRunAtBootUp* \[在\]
</dt> <dd>

若 **為 true**，則會在下次開機時執行 **chkdsk** 作業，以防無法執行作業，因為在呼叫這個方法時，磁片會被鎖定。 預設值為 **false**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 0 (零) 的值。 其他值會列在下列清單中。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功-Chkdsk 已完成**
</dt> <dd>

0

成功- [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) 已完成

</dd> <dt>

**在重新開機時成功鎖定和 chkdsk 排程**
</dt> <dd>

1

</dd> <dt>

**失敗-未知的檔案系統**
</dt> <dd>

2

</dd> <dt>

**失敗-未知的錯誤**
</dt> <dd>

3

</dd> <dt>

**失敗-不支援的檔案系統**
</dt> <dd>

4

</dd> </dl>

## <a name="remarks"></a>備註

此方法僅適用于代表電腦中實體磁片的邏輯磁片實例。 它不適用於對應的邏輯磁碟機。

## <a name="examples"></a>範例

如果設定了 chkdsk/f 旗標，伺服器 PowerShell 程式碼範例會檢查遠端系統，並傳回 true 或 false，以在伺服器 PowerShell 程式碼範例[上設定 chkdsk 中途位](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) 。

[遠端掃描磁片](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267)PowerShell 程式碼範例會從遠端啟動或排程掃描磁片。

下列 VBScript 程式碼範例會針對電腦上的 D 磁片磁碟機執行 ChkDsk.exe。


```VB
Const FIX_ERRORS = True 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk.DeviceID='D:'") 
 
errReturn = objDisk.ChkDsk(FIX_ERRORS) 
```



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

[**Win32 \_ LogicalDisk**](win32-logicaldisk.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

