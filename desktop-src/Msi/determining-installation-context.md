---
description: 應用程式可以呼叫 MsiEnumProducts 或 MsiEnumProductsEx 函式來列舉系統上已安裝或公告的產品。
ms.assetid: 162bda20-0c62-4eac-8c1f-fd107e42c528
title: 判斷安裝內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24367e2367f845dfef2e4947a32d9dec84d644cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985667"
---
# <a name="determining-installation-context"></a><span data-ttu-id="74a8d-103">判斷安裝內容</span><span class="sxs-lookup"><span data-stu-id="74a8d-103">Determining Installation Context</span></span>

<span data-ttu-id="74a8d-104">應用程式可以呼叫 [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) 或 [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) 函式來列舉系統上已安裝或公告的產品。</span><span class="sxs-lookup"><span data-stu-id="74a8d-104">An application can call the [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) or [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) functions to enumerate products that are installed or advertised on the system.</span></span> <span data-ttu-id="74a8d-105">此函數可以列舉安裝在每部電腦 [安裝內容](installation-context.md)中的所有產品。</span><span class="sxs-lookup"><span data-stu-id="74a8d-105">This function can enumerate all the products installed in the per-machine [installation context](installation-context.md).</span></span> <span data-ttu-id="74a8d-106">它可以列舉針對目前使用者安裝在每個使用者內容中的產品。</span><span class="sxs-lookup"><span data-stu-id="74a8d-106">It can enumerate the products installed in the per-user context for the current user.</span></span> <span data-ttu-id="74a8d-107">應用程式可以藉由呼叫 [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) 或 [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) 函數來取得這些產品內容的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="74a8d-107">The application can retrieve information about the context of these products by calling the [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) or [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) functions.</span></span>

<span data-ttu-id="74a8d-108">Windows Installer 可以安裝產品，以提升非系統管理員使用者的 (系統) 許可權執行。</span><span class="sxs-lookup"><span data-stu-id="74a8d-108">The Windows Installer can install products to run with elevated (system) privileges for non-administrator users.</span></span> <span data-ttu-id="74a8d-109">這需要系統管理員使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="74a8d-109">This requires the permission of an administrator user.</span></span> <span data-ttu-id="74a8d-110">以較高的許可權安裝的產品稱為「受管理」。</span><span class="sxs-lookup"><span data-stu-id="74a8d-110">A product that is installed with elevated privileges is called "managed."</span></span> <span data-ttu-id="74a8d-111">每台電腦安裝的所有產品都是受控的。</span><span class="sxs-lookup"><span data-stu-id="74a8d-111">All products installed per-machine are managed.</span></span> <span data-ttu-id="74a8d-112">只有當本機系統代理程式在模擬使用者時執行公告時，才會管理每位使用者安裝的產品。</span><span class="sxs-lookup"><span data-stu-id="74a8d-112">Products installed per-user are only managed if a local system agent performs an advertisement while impersonating a user.</span></span> <span data-ttu-id="74a8d-113">這是透過 [群組原則](/previous-versions/windows/desktop/Policy/group-policy-start-page)軟體部署所使用的方法。</span><span class="sxs-lookup"><span data-stu-id="74a8d-113">This is the method used by software deployment through [Group Policy](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span></span> <span data-ttu-id="74a8d-114">設定 [AlwaysInstallElevated](alwaysinstallelevated.md) 原則時所安裝的每個使用者應用程式都不會被視為受管理。</span><span class="sxs-lookup"><span data-stu-id="74a8d-114">Per-user applications installed while the [AlwaysInstallElevated](alwaysinstallelevated.md) policies are set are not considered managed.</span></span> <span data-ttu-id="74a8d-115">藉由呼叫 [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)，應用程式可以檢查特定產品是否受管理。</span><span class="sxs-lookup"><span data-stu-id="74a8d-115">By calling [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda), an application can check whether a particular product is managed.</span></span>

<span data-ttu-id="74a8d-116">下列範例示範應用程式如何使用 [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)、 [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)和 [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)來判斷內容。</span><span class="sxs-lookup"><span data-stu-id="74a8d-116">The following sample demonstrates how an application determines context by using [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa), [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa), and [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda).</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif //UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI 200
#endif //_WIN32_MSI

#include <stdio.h>
#include <windows.h>
#include <msi.h>
#pragma comment(lib, "msi.lib")

const int cchGUID = 38;

UINT DetermineContextForAllProducts()
{
    WCHAR wszProductCode[cchGUID+1] = {0};
    WCHAR wszAssignmentType[10] = {0};
    DWORD cchAssignmentType = 
            sizeof(wszAssignmentType)/sizeof(wszAssignmentType[0]);
    DWORD dwIndex = 0;

    DWORD cchProductName = MAX_PATH;
    WCHAR* lpProductName = new WCHAR[cchProductName];
    if (!lpProductName)
    {
        return ERROR_OUTOFMEMORY;
    }

    UINT uiStatus = ERROR_SUCCESS;

    // enumerate all visible products
    do
    {
        uiStatus = MsiEnumProducts(dwIndex,
                          wszProductCode);
        if (ERROR_SUCCESS == uiStatus)
        {
            cchAssignmentType = 
                sizeof(wszAssignmentType)/sizeof(wszAssignmentType[0]);
            BOOL fPerMachine = FALSE;
            BOOL fManaged = FALSE;

            // Determine assignment type of product
            // This indicates whether the product
            // instance is per-user or per-machine
            if (ERROR_SUCCESS == 
                MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_ASSIGNMENTTYPE,wszAssignmentType,&cchAssignmentType))
            {
                if (L'1' == wszAssignmentType[0])
                    fPerMachine = TRUE;
            }
            else
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // determine the "managed" status of the product.
            // If fManaged is TRUE, product is installed managed
            // and runs with elevated privileges.
            // If fManaged is FALSE, product installation operations
            // run as the user.
            if (ERROR_SUCCESS != MsiIsProductElevated(wszProductCode,
                                         &fManaged))
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // obtain the user friendly name of the product
            UINT uiReturn = MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_PRODUCTNAME,lpProductName,&cchProductName);
            if (ERROR_MORE_DATA == uiReturn)
            {
                // try again, but with a larger product name buffer
                delete [] lpProductName;

                // returned character count does not include
                // terminating NULL
                ++cchProductName;

                lpProductName = new WCHAR[cchProductName];
                if (!lpProductName)
                {
                    uiStatus = ERROR_OUTOFMEMORY;
                    break;
                }

                uiReturn = MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_PRODUCTNAME,lpProductName,&cchProductName);
            }

            if (ERROR_SUCCESS != uiReturn)
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // output information
            wprintf(L" Product %s:\n", lpProductName);
            wprintf(L"\t%s\n", wszProductCode);
                        wprintf(L"\tInstalled %s %s\n", 
                fPerMachine ? L"per-machine" : L"per-user",
                fManaged ? L"managed" : L"non-managed");
        }
        dwIndex++;
    }
    while (ERROR_SUCCESS == uiStatus);

    if (lpProductName)
    {
        delete [] lpProductName;
        lpProductName = NULL;
    }

    return (ERROR_NO_MORE_ITEMS == uiStatus) ? ERROR_SUCCESS : uiStatus;
}
```



## <a name="related-topics"></a><span data-ttu-id="74a8d-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="74a8d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74a8d-118">**MsiEnumProducts**</span><span class="sxs-lookup"><span data-stu-id="74a8d-118">**MsiEnumProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> <dt>

[<span data-ttu-id="74a8d-119">**MsiGetProductInfo**</span><span class="sxs-lookup"><span data-stu-id="74a8d-119">**MsiGetProductInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[<span data-ttu-id="74a8d-120">**MsiGetProductInfoEx**</span><span class="sxs-lookup"><span data-stu-id="74a8d-120">**MsiGetProductInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
</dt> <dt>

[<span data-ttu-id="74a8d-121">**MsiIsProductElevated**</span><span class="sxs-lookup"><span data-stu-id="74a8d-121">**MsiIsProductElevated**</span></span>](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)
</dt> <dt>

[<span data-ttu-id="74a8d-122">以較高的許可權安裝非系統管理員的封裝</span><span class="sxs-lookup"><span data-stu-id="74a8d-122">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
</dt> <dt>

[<span data-ttu-id="74a8d-123">廣告以較高的許可權安裝的 Per-User 應用程式</span><span class="sxs-lookup"><span data-stu-id="74a8d-123">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
</dt> <dt>

[<span data-ttu-id="74a8d-124">安裝內容</span><span class="sxs-lookup"><span data-stu-id="74a8d-124">Installation Context</span></span>](installation-context.md)
</dt> </dl>

 

 
