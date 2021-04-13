---
description: WMI 具有可讓您讀取和操作安全描述項的物件和方法，以決定誰可以存取安全物件。
ms.assetid: ce4b7c9e-2c16-40d4-8839-76e69ddb2d8c
ms.tgt_platform: multiple
title: WMI 安全描述項物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc315e955c2d449d0dea0db97684cc352257cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568476"
---
# <a name="wmi-security-descriptor-objects"></a>WMI 安全描述項物件

WMI 具有可讓您讀取和操作安全描述項的物件和方法，以決定誰可以存取安全物件。

-   [安全描述項的角色](#the-role-of-security-descriptors)
-   [存取控制和 WMI 安全性物件](#access-control-and-wmi-security-objects)
-   [Win32 \_ SecurityDescriptor 物件](/windows)
-   [DACL 和 SACL](#dacl-and-sacl)
-   [Win32 \_ ACE，win32 \_ 信任者，win32 \_ SID](/windows)
-   [範例：檢查誰有印表機的存取權](#example-checking-who-has-access-to-printers)
-   [相關主題](#related-topics)

## <a name="the-role-of-security-descriptors"></a>安全描述項的角色

安全描述項會定義安全物件的安全性屬性，例如檔案、登錄機碼、WMI 命名空間、印表機、服務或共用。 安全描述項包含物件的擁有者和主要群組的相關資訊。 提供者可以比較資源安全描述項與提出要求之使用者的身分識別，並判斷使用者是否有許可權存取使用者要求的資源。 如需詳細資訊，請參閱 [存取 WMI 安全物件](access-to-wmi-securable-objects.md)。

某些 WMI 方法（例如 [**GetSD**](--systemsecurity-getsd.md)）會以二進位位元組陣列格式傳回安全描述項。 從 Windows Vista 開始，使用 [**win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) 類別的方法，將二進位安全描述項轉換成 [**win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)的實例，這樣可以更輕鬆地操作。 如需詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。

## <a name="access-control-and-wmi-security-objects"></a>存取控制和 WMI 安全性物件

以下是 WMI 安全性物件的清單：

-   [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
-   [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
-   [**Win32 \_ 信任者**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
-   [**Win32 \_ SID**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)

下圖顯示 WMI 安全性物件之間的關聯性。

![wmi 安全性物件之間的關聯性](images/security-descriptor.png)

如需有關存取安全性角色的詳細資訊，請參閱 [安全性最佳作法](/windows/desktop/SecBP/best-practices-for-the-security-apis)、 [維護 WMI 安全性](maintaining-wmi-security.md)和 [存取控制](/windows/desktop/SecAuthZ/access-control)。

## <a name="win32_securitydescriptor-object"></a>Win32 \_ SecurityDescriptor 物件

下表列出 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別屬性。



| 屬性         | 描述                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ControlFlags** | 限定 SD 或其個別成員意義的控制位集。 如需設定 **ControlFlags** 位值的詳細資訊，請參閱 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)。<br/>                                                                                                                                                                      |
| **Dacl**         | [任意存取控制清單 (](/windows/desktop/SecAuthZ/access-control-lists) 使用者和群組的 ACL) ，以及其對受保護物件的存取權限。 這個屬性包含 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 實例的陣列，代表 [存取控制專案](/windows/desktop/SecAuthZ/access-control-entries)。 如需詳細資訊，請參閱 [建立 DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis)。<br/> |
| **群組**        | 此受保護物件所屬的群組。 這個屬性包含 [**Win32 \_ 信任者**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) 的實例，其中包含擁有者所屬群組的名稱、網域及安全識別碼 (SID) 。<br/>                                                                                                                                                             |
| **擁有者**        | 此受保護物件的擁有者。 此屬性包含 [Win32 \_ 信任者](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) 的實例，其中包含擁有者 (SID) 的名稱、網域及安全識別碼。<br/>                                                                                                                                                                                                          |
| **SACL**         | [系統存取控制清單 (ACL)](/windows/desktop/SecAuthZ/access-control-lists) 包含 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 實例陣列，代表為使用者或群組產生審核記錄的存取嘗試類型。 如需詳細資訊，請參閱 [SACL 的新物件](/windows/desktop/SecAuthZ/sacl-for-a-new-object)。<br/>                                                                        |



 

## <a name="dacl-and-sacl"></a>DACL 和 SACL

任意存取控制清單中的 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 物件陣列 (DACL) 和系統存取控制清單 {SACL) 建立使用者或群組之間的連結，以及其存取權限。

當 DACL 屬性未包含 (ACE) 的存取控制專案時，不會授與存取權限，且拒絕存取物件。

> [!Note]  
> **Null** DACL 可提供所有人的完整存取權，這是嚴重的安全性風險。 如需詳細資訊，請參閱 [建立 DACL](/windows/desktop/SecBP/creating-a-dacl)。

 

## <a name="win32_ace-win32_trustee-win32_sid"></a>Win32 \_ ACE，win32 \_ 信任者，win32 \_ SID

[**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)物件包含識別使用者或群組的 [**win32 \_ 受信任**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)類別的實例，而 **AccessMask** 屬性則是位元遮罩，可指定使用者或群組可以採取的動作。 例如，使用者或群組可能會被授與讀取檔案的許可權，但無法寫入檔案。 **Win32 \_ ACE** 物件也包含 ACE，指出它是允許或拒絕存取。

> [!Note]  
> DACL 中的 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 順序很重要，因為 dacl 中允許 (ACE) 允許和拒絕存取控制專案。 如需詳細資訊，請參閱 [DACL 中的 Ace 順序](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)。

 

由 [**Win32 \_ 信任者**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) 表示的每個使用者帳戶或群組都有安全識別碼 (SID) ，可唯一識別帳戶，並指定帳戶的存取權限。 您指定 SID 資料的方式取決於作業系統。 如需詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。

下圖顯示一個 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 實例的內容。

![一個 win32 \- ace 實例的內容](images/win32-ace.png)

## <a name="example-checking-who-has-access-to-printers"></a>範例：檢查誰有印表機的存取權

下列 VBScript 程式碼範例顯示如何使用印表機安全描述項。 腳本會在 [**Win32 \_ 印表機**](/windows/desktop/CIMWin32Prov/win32-printer)類別中呼叫 [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer)方法，以取得描述項，然後判斷安全描述項中是否有任意的存取控制清單 (DACL) 存在。 如果有 DACL，則腳本會從 DACL 取得 (ACE) 存取控制專案的清單。 每個 ACE 都是由 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)的實例表示。 腳本會檢查每個 ACE 來取得使用者的名稱，並判斷使用者是否具有印表機的存取權。 使用者會以內嵌在 **win32 \_ ACE** 實例中的 [**win32 \_ 受信任**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)實例來表示。


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        colACEs = objSD.DACL
    For Each objACE in colACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)
</dt> <dt>

[安全描述項協助程式類別](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[安全性最佳作法](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[維護 WMI 安全性](maintaining-wmi-security.md)
</dt> <dt>

[存取控制](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[存取 WMI 命名空間](access-to-wmi-namespaces.md)
</dt> </dl>

 

