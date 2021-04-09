---
description: Product 資料庫包含產品的相關資訊。 如需使用列舉函數取得產品資訊的詳細資訊，請參閱初始化應用程式。
ms.assetid: 528c915c-296c-4620-8105-0b5d543e56a5
title: 取得應用程式資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dce842f057efb65b6d0db3ad0407a19bf08435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943765"
---
# <a name="getting-application-information"></a><span data-ttu-id="f4770-104">取得應用程式資訊</span><span class="sxs-lookup"><span data-stu-id="f4770-104">Getting Application Information</span></span>

<span data-ttu-id="f4770-105">Product 資料庫包含產品的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f4770-105">The product database contains information about a product.</span></span> <span data-ttu-id="f4770-106">如需使用列舉函數取得產品資訊的詳細資訊，請參閱 [初始化應用程式](initializing-an-application.md)。</span><span class="sxs-lookup"><span data-stu-id="f4770-106">For more information on obtaining product information with enumeration functions, see [Initializing an Application](initializing-an-application.md).</span></span>

<span data-ttu-id="f4770-107">**取得產品資訊**</span><span class="sxs-lookup"><span data-stu-id="f4770-107">**To get product information**</span></span>

1.  <span data-ttu-id="f4770-108">藉由呼叫 [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) 函式，確認是否已安裝產品。</span><span class="sxs-lookup"><span data-stu-id="f4770-108">Verify that a product is installed by calling the [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) function.</span></span>
2.  <span data-ttu-id="f4770-109">開啟資料庫，然後藉由呼叫 [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) 函數來取得其控制碼。</span><span class="sxs-lookup"><span data-stu-id="f4770-109">Open the database and obtain a handle to it by calling the [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) function.</span></span>

    <span data-ttu-id="f4770-110">如果資料庫包含在安裝封裝中，請呼叫 [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) 函數。</span><span class="sxs-lookup"><span data-stu-id="f4770-110">If the database is contained in an installation package, call the [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) function.</span></span>

3.  <span data-ttu-id="f4770-111">使用開啟控制碼來取得具有 [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) 函式的產品屬性，並使用 [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) 函式取得描述性的功能資訊。</span><span class="sxs-lookup"><span data-stu-id="f4770-111">Use the open handle to obtain product properties with the [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) function, and to obtain descriptive feature information with the [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) function.</span></span>

    <span data-ttu-id="f4770-112">如果您想要使用產品代碼取得產品資訊，而不是使用開放式資料庫控制碼，請呼叫 [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) 函式，而不是 [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)。</span><span class="sxs-lookup"><span data-stu-id="f4770-112">If you want to obtain product information using the product code, rather than using the open database handle, call the [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) function instead of [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).</span></span>

4.  <span data-ttu-id="f4770-113">藉由呼叫 [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) 函數來關閉開啟的安裝控制碼。</span><span class="sxs-lookup"><span data-stu-id="f4770-113">Close an open installation handle by calling the [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) function.</span></span>

    <span data-ttu-id="f4770-114">[**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles)函式是診斷函數，不應該用來關閉您知道要開啟的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f4770-114">The [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) function is a diagnostic function and should not be used to close handles you know to be open.</span></span> <span data-ttu-id="f4770-115">當應用程式關閉時，可以接受呼叫 **MsiCloseAllHandles** 函式，以確保已關閉所有控制碼。</span><span class="sxs-lookup"><span data-stu-id="f4770-115">It is acceptable to call the **MsiCloseAllHandles** function when the application closes to ensure that all handles have been closed.</span></span>

 

 



