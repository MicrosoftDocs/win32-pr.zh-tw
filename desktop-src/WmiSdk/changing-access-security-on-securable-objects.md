---
description: 從 Windows Vista 開始，許多安全物件都有取得或設定安全描述項的方法。 使用適當的許可權，您可以讀取或變更安全物件的安全描述項。
ms.assetid: da660e7e-f32d-4b7d-b979-f7b482a73fa2
ms.tgt_platform: multiple
title: 變更安全物件的存取安全性
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4cdaa948e6f0e695b3e77576b0a0726f0b38f3b649f005b42aa8e205c894db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050986"
---
# <a name="changing-access-security-on-securable-objects"></a>變更安全物件的存取安全性

印表機、服務、登錄機碼、DCOM 應用程式和 WMI 命名空間都是安全物件。 安全物件的存取會受到 [*安全描述項*](/windows/desktop/SecGloss/s-gly)的保護，以指定具有存取權的使用者。 從 Windows Vista 開始，許多安全物件都有取得或設定安全描述項的方法。 使用適當的許可權，您可以讀取或變更安全物件的安全描述項。 您可以使用這些方法來控制哪些使用者帳戶或群組可以存取印表機、服務、WMI 命名空間或其他物件。 如需有關安全描述項及其在 WMI 中使用方式的詳細資訊，請參閱 [Wmi 安全物件的存取](access-to-wmi-securable-objects.md)。

本主題將討論下列各節：

-   [物件和安全描述項方法](#objects-and-security-descriptor-methods)
-   [在安全描述項格式之間轉換](#converting-between-security-descriptor-formats)
-   [安全性問題](#security-issues)
-   [相關主題](#related-topics)

## <a name="objects-and-security-descriptor-methods"></a>物件和安全描述項方法

下列清單包含安全物件必須讓您讀取或變更安全描述項的方法：

-   WMI 命名空間

    提供者可以建立只允許某些群組存取 WMI 命名空間中資料的安全性。 命名空間安全性是由 [**\_ \_ SystemSecurity**](--systemsecurity.md)類別上的方法所控制。 從 Windows Vista 開始， [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)和 [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)方法會傳回並寫入 [**\_ \_ SecurityDescriptor**](--securitydescriptor.md)物件。 如需詳細資訊，請參閱 [設定命名空間安全描述項](setting-namespace-security-descriptors.md)。

-   登錄機碼

    從 Windows Vista 開始，您可以保護登錄機碼，使其無法被未經授權的使用者變更。 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)類別具有 [**GetSecurityDescriptor**](/previous-versions/windows/desktop/regprov/getsecuritydescriptor-method-in-class-stdregprov)和 [**SetSecurityDescriptor**](/previous-versions/windows/desktop/regprov/setsecuritydescriptor-method-in-class-stdregprov)方法。 這些方法會傳回和寫入 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 物件。

-   印表機

    從 Windows Vista 開始，您可以使用 [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer)和 [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer)方法來保護 [**Win32 \_ 印表機**](/windows/desktop/CIMWin32Prov/win32-printer)類別實例的存取。 這些方法會傳回和寫入 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 物件。

-   服務

    從 Windows Vista 開始，您可以使用 [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service)和 [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service)方法來保護 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)類別實例的存取。 這些方法會傳回和寫入 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 物件。

-   DCOM 應用程式

    DCOM 應用程式實例有數個安全描述項。 從 Windows Vista 開始，使用 [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)類別的方法來取得或變更不同的安全描述項。 系統會以 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別的實例傳回安全描述項。

    若要取得或變更設定許可權，請呼叫 [**GetConfigurationSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) 或 [**SetConfigurationSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) 方法。

    若要取得或變更存取權限，請呼叫 [**GetAccessSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) 或 [**SetAccessSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) 方法。

    若要取得或變更啟動和啟用許可權，請呼叫 [**GetLaunchSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting) 或 [**SetLaunchSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) 方法。

-   檔案

    [**GetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting)和 [**SetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting)方法位於 [**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)類別中，而不是在 [**CIM \_ 資料檔案**](/windows/desktop/CIMWin32Prov/cim-datafile)類別中。

-   共用

    [**GetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting)和 [**SetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting)方法位於 [**win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting)類別中，而不是 [**win32 \_ Share**](/windows/desktop/CIMWin32Prov/win32-share)類別中。

> [!Note]  
> 如果未在 **SetSecurityDescriptor** 方法的呼叫中指定新的 [*安全性存取控制清單 (SACL)*](/windows/desktop/SecGloss/s-gly) ，則目標安全物件上的安全描述項 SACL 會設定為 **Null** ，因此不會保存先前的 SACL 設定。

 

## <a name="converting-between-security-descriptor-formats"></a>在安全描述項格式之間轉換

安全描述項是複雜的二進位位元組陣列，通常必須在 c + + 中建立和變更。 使用其中一個 Get 方法取得安全描述項之後， [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) 類別會提供方法，將安全描述項轉換成 [安全描述項定義語言 (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) 或 [**win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 實例。

您可以更輕鬆地在 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 實例或 SDDL 中操作 (ACL) 的存取控制清單。 如需有關 WMI 中安全描述項的結構和使用方式的詳細資訊，請參閱 [Wmi 安全描述項物件](wmi-security-descriptor-objects.md)。

在 c + + 或 c # 中，使用轉換函式將二進位安全描述項轉換成 [安全描述項定義語言 (SDDL) ](/windows/desktop/SecAuthZ/security-descriptor-definition-language)。 若要在 c + + 應用程式中修改安全描述項值，請使用 [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) 和 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)。

## <a name="security-issues"></a>安全性問題

建議您務必小心完成安全描述項的變更，讓物件的安全性不會受到危害。 請注意，存取控制專案的順序 (Ace) 在任意存取控制清單 (DACL) 可能會影響存取安全性。 如需詳細資訊，請參閱 [DACL 中的 Ace 順序](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 安全描述項物件](wmi-security-descriptor-objects.md)
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

 

 
