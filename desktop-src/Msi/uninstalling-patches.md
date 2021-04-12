---
description: 從 Windows Installer 3.0 開始，您可以從應用程式卸載一些修補程式。
ms.assetid: 11e995b7-30c7-4992-b436-3af289ac3966
title: 卸載修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff9418704bdeeb5ccc57839cbe2416faa5692265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195419"
---
# <a name="uninstalling-patches"></a>卸載修補程式

從 Windows Installer 3.0 開始，您可以從應用程式卸載一些修補程式。 修補程式必須是 [可卸載修補程式](uninstallable-patches.md)。 使用小於3.0 版的 Windows Installer 版本時， [移除修補](removing-patches.md) 程式需要卸載修補產品，並在不套用修補程式的情況下重新安裝產品。

**Windows Installer 2.0：** 不支援。 使用早于 Windows Installer 3.0 的 Windows Installer 版本所套用的修補程式則不會可卸載。

當您使用下列任何一種方法來叫用修補程式卸載時，安裝程式會嘗試從應用程式或要求卸載的使用者看到的第一個產品中移除修補程式。 安裝程式會依下列順序搜尋修補過的產品：每位使用者管理、每位使用者非受控、每部電腦。

## <a name="uninstalling-a-patch-using-msipatchremove-on-a-command-line"></a>在命令列上使用 MSIPATCHREMOVE 卸載修補程式

您可以使用 msiexec.exe 和 [命令列選項](command-line-options.md)，從命令卸載修補程式。 下列命令列範例會使用 [**MSIPATCHREMOVE**](msipatchremove.md)屬性和/i 命令列選項，從應用程式中移除 [可卸載修補](uninstallable-patches.md)程式（例如 .msp），example.msi。 使用/i 時，已修補的應用程式可透過應用程式封裝的路徑來識別 ( .msi 檔案) 或應用程式的 [產品代碼](product-codes.md)。 在此範例中，應用程式的安裝套件位於「 \\ \\ server \\ share \\ products \\ 範例example.msi」 \\ ，而應用程式的 [**ProductCode**](productcode.md)屬性為 "{0C9840E7-7F0B-C648-10F0-4641926FE463}"。 修補程式套件位於「 \\ \\ 伺服器 \\ 共用 \\ 產品 \\ 範例 \\ 修補程式 \\ 範例 .msp」，而 patch code GUID 為 "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"。

**Msiexec/I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE = {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/qb**

## <a name="uninstalling-a-patch-using-the-standard-command-line-options"></a>使用標準命令列選項卸載修補程式

從 Windows Installer 版本3.0 開始，您可以使用 Microsoft Windows 作業系統更新所使用的 [標準命令列選項](standard-installer-command-line-options.md) (update.exe) 從命令列卸載 Windows Installer 修補程式。

下列命令列是標準命令列，相當於使用 [**MSIPATCHREMOVE**](msipatchremove.md) 屬性卸載修補程式的 Windows Installer 命令列。 搭配/package 選項使用的/uninstall 選項表示卸載修補程式。 修補程式的完整路徑或 patch code GUID 可以參考修補程式。

**Msiexec/package {0C9840E7-7F0B-C648-10F0-4641926FE463}/uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/passive**

> [!Note]  
> /Passive standard 選項與 Windows Installer/qb 選項完全相等。

 

## <a name="uninstalling-a-patch-using-the-removepatches-method"></a>使用 RemovePatches 方法卸載修補程式

您可以使用 Windows Installer [Automation 介面](automation-interface.md)，從腳本卸載修補程式。 下列腳本範例會使用 [安裝](installer-object.md)程式物件的 [**RemovePatches**](installer-removepatches.md)方法，從應用程式中移除 [可卸載 patch](uninstallable-patches.md)（例如 .msp），example.msi。 要卸載的每個修補程式都可以用修補封裝的完整路徑或 patch code GUID 來表示。 在此範例中，應用程式的安裝套件位於「 \\ \\ server \\ share \\ products \\ 範例example.msi」 \\ ，而應用程式的 [**ProductCode**](productcode.md)屬性為 "{0C9840E7-7F0B-C648-10F0-4641926FE463}"。 修補程式套件位於「 \\ \\ 伺服器 \\ 共用 \\ 產品 \\ 範例 \\ 修補程式 \\ 範例 .msp」，而 patch code GUID 為 "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"。


```VB
const msiInstallTypeSingleInstance = 2
const PatchList = "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"
const Product = "{0C9840E7-7F0B-C648-10F0-4641926FE463}"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

installer.RemovePatches(PatchList, Product, msiInstallTypeSingleInstance, "")
```



## <a name="uninstalling-a-patch-using-addremove-programs"></a>使用 [新增/移除程式] 卸載修補程式

在 Windows XP 中，您可以使用 [新增/移除程式] 卸載修補程式。

## <a name="uninstalling-a-patch-using-the-msiremovepatches-function"></a>使用 MsiRemovePatches 函數卸載修補程式

您的應用程式可以使用 [Windows Installer 功能](installer-functions.md)，從其他應用程式卸載修補程式。 下列程式碼範例會使用 [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)函數，從應用程式中移除 [可卸載 patch](uninstallable-patches.md)（.msp），example.msi。 Patch 封裝的完整路徑或 patch code GUID 可以參考修補程式。 在此範例中，應用程式的安裝套件位於「 \\ \\ server \\ share \\ products \\ 範例example.msi」 \\ ，而應用程式的 [**ProductCode**](productcode.md)屬性為 "{0C9840E7-7F0B-C648-10F0-4641926FE463}"。 修補程式套件位於「 \\ \\ 伺服器 \\ 共用 \\ 產品 \\ 範例 \\ 修補程式 \\ 範例 .msp」，而 patch code GUID 為 "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"。


```C++
    UINT uiReturn = MsiRemovePatches(
          /*szPatchList=*/TEXT("\\server\\share\\products\\example\\patches\\example.msp"),
          /*szProductCode=*/  TEXT("{0C9840E7-7F0B-C648-10F0-4641926FE463}"),
          /*eUninstallType=*/ INSTALLTYPE_SINGLE_INSTANCE,
          /*szPropertyList=*/ NULL);
```



## <a name="uninstalling-a-patch-from-all-applications-using-msiremovepatches-function"></a>使用 MsiRemovePatches 函式從所有應用程式卸載修補程式

單一修補程式可在電腦上更新多項產品。 應用程式可以使用 [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) 來列舉電腦上的所有產品，並判斷是否已將修補程式套用至產品的特定實例。 然後，應用程式可以使用 [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)卸載修補程式。 例如，如果修補程式更新多個產品所共用之元件中的檔案，且發行修補程式來更新這兩項產品，則單一修補程式可能會更新多個產品。

下列範例會示範應用程式如何使用 Windows Installer，從所有可用的應用程式中移除修補程式。 它不會從為其他使用者為每位使用者安裝的應用程式移除修補程式。


```C++
#ifndef UNICODE
#define UNICODE
#endif //UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI 300
#endif //_WIN32_MSI

#include <stdio.h>
#include <windows.h>
#include <msi.h>

#pragma comment(lib, "msi.lib")

const int cchGUID = 38;

///////////////////////////////////////////////////////////////////
// RemovePatchFromAllVisibleapplications:
//
// Arguments:
//    wszPatchToRemove - GUID of patch to remove
//
///////////////////////////////////////////////////////////////////
//
UINT RemovePatchFromAllVisibleapplications(LPCWSTR wszPatchToRemove)
{
    if (!wszPatchToRemove)
        return ERROR_INVALID_PARAMETER;

    UINT uiStatus = ERROR_SUCCESS;
    DWORD dwIndex = 0;
    WCHAR wszapplicationCode[cchGUID+1] = {0};

    DWORD dwapplicationSearchContext = MSIINSTALLCONTEXT_ALL;
    MSIINSTALLCONTEXT dwInstallContext = MSIINSTALLCONTEXT_NONE;

    do
    {
        // Enumerate all visible applications in all contexts for the caller.
        // NULL for szUserSid defaults to using the caller's SID
        uiStatus = MsiEnumProductsEx(/*szapplicationCode*/NULL,
         /*szUserSid*/NULL,
         dwapplicationSearchContext,
         dwIndex,
         wszapplicationCode,
         &dwInstallContext,
         /*szSid*/NULL,
         /*pcchSid*/NULL);

        if (ERROR_SUCCESS == uiStatus)
        {
            // check to see if the provided patch is
            // registered for this application instance
            UINT uiPatchStatus = MsiGetPatchInfoEx(wszPatchToRemove,
             wszapplicationCode,
             /*szUserSid*/NULL,
             dwInstallContext,
             INSTALLPROPERTY_PATCHSTATE,
             NULL,
             NULL);

            if (ERROR_SUCCESS == uiPatchStatus)
            {
                // patch is registered to this application; remove patch
                wprintf(L"Removing patch %s from application %s...\n",
                 wszPatchToRemove, wszapplicationCode);
                                
                UINT uiRemoveStatus = MsiRemovePatches(
                 wszPatchToRemove,
                 wszapplicationCode,
                 INSTALLTYPE_SINGLE_INSTANCE,
                 L"");

                if (ERROR_SUCCESS != uiRemoveStatus)
                {
                    // This halts the enumeration and fails. Alternatively
                    // you could output an error and continue the
                    // enumeration
                     return ERROR_FUNCTION_FAILED;
                }
            }
            else if (ERROR_UNKNOWN_PATCH != uiPatchStatus)
            {
                // Some other error occurred during processing. This
                // halts the enumeration and fails. Alternatively you
                // could output an error and continue the enumeration
                 return ERROR_FUNCTION_FAILED;
            }
            // else patch was not applied to this application
            // (ERROR_UNKNOWN_PATCH returned)
        }

        dwIndex++;
    }
    while (uiStatus == ERROR_SUCCESS);

    if (ERROR_NO_MORE_ITEMS != uiStatus)
        return ERROR_FUNCTION_FAILED;

    return ERROR_SUCCESS;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[修補程式順序](sequencing-patches.md)
</dt> <dt>

[移除修補程式](removing-patches.md)
</dt> <dt>

[可卸載修補程式](uninstallable-patches.md)
</dt> <dt>

[修補卸載自訂動作](patch-uninstall-custom-actions.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



