---
description: 起始伺服器資源的共用。
ms.assetid: 36530e1b-9109-4a6c-bba9-d9358101f5e2
ms.tgt_platform: multiple
title: Win32_Share 類別的 Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7a74838d9f6c532d3433240a5b8a70846b63776
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936531"
---
# <a name="create-method-of-the-win32_share-class"></a>Win32 共用類別的 Create 方法 \_

**建立**[WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會起始伺服器資源的共用。   

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*路徑* \[在\]
</dt> <dd>

Windows 共用的本機路徑。

範例： "C： \\ Program Files"。

</dd> <dt>

*名稱* \[在\]
</dt> <dd>

將別名傳遞到在執行 Windows 的電腦系統上設定為共用的路徑。

範例： "public"。

</dd> <dt>

*類型* \[在\]
</dt> <dd>

傳遞要共用的資源類型。 類型包括磁片磁碟機、列印佇列、處理序間通訊 (IPC) 和一般裝置。 可以是下列其中一個值。

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**磁片磁碟機** (0) 


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

**列印佇列** (1) 


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

**裝置** (2) 


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (3) 


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

**磁片磁碟機系統管理員** (2147483648) 


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**列印佇列管理** (2147483649) 


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**裝置系統管理員** (2147483650) 


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

**IPC 系統管理員** (2147483651) 


</dt> <dd></dd> </dl> </dd> <dt>

*MaximumAllowed* \[在中，選擇性\]
</dt> <dd>

允許同時使用此資源的使用者數目上限。

範例：10。 這是選擇性參數。

</dd> <dt>

*描述* \[在中，選擇性\]
</dt> <dd>

描述所共用資源的選擇性批註。 這是選擇性參數。

</dd> <dt>

*密碼* \[在中，選擇性\]
</dt> <dd>

使用共用資源的共用層級安全性) 執行伺服器時的密碼 (。 如果伺服器正在以使用者層級安全性執行，則會忽略此參數。 這是選擇性參數。

</dd> <dt>

*存取* \[在中，選擇性\]
</dt> <dd>

使用者層級許可權的安全描述項。 安全描述項包含資源的許可權、擁有者和存取功能的相關資訊。 如果未提供此參數或為 **Null**，則每個人都具有共用的讀取權限。 如需詳細資訊，請參閱 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 和 [變更安全物件的存取安全性](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功** (0) 
</dt> <dt>

**拒絕存取** (2) 
</dt> <dt>

**未知的失敗** (8) 
</dt> <dt>

**不正確名稱** (9) 
</dt> <dt>

**層級** (10) 無效
</dt> <dt>

**不正確參數** (21) 
</dt> <dt>

**重複的共用** (22) 
</dt> <dt>

重新 **導向路徑** (23) 
</dt> <dt>

**未知的裝置或目錄** (24) 
</dt> <dt>

**找不到網路名稱** (25) 
</dt> <dt>

**其他** (26 4294967295) 
</dt> </dl>

## <a name="remarks"></a>備註

**Create** 是靜態方法。

只有 Administrators 或 Account Operators 本機群組的成員，或是具有通訊、列印或伺服器操作員群組成員資格的成員，才能夠成功執行 **Create**。 列印操作員只能新增印表機佇列。 通訊運算子只能新增通訊裝置佇列。

## <a name="examples"></a>範例

[匯出和匯入檔案共用](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1)PowerShell 範例會匯出並匯入檔案共用，並設定共用許可權。 同樣地，[ [建立共用和設定許可權](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) ] 範例也會建立新的共用，並設定共用許可權。

下列 PowerShell 程式碼會建立共用。


```PowerShell
# create pointer to class
$comp=[WMICLASS]"Win32_share"

# create a new share
$comp.create("c:\","mynewshare",0)

# see results
gwmi win32_share 
```



上述程式碼範例會傳回下列內容：

``` syntax
__GENUS          : 2
__CLASS          : __PARAMETERS
__SUPERCLASS     : 
__DYNASTY        : __PARAMETERS
__RELPATH        : 
__PROPERTY_COUNT : 1
__DERIVATION     : {}
__SERVER         : 
__NAMESPACE      : 
__PATH           : 
ReturnValue      : 2
PSComputerName   : 

Name        : ADMIN$
Path        : C:\Windows
Description : Remote Admin

Name        : C$
Path        : C:\
Description : Default share

Name        : CCMLOGS$
Path        : C:\Windows\CCM\Logs
Description : Public Share

Name        : ccmsetup$
Path        : C:\Windows\ccmsetup
Description : Public Share

Name        : Drop
Path        : C:\Drop
Description : 

Name        : IPC$
Path        : 
Description : Remote IPC

Name        : Share
Path        : C:\Share
Description : 
```

下列 C 程式 \# 代碼範例說明如何呼叫 create 方法。


```CSharp
private static void makeShare(string servername, string filepath, string sharename)
{
try
 {
 // assemble the string so the scope represents the remote server
 string scope = string.Format("\\\\{0}\\root\\cimv2", servername);

 // connect to WMI on the remote server
 ManagementScope ms = new ManagementScope(scope);

 // create a new instance of the Win32_Share WMI object
 ManagementClass cls = new ManagementClass("Win32_Share");

 // set the scope of the new instance to that created above
 cls.Scope = ms;

 // assemble the arguments to be passed to the Create method
 object[] methodargs = { filepath, sharename, "0" };

 // invoke the Create method to create the share
 object result = cls.InvokeMethod("Create", methodargs);
 }
catch (SystemException e)
 {
  Console.WriteLine("Error attempting to create share {0}:", sharename);
  Console.WriteLine(e.Message);
 }

}
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

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ 共用**](win32-share.md)
</dt> </dl>

 

