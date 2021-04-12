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
# <a name="uninstalling-patches"></a><span data-ttu-id="49b58-103">卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="49b58-103">Uninstalling Patches</span></span>

<span data-ttu-id="49b58-104">從 Windows Installer 3.0 開始，您可以從應用程式卸載一些修補程式。</span><span class="sxs-lookup"><span data-stu-id="49b58-104">Beginning with Windows Installer 3.0, it is possible to uninstall some patches from applications.</span></span> <span data-ttu-id="49b58-105">修補程式必須是 [可卸載修補程式](uninstallable-patches.md)。</span><span class="sxs-lookup"><span data-stu-id="49b58-105">The patch must be an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="49b58-106">使用小於3.0 版的 Windows Installer 版本時， [移除修補](removing-patches.md) 程式需要卸載修補產品，並在不套用修補程式的情況下重新安裝產品。</span><span class="sxs-lookup"><span data-stu-id="49b58-106">When using a Windows Installer version less than version 3.0, [removing patches](removing-patches.md) requires uninstalling the patch product and reinstalling the product without applying the patch.</span></span>

<span data-ttu-id="49b58-107">**Windows Installer 2.0：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="49b58-107">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="49b58-108">使用早于 Windows Installer 3.0 的 Windows Installer 版本所套用的修補程式則不會可卸載。</span><span class="sxs-lookup"><span data-stu-id="49b58-108">Patches applied using a version of Windows Installer that is earlier than Windows Installer 3.0 are not uninstallable.</span></span>

<span data-ttu-id="49b58-109">當您使用下列任何一種方法來叫用修補程式卸載時，安裝程式會嘗試從應用程式或要求卸載的使用者看到的第一個產品中移除修補程式。</span><span class="sxs-lookup"><span data-stu-id="49b58-109">When you invoke an uninstallation of a patch by any of the following methods, the installer attempts to remove the patch from the first product visible to the application or user requesting the uninstallation.</span></span> <span data-ttu-id="49b58-110">安裝程式會依下列順序搜尋修補過的產品：每位使用者管理、每位使用者非受控、每部電腦。</span><span class="sxs-lookup"><span data-stu-id="49b58-110">The installer searches for patched products in the following order: per-user managed, per-user unmanaged, per-machine.</span></span>

## <a name="uninstalling-a-patch-using-msipatchremove-on-a-command-line"></a><span data-ttu-id="49b58-111">在命令列上使用 MSIPATCHREMOVE 卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="49b58-111">Uninstalling a patch using MSIPATCHREMOVE on a command line</span></span>

<span data-ttu-id="49b58-112">您可以使用 msiexec.exe 和 [命令列選項](command-line-options.md)，從命令卸載修補程式。</span><span class="sxs-lookup"><span data-stu-id="49b58-112">You can uninstall patches from a command by using msiexec.exe and the [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="49b58-113">下列命令列範例會使用 [**MSIPATCHREMOVE**](msipatchremove.md)屬性和/i 命令列選項，從應用程式中移除 [可卸載修補](uninstallable-patches.md)程式（例如 .msp），example.msi。</span><span class="sxs-lookup"><span data-stu-id="49b58-113">The following sample command line removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**MSIPATCHREMOVE**](msipatchremove.md) property and the /i command line option.</span></span> <span data-ttu-id="49b58-114">使用/i 時，已修補的應用程式可透過應用程式封裝的路徑來識別 ( .msi 檔案) 或應用程式的 [產品代碼](product-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="49b58-114">When using /i, the patched application can be identified by the path to the application's package (.msi file) or the application's [product code](product-codes.md).</span></span> <span data-ttu-id="49b58-115">在此範例中，應用程式的安裝套件位於「 \\ \\ server \\ share \\ products \\ 範例example.msi」 \\ ，而應用程式的 [**ProductCode**](productcode.md)屬性為 "{0C9840E7-7F0B-C648-10F0-4641926FE463}"。</span><span class="sxs-lookup"><span data-stu-id="49b58-115">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="49b58-116">修補程式套件位於「 \\ \\ 伺服器 \\ 共用 \\ 產品 \\ 範例 \\ 修補程式 \\ 範例 .msp」，而 patch code GUID 為 "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"。</span><span class="sxs-lookup"><span data-stu-id="49b58-116">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>

<span data-ttu-id="49b58-117">**Msiexec/I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE = {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/qb**</span><span class="sxs-lookup"><span data-stu-id="49b58-117">**Msiexec /I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE={EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /qb**</span></span>

## <a name="uninstalling-a-patch-using-the-standard-command-line-options"></a><span data-ttu-id="49b58-118">使用標準命令列選項卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="49b58-118">Uninstalling a patch using the standard command line options</span></span>

<span data-ttu-id="49b58-119">從 Windows Installer 版本3.0 開始，您可以使用 Microsoft Windows 作業系統更新所使用的 [標準命令列選項](standard-installer-command-line-options.md) (update.exe) 從命令列卸載 Windows Installer 修補程式。</span><span class="sxs-lookup"><span data-stu-id="49b58-119">Beginning with Windows Installer version 3.0, you can use the [standard command line options](standard-installer-command-line-options.md) used by Microsoft Windows Operating System Updates (update.exe) to uninstall Windows Installer patches from a command line.</span></span>

<span data-ttu-id="49b58-120">下列命令列是標準命令列，相當於使用 [**MSIPATCHREMOVE**](msipatchremove.md) 屬性卸載修補程式的 Windows Installer 命令列。</span><span class="sxs-lookup"><span data-stu-id="49b58-120">The following command line is the standard command line equivalent of the Windows Installer command line used to uninstall a patch using the [**MSIPATCHREMOVE**](msipatchremove.md) property.</span></span> <span data-ttu-id="49b58-121">搭配/package 選項使用的/uninstall 選項表示卸載修補程式。</span><span class="sxs-lookup"><span data-stu-id="49b58-121">The /uninstall option used with the /package option denotes the uninstallation of a patch.</span></span> <span data-ttu-id="49b58-122">修補程式的完整路徑或 patch code GUID 可以參考修補程式。</span><span class="sxs-lookup"><span data-stu-id="49b58-122">The patch can be referenced by the full path to the patch or by the patch code GUID.</span></span>

<span data-ttu-id="49b58-123">**Msiexec/package {0C9840E7-7F0B-C648-10F0-4641926FE463}/uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/passive**</span><span class="sxs-lookup"><span data-stu-id="49b58-123">**Msiexec /package {0C9840E7-7F0B-C648-10F0-4641926FE463} /uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /passive**</span></span>

> [!Note]  
> <span data-ttu-id="49b58-124">/Passive standard 選項與 Windows Installer/qb 選項完全相等。</span><span class="sxs-lookup"><span data-stu-id="49b58-124">The /passive standard option is not an exact equivalent of the Windows Installer /qb option.</span></span>

 

## <a name="uninstalling-a-patch-using-the-removepatches-method"></a><span data-ttu-id="49b58-125">使用 RemovePatches 方法卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="49b58-125">Uninstalling a patch using the RemovePatches method</span></span>

<span data-ttu-id="49b58-126">您可以使用 Windows Installer [Automation 介面](automation-interface.md)，從腳本卸載修補程式。</span><span class="sxs-lookup"><span data-stu-id="49b58-126">You can uninstall patches from script by using the Windows Installer [Automation Interface](automation-interface.md).</span></span> <span data-ttu-id="49b58-127">下列腳本範例會使用 [安裝](installer-object.md)程式物件的 [**RemovePatches**](installer-removepatches.md)方法，從應用程式中移除 [可卸載 patch](uninstallable-patches.md)（例如 .msp），example.msi。</span><span class="sxs-lookup"><span data-stu-id="49b58-127">The following scripting sample removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**RemovePatches**](installer-removepatches.md) method of the [Installer](installer-object.md) object.</span></span> <span data-ttu-id="49b58-128">要卸載的每個修補程式都可以用修補封裝的完整路徑或 patch code GUID 來表示。</span><span class="sxs-lookup"><span data-stu-id="49b58-128">Each patch being uninstalled can be represented by either the full path to the patch package or the patch code GUID.</span></span> <span data-ttu-id="49b58-129">在此範例中，應用程式的安裝套件位於「 \\ \\ server \\ share \\ products \\ 範例example.msi」 \\ ，而應用程式的 [**ProductCode**](productcode.md)屬性為 "{0C9840E7-7F0B-C648-10F0-4641926FE463}"。</span><span class="sxs-lookup"><span data-stu-id="49b58-129">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="49b58-130">修補程式套件位於「 \\ \\ 伺服器 \\ 共用 \\ 產品 \\ 範例 \\ 修補程式 \\ 範例 .msp」，而 patch code GUID 為 "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"。</span><span class="sxs-lookup"><span data-stu-id="49b58-130">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>


```VB
const msiInstallTypeSingleInstance = 2
const PatchList = "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"
const Product = "{0C9840E7-7F0B-C648-10F0-4641926FE463}"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

installer.RemovePatches(PatchList, Product, msiInstallTypeSingleInstance, "")
```



## <a name="uninstalling-a-patch-using-addremove-programs"></a><span data-ttu-id="49b58-131">使用 [新增/移除程式] 卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="49b58-131">Uninstalling a patch using Add/Remove Programs</span></span>

<span data-ttu-id="49b58-132">在 Windows XP 中，您可以使用 [新增/移除程式] 卸載修補程式。</span><span class="sxs-lookup"><span data-stu-id="49b58-132">With Windows XP, you can uninstall patches using Add/Remove programs.</span></span>

## <a name="uninstalling-a-patch-using-the-msiremovepatches-function"></a><span data-ttu-id="49b58-133">使用 MsiRemovePatches 函數卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="49b58-133">Uninstalling a patch using the MsiRemovePatches function</span></span>

<span data-ttu-id="49b58-134">您的應用程式可以使用 [Windows Installer 功能](installer-functions.md)，從其他應用程式卸載修補程式。</span><span class="sxs-lookup"><span data-stu-id="49b58-134">Your applications can uninstall patches from other applications by using the [Windows Installer Functions](installer-functions.md).</span></span> <span data-ttu-id="49b58-135">下列程式碼範例會使用 [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)函數，從應用程式中移除 [可卸載 patch](uninstallable-patches.md)（.msp），example.msi。</span><span class="sxs-lookup"><span data-stu-id="49b58-135">The following code example removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) function.</span></span> <span data-ttu-id="49b58-136">Patch 封裝的完整路徑或 patch code GUID 可以參考修補程式。</span><span class="sxs-lookup"><span data-stu-id="49b58-136">A patch can be referenced by the full path to the patch package or the patch code GUID.</span></span> <span data-ttu-id="49b58-137">在此範例中，應用程式的安裝套件位於「 \\ \\ server \\ share \\ products \\ 範例example.msi」 \\ ，而應用程式的 [**ProductCode**](productcode.md)屬性為 "{0C9840E7-7F0B-C648-10F0-4641926FE463}"。</span><span class="sxs-lookup"><span data-stu-id="49b58-137">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="49b58-138">修補程式套件位於「 \\ \\ 伺服器 \\ 共用 \\ 產品 \\ 範例 \\ 修補程式 \\ 範例 .msp」，而 patch code GUID 為 "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"。</span><span class="sxs-lookup"><span data-stu-id="49b58-138">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>


```C++
    UINT uiReturn = MsiRemovePatches(
          /*szPatchList=*/TEXT("\\server\\share\\products\\example\\patches\\example.msp"),
          /*szProductCode=*/  TEXT("{0C9840E7-7F0B-C648-10F0-4641926FE463}"),
          /*eUninstallType=*/ INSTALLTYPE_SINGLE_INSTANCE,
          /*szPropertyList=*/ NULL);
```



## <a name="uninstalling-a-patch-from-all-applications-using-msiremovepatches-function"></a><span data-ttu-id="49b58-139">使用 MsiRemovePatches 函式從所有應用程式卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="49b58-139">Uninstalling a patch from all applications using MsiRemovePatches function</span></span>

<span data-ttu-id="49b58-140">單一修補程式可在電腦上更新多項產品。</span><span class="sxs-lookup"><span data-stu-id="49b58-140">A single patch can update more than one product on the computer.</span></span> <span data-ttu-id="49b58-141">應用程式可以使用 [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) 來列舉電腦上的所有產品，並判斷是否已將修補程式套用至產品的特定實例。</span><span class="sxs-lookup"><span data-stu-id="49b58-141">An application can use [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) to enumerate all the products on the computer and determine whether a patch has been applied to a particular instance of the product.</span></span> <span data-ttu-id="49b58-142">然後，應用程式可以使用 [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)卸載修補程式。</span><span class="sxs-lookup"><span data-stu-id="49b58-142">The application can then uninstall the patch using [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span></span> <span data-ttu-id="49b58-143">例如，如果修補程式更新多個產品所共用之元件中的檔案，且發行修補程式來更新這兩項產品，則單一修補程式可能會更新多個產品。</span><span class="sxs-lookup"><span data-stu-id="49b58-143">For example, a single patch can update multiple products if the patch updates a file in a component that is shared by multiple products and the patch is distributed to update both products.</span></span>

<span data-ttu-id="49b58-144">下列範例會示範應用程式如何使用 Windows Installer，從所有可用的應用程式中移除修補程式。</span><span class="sxs-lookup"><span data-stu-id="49b58-144">The following example demonstrates how an application can use the Windows Installer to remove a patch from all applications that are available to the user.</span></span> <span data-ttu-id="49b58-145">它不會從為其他使用者為每位使用者安裝的應用程式移除修補程式。</span><span class="sxs-lookup"><span data-stu-id="49b58-145">It does not remove the patch from applications installed per-user for another user.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="49b58-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="49b58-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49b58-147">修補程式順序</span><span class="sxs-lookup"><span data-stu-id="49b58-147">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="49b58-148">移除修補程式</span><span class="sxs-lookup"><span data-stu-id="49b58-148">Removing Patches</span></span>](removing-patches.md)
</dt> <dt>

[<span data-ttu-id="49b58-149">可卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="49b58-149">Uninstallable Patches</span></span>](uninstallable-patches.md)
</dt> <dt>

[<span data-ttu-id="49b58-150">修補卸載自訂動作</span><span class="sxs-lookup"><span data-stu-id="49b58-150">Patch Uninstall Custom Actions</span></span>](patch-uninstall-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="49b58-151">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="49b58-151">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="49b58-152">**MsiEnumapplicationsEx**</span><span class="sxs-lookup"><span data-stu-id="49b58-152">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="49b58-153">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="49b58-153">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="49b58-154">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="49b58-154">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



