---
description: Win32_Service 類別的 delete 方法 (CIMWin32 WMI 提供者) -Delete&\# 8194;WMI 類別方法會刪除現有的服務。
ms.assetid: aa4e7630-3b19-47dd-acd1-4d1735acb819
ms.tgt_platform: multiple
title: " (CIMWin32 WMI 提供者來刪除 Win32_Service 類別的方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4031184e23e99fc54237ed0b0b4196fe6c075c5b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089576"
---
# <a name="delete-method-of-the-win32_service-class-cimwin32-wmi-providers"></a> (CIMWin32 WMI 提供者來刪除 Win32_Service 類別的方法) 

**Delete** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會刪除現有的服務。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Delete();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**0**
</dt> <dd>

要求已被接受。

</dd> <dt>

**1**
</dt> <dd>

不支援此要求。

</dd> <dt>

**2**
</dt> <dd>

使用者沒有必要的存取權。

</dd> <dt>

**3**
</dt> <dd>

無法停止此服務，因為與它相依的其他服務正在執行中。

</dd> <dt>

**4**
</dt> <dd>

要求的控制碼無效，或是服務不接受此控制碼。

</dd> <dt>

**5**
</dt> <dd>

因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。

</dd> <dt>

**6**
</dt> <dd>

尚未啟動服務。

</dd> <dt>

**7**
</dt> <dd>

服務並未及時回應啟動要求。

</dd> <dt>

**8**
</dt> <dd>

啟動服務時發生未知的錯誤。

</dd> <dt>

**9**
</dt> <dd>

找不到服務可執行檔的目錄路徑。

</dd> <dt>

**10**
</dt> <dd>

服務已在執行中。

</dd> <dt>

**11**
</dt> <dd>

要加入新服務的資料庫已被鎖定。

</dd> <dt>

**12**
</dt> <dd>

這項服務所依賴的相依性已從系統中移除。

</dd> <dt>

**13**
</dt> <dd>

服務在相依的服務中找不到所需的服務。

</dd> <dt>

**14**
</dt> <dd>

已經從系統中停用服務。

</dd> <dt>

**15**
</dt> <dd>

此服務未通過驗證，無法在系統上執行。

</dd> <dt>

**16**
</dt> <dd>

這項服務正在從系統中移除。

</dd> <dt>

**17**
</dt> <dd>

服務沒有執行執行緒。

</dd> <dt>

**達**
</dt> <dd>

服務會在啟動時有迴圈相依性。

</dd> <dt>

**診斷**
</dt> <dd>

服務正在相同名稱下執行。

</dd> <dt>

**20**
</dt> <dd>

服務名稱包含不正確字元。

</dd> <dt>

**21**
</dt> <dd>

傳遞給服務的參數無效。

</dd> <dt>

**22**
</dt> <dd>

用來執行此服務的帳戶無效，或缺少執行服務的許可權。

</dd> <dt>

**23**
</dt> <dd>

服務存在於系統可使用之服務的資料庫中。

</dd> <dt>

**24**
</dt> <dd>

服務目前在系統中暫停。

</dd> </dl>

## <a name="remarks"></a>備註

當您的組織變更時，您可能會決定從特定電腦移除特定的服務。 您可以使用 WMI 來移除內部和協力廠商服務，也可以使用 Sysocmgr.exe 來移除作業系統服務。

準備移除服務時，請記住下列資訊：

-   您必須先停止服務，才能將其移除。 當您發出 delete 命令時，如果服務正在執行，則會將服務標示為要刪除，但它會繼續執行，直到停止並關閉所有開啟的控制碼為止。

    如果服務永遠不會停止，則永遠不會刪除該服務。

-   移除服務並不會移除服務的可執行檔。

    使用 WMI 移除服務會刪除 HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Services 下的相關登錄專案。 如此一來，就不會再安裝服務，也無法透過 [服務] 嵌入式管理單元使用。 不過，WMI 不會刪除可執行檔，這表示您可以輕鬆地重新安裝服務。 若要刪除可執行檔，您必須先取出路徑名稱，然後再刪除該檔案。

-   移除基底 Windows 2000 服務 (例如，使用 WMI 的 DHCP) 會刪除該服務的登錄專案，但不會從 [系統管理工具] 功能表移除快捷方式，或從 Windows 元件嚮導移除此服務。 這可能會讓任何嘗試判斷電腦設定方式的人混淆。

    例如，如果您使用 WMI 腳本移除 DHCP 服務，[服務] 嵌入式管理單元中將不再列出 DHCP 服務。 不過，DHCP 主控台的 nonfunctioning 快捷方式仍會保留在 [系統管理工具] 功能表中，如果您啟動 [Windows 元件嚮導]，則表示已安裝 DHCP 服務。

    因此，您應該一律使用 Sysocmgr.exe 以程式設計方式移除 Windows 2000 服務。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例說明如何刪除服務。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colListOfServices = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE Name = 'DbService'")
For Each objService in colListOfServices
 objService.StopService()
 objService.Delete()
Next
```



下列 Perl 程式碼範例說明如何刪除服務。


```
use strict;
use Win32::OLE;

my ($Service, $ServiceSet) ;
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='MyService'");};
unless($@)
{
 foreach $Service (in $ServiceSet)
 {
  my $RetVal = $Service->Delete();
  if ($RetVal == 0)  
  {
   print "Service deleted \n"; 
  }
  else  
  {
   print "Delete failed: %d", $RetVal;
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
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

[**Win32 \_ 服務**](win32-service.md)
</dt> <dt>

[WMI 工作：服務](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

