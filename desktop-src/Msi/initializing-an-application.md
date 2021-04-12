---
description: 若要啟用安裝程式功能，應用程式必須在初始化時呼叫許多函數。
ms.assetid: cfeaf9b9-f772-49f9-8b6f-e7fd0c93cc9f
title: 初始化應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221c5d97f0febb23ba73f98605ee6ec0e853940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192441"
---
# <a name="initializing-an-application"></a><span data-ttu-id="7fef4-103">初始化應用程式</span><span class="sxs-lookup"><span data-stu-id="7fef4-103">Initializing an Application</span></span>

<span data-ttu-id="7fef4-104">若要啟用安裝程式功能，應用程式必須在初始化時呼叫許多函數。</span><span class="sxs-lookup"><span data-stu-id="7fef4-104">To enable installer functionality, an application must call a number of functions when it is initializing.</span></span> <span data-ttu-id="7fef4-105">如需詳細資訊，請參閱 [安裝機制](installation-mechanism.md)。</span><span class="sxs-lookup"><span data-stu-id="7fef4-105">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span> <span data-ttu-id="7fef4-106">下列步驟說明如何使用安裝程式將應用程式初始化：</span><span class="sxs-lookup"><span data-stu-id="7fef4-106">The following steps describe how to use the installer to initialize an application:</span></span>

<span data-ttu-id="7fef4-107">**初始化應用程式**</span><span class="sxs-lookup"><span data-stu-id="7fef4-107">**To initialize an application**</span></span>

1.  <span data-ttu-id="7fef4-108">呼叫 [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) 函式，讓應用程式能夠將其本身識別為安裝程式。</span><span class="sxs-lookup"><span data-stu-id="7fef4-108">Call the [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) function so the application can identify itself to the installer.</span></span>

    <span data-ttu-id="7fef4-109">產品代碼是許多安裝程式函數的必要參數。</span><span class="sxs-lookup"><span data-stu-id="7fef4-109">The product code is a required parameter for many installer functions.</span></span>

2.  <span data-ttu-id="7fef4-110">呼叫 [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) 函式，以在應用程式第一次啟動時收集使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="7fef4-110">Call the [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) function to collect user information the first time the application starts.</span></span>

    <span data-ttu-id="7fef4-111">如果呼叫 [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) 失敗，請呼叫 [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) 函式來收集使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="7fef4-111">If the call to [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) fails, call the [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) function to collect user information.</span></span>

3.  <span data-ttu-id="7fef4-112">藉由呼叫 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) 函式來顯示預設使用者介面（如有必要）。</span><span class="sxs-lookup"><span data-stu-id="7fef4-112">Display a default user interface, if necessary, by calling the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) function.</span></span>

    <span data-ttu-id="7fef4-113">若要撰寫您自己的使用者介面，請呼叫 [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) 函式將其註冊到安裝程式。</span><span class="sxs-lookup"><span data-stu-id="7fef4-113">To author your own user interface, register it with the installer by calling the [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) function.</span></span>

4.  <span data-ttu-id="7fef4-114">呼叫 [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) 函數來設定記錄層級。</span><span class="sxs-lookup"><span data-stu-id="7fef4-114">Call the [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) function to set the logging level.</span></span>
5.  <span data-ttu-id="7fef4-115">藉由列舉應用程式的功能，讓使用者擁有可用的功能。</span><span class="sxs-lookup"><span data-stu-id="7fef4-115">Present the user with available features by enumerating the features of your application.</span></span> <span data-ttu-id="7fef4-116">您可以透過下列方式列舉功能：</span><span class="sxs-lookup"><span data-stu-id="7fef4-116">You can enumerate features in the following ways:</span></span>
    -   <span data-ttu-id="7fef4-117">依功能查詢安裝程式功能。</span><span class="sxs-lookup"><span data-stu-id="7fef4-117">Query the installer feature-by-feature.</span></span> <span data-ttu-id="7fef4-118">例如，在應用程式繪製按鈕或功能表項目之前，應用程式會呼叫 [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) 函式，讓安裝程式可以檢查功能是否可用。</span><span class="sxs-lookup"><span data-stu-id="7fef4-118">For example, before the application draws a button or a menu item, the application calls the [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) function so the installer can check that the feature is available.</span></span>
    -   <span data-ttu-id="7fef4-119">藉由呼叫 [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) 函數，一次列舉所有可用的功能。</span><span class="sxs-lookup"><span data-stu-id="7fef4-119">Enumerate all of the available features at once by calling the [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) function.</span></span> <span data-ttu-id="7fef4-120">若要使用此函數，應用程式必須在遞增索引時重複呼叫 **MsiEnumFeatures** 。</span><span class="sxs-lookup"><span data-stu-id="7fef4-120">To use this function, the application must call **MsiEnumFeatures** repeatedly while incrementing an index.</span></span>
6.  <span data-ttu-id="7fef4-121">若要取得目前安裝的詳細資訊，請重複呼叫下列列舉函數，為每個呼叫遞增索引變數：</span><span class="sxs-lookup"><span data-stu-id="7fef4-121">Get detailed information about the current installation by calling the following enumeration functions repeatedly, incrementing an index variable for each call:</span></span>

    -   <span data-ttu-id="7fef4-122">呼叫 [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) 函式來列舉向安裝程式註冊的產品。</span><span class="sxs-lookup"><span data-stu-id="7fef4-122">Call the [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) function to enumerate products registered with the installer.</span></span>
    -   <span data-ttu-id="7fef4-123">呼叫 [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) 函數來列舉元件。</span><span class="sxs-lookup"><span data-stu-id="7fef4-123">Call the [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) function to enumerate components.</span></span>
    -   <span data-ttu-id="7fef4-124">呼叫 [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) 函數來列舉元件限定詞。</span><span class="sxs-lookup"><span data-stu-id="7fef4-124">Call the [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) function to enumerate component qualifiers.</span></span>
    -   <span data-ttu-id="7fef4-125">呼叫 [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) 函數，以列舉特定元件的產品。</span><span class="sxs-lookup"><span data-stu-id="7fef4-125">Call the [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) function to enumerate the products for a particular component.</span></span>

    <span data-ttu-id="7fef4-126">如果列舉函數的傳回值是錯誤 \_ 成功，則會列舉更多專案，而且應該使用遞增的索引變數再次呼叫函式。</span><span class="sxs-lookup"><span data-stu-id="7fef4-126">If the return value on an enumeration function is ERROR\_SUCCESS, there are still more items to be enumerated and the function should be called again with an incremented index variable.</span></span> <span data-ttu-id="7fef4-127">如果傳回值 \_ 沒有 \_ 其他 \_ 專案，則會列舉所有的專案，而且不應該再次呼叫該函式。</span><span class="sxs-lookup"><span data-stu-id="7fef4-127">If the return value is ERROR\_NO\_MORE\_ITEMS, then all of the items have been enumerated, and the function should not be called again.</span></span>

 

 



