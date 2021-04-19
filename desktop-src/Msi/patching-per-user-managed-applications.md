---
description: 從 Windows Installer 3.0 開始，可以將修補程式套用至應用程式，該應用程式在修補程式註冊為具有更高的許可權之後，已安裝在個別使用者管理的內容中。
ms.assetid: ebe5f447-9b74-48dc-8192-f2ac90dca490
title: 修補 Per-User 受控應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa6a19933e5c8ab409d510d980b8ed634a630e1
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106991399"
---
# <a name="patching-per-user-managed-applications"></a>修補 Per-User 受控應用程式

從 Windows Installer 3.0 開始，可以將修補程式套用至應用程式，該應用程式在修補程式註冊為具有更高的許可權之後，已安裝在個別使用者管理的內容中。

**Windows Installer 2.0：** 不支援。 您無法使用早于 Windows Installer 3.0 的 Windows Installer 版本，將修補程式套用到每個使用者管理內容中所安裝的應用程式。

在下列情況下，會以每個使用者管理的狀態安裝應用程式。

-   應用程式的每個使用者安裝是使用部署和 [群組原則](/previous-versions/windows/desktop/Policy/group-policy-start-page)來執行。
-   應用程式已公告至指定的使用者，並由廣告 Per-User 應用程式中所述的方法安裝，並 [以較高的許可權進行安裝](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)。

需要許可權才能在每個使用者管理的內容中安裝應用程式。因此，使用較高的許可權，安裝程式也會執行應用程式的未來 Windows Installer 重新安裝或修復。 這表示只有來自信任來源的修補程式才能套用至應用程式。

從 Windows Installer 3.0 開始，您可以在修補程式註冊為具有更高許可權之後，將修補程式套用至每位使用者的受控應用程式。 若要將修補程式註冊為具有較高的許可權，請使用 [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)函式或 [**Patch**](patch-object.md)物件的 [**SourceListAddSource**](patch-sourcelistaddsource.md)方法（具有更高的許可權）。 註冊修補程式之後，您可以使用 [**安裝程式物件**](installer-object.md)的 [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)或 [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)函式、 [**ApplyPatch**](installer-applypatch.md)或 [**ApplyMultiplePatches**](installer-applymultiplepatches.md)方法，或/p [命令列選項](command-line-options.md)來套用修補程式。

> [!Note]
> 在安裝應用程式之前，您可以將修補程式註冊為具有較高的許可權。 註冊修補程式之後，它會維持註冊狀態，直到移除此修補程式的最後一個註冊應用程式為止。
> 
> 未移除整個應用程式，因此無法移除已套用至每個使用者受控應用程式的修補程式。 移除應用程式時，會移除每個使用者受管理應用程式的修補註冊。

您也可以使用這個方法來讓非系統管理員修補每一部電腦的應用程式，或者您可以使用 [使用者帳戶控制 (UAC) 修補](user-account-control--uac--patching.md)中所述的最低許可權修補。

## <a name="example-1"></a>範例 1

下列腳本範例會使用 [**SourceListAddSource**](patch-sourcelistaddsource.md)方法，將位於 \\ \\ 伺服器 \\ 共用 \\ 產品 \\ 修補程式範例中的 patch 套件註冊 \\ 為具有較高的許可權。 然後可以將該修補程式套用到每個使用者管理的產品。

``` syntax
const msiInstallContextUserManaged = 1
const msiInstallSourceTypeNetwork = 1

const PatchCode = "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}"
const UserSid = "S-X-X-XX-XXXXXXXXX-XXXXXXXXX-XXXXXXXXX-XXXXXXX"
const PatchPath = "\\server\share\products\patches\"
const PatchPackageName = "example.msp"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

Set patch = installer.Patch(PatchCode, "", UserSid, msiInstallContextUserManaged)

patch.SourceListAddSource msiInstallSourceTypeNetwork, PatchPath, 0

patch.SourceListInfo("PackageName") = PatchPackageName
```

## <a name="example-2"></a>範例 2

下列程式碼範例會使用 [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)函式，將位於 \\ \\ 伺服器 \\ 共用 \\ 產品 \\ 修補程式範例中的 patch 套件註冊 \\ 為具有更高的許可權。 然後可以將該修補程式套用到每個使用者管理的產品。


```C++
#ifndef UNICODE
#define UNICODE
#endif    // UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI
#endif    // _WIN32_MSI

#include <windows.h>
#include <msi.h>


/////////////////////////////////////////////////////////////////
// RegisterElevatedPatch
//
// Purpose: register a patch elevated from a network location
//
// Arguments:
//    wszPatchCode <entity type="ndash"/> GUID of patch to be registered
//    wszUserSid   - String SID that specifies the user account
//    wszPatchPath <entity type="ndash"/> Network location of patch
//    wszPatchPackageName <entity type="ndash"/> Package name of patch
//
/////////////////////////////////////////////////////////////////
UINT RegisterElevatedPatch(LPCWSTR wszPatchCode, 
LPCWSTR wszUserSid, 
LPCWSTR wszPatchPath, 
LPCWSTR wszPatchPackageName)
{
// wszUserSid can be NULL
// when wszUserSid is NULL, register patch for current user
// current user must be administrator
if (!wszPatchCode || !wszPatchPath || !wszPatchPackageName)
    return ERROR_INVALID_PARAMETER;

UINT uiReturn = ERROR_SUCCESS;

uiReturn = MsiSourceListAddSourceEx(
/*szPatchCode*/ wszPatchCode,
/*szUserSid*/ wszUserSid,
/*dwContext*/ MSIINSTALLCONTEXT_USERMANAGED,
/*dwOptions*/ MSISOURCETYPE_NETWORK+MSICODE_PATCH,
/*szSource*/ wszPatchPath,
/*dwIndex*/ 0);
if (ERROR_SUCCESS == uiReturn)
{
uiReturn = MsiSourceListSetInfo(
/*szPatchCode*/ wszPatchCode,
/*szUserSid*/ wszUserSid,
/*dwContext*/ MSIINSTALLCONTEXT_USERMANAGED,
/*dwOptions*/ MSISOURCETYPE_NETWORK+MSICODE_PATCH,
/*szProperty*/ L"PackageName",
/*szValue*/ wszPatchPackageName);
if (ERROR_SUCCESS != uiReturn)
{
// Function call failed, return error code
    return uiReturn;
}
}
else
{
// Function call failed, return error code
    return uiReturn;
}

return ERROR_SUCCESS;
}


```



 

 
