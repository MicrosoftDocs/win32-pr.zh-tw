---
title: ADSI 介面
description: 本主題說明 ADSI 介面所使用的類別。
ms.assetid: 8c735dbf-41d7-4fbb-b372-9abe4e1b8fdd
ms.tgt_platform: multiple
keywords:
- ADSI 介面 ADSI
- ADSI ADSI、參考、介面
- 介面 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2930292defa99301fb74f37c933a9af24b73f1fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371853"
---
# <a name="adsi-interfaces"></a><span data-ttu-id="7a751-106">ADSI 介面</span><span class="sxs-lookup"><span data-stu-id="7a751-106">ADSI Interfaces</span></span>

<span data-ttu-id="7a751-107">Active Directory 服務介面 (ADSI) 支援一組豐富的介面，可根據下列類別分類：</span><span class="sxs-lookup"><span data-stu-id="7a751-107">Active Directory Service Interfaces (ADSI) supports a rich set of interfaces that can be classified according to the following categories:</span></span>

-   <span data-ttu-id="7a751-108">[核心](core-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="7a751-108">[Core](core-interfaces.md).</span></span> <span data-ttu-id="7a751-109">這些介面會提供 ADSI 物件的基本物件管理功能。</span><span class="sxs-lookup"><span data-stu-id="7a751-109">These interfaces provide the basic object management functions of ADSI objects.</span></span> <span data-ttu-id="7a751-110">核心功能包括提供目錄存放區的進入點、將屬性載入屬性快取，以及認可基礎目錄的變更。</span><span class="sxs-lookup"><span data-stu-id="7a751-110">The core functions include providing an entry point into a directory store, loading properties into the property cache, and committing changes to the underlying directory.</span></span>
-   <span data-ttu-id="7a751-111">[架構](schema-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="7a751-111">[Schema](schema-interfaces.md).</span></span> <span data-ttu-id="7a751-112">這些介面提供管理和延伸目錄架構的方法。</span><span class="sxs-lookup"><span data-stu-id="7a751-112">These interfaces provide methods for managing and extending the directory schema.</span></span>
-   <span data-ttu-id="7a751-113">[屬性](property-cache-interfaces.md)快取。</span><span class="sxs-lookup"><span data-stu-id="7a751-113">[Property Cache](property-cache-interfaces.md).</span></span> <span data-ttu-id="7a751-114">這些介面會定義方法，以操作屬性快取中的屬性。</span><span class="sxs-lookup"><span data-stu-id="7a751-114">These interfaces define methods for manipulating properties in the property cache.</span></span>
-   <span data-ttu-id="7a751-115">[持續性物件](persistent-object-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="7a751-115">[Persistent Object](persistent-object-interfaces.md).</span></span> <span data-ttu-id="7a751-116">這些介面會操作基礎目錄服務的命名空間中的持續性資料。</span><span class="sxs-lookup"><span data-stu-id="7a751-116">These interfaces manipulate persistent data in the namespace of the underlying directory service.</span></span> <span data-ttu-id="7a751-117">ADSI 物件會執行這些類型的介面，以提供其持續性資料的存取權，包括使用者帳戶、檔案共用、組織階層和列印佇列中的作業清單。</span><span class="sxs-lookup"><span data-stu-id="7a751-117">ADSI objects implement these types of interfaces to provide access to their persistent data, including user accounts, file shares, organizational hierarchies, and job listings in a print queue.</span></span>
-   <span data-ttu-id="7a751-118">[動態物件](dynamic-object-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="7a751-118">[Dynamic Object](dynamic-object-interfaces.md).</span></span> <span data-ttu-id="7a751-119">這些介面會使用目錄服務中的動態資料。</span><span class="sxs-lookup"><span data-stu-id="7a751-119">These interfaces work with dynamic data in a directory service.</span></span> <span data-ttu-id="7a751-120">基礎目錄服務中未表示的目錄物件會執行這類介面。</span><span class="sxs-lookup"><span data-stu-id="7a751-120">Directory objects not represented in the underlying directory service implement such interfaces.</span></span> <span data-ttu-id="7a751-121">動態資料的範例包括透過網路發出的命令。</span><span class="sxs-lookup"><span data-stu-id="7a751-121">Examples of dynamic data include commands issued over a network.</span></span>
-   <span data-ttu-id="7a751-122">[安全性](security-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="7a751-122">[Security](security-interfaces.md).</span></span> <span data-ttu-id="7a751-123">這些介面可讓 ADSI 用戶端建立其認證給伺服器，並使用目錄服務所支援的安全性功能，例如存取控制清單或安全描述項。</span><span class="sxs-lookup"><span data-stu-id="7a751-123">These interfaces enable an ADSI client to establish its credentials to a server and use security features that the directory service supports, such as the access control list or security descriptors.</span></span>
-   <span data-ttu-id="7a751-124">[非自動化](non-automation-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="7a751-124">[Non-Automation](non-automation-interfaces.md).</span></span> <span data-ttu-id="7a751-125">這些介面允許非自動化用戶端 (例如，C/c + + 應用程式) 低額外負荷的目錄物件存取權，方法是提供 Vtable 存取方法來管理和搜尋目錄服務物件。</span><span class="sxs-lookup"><span data-stu-id="7a751-125">These interfaces allow non-Automation clients (for example, C/C++ applications) low-overhead access to directory objects by providing Vtable access to methods for managing and searching directory service objects.</span></span>
-   <span data-ttu-id="7a751-126">[延伸](extension-interfaces.md)模組。</span><span class="sxs-lookup"><span data-stu-id="7a751-126">[Extension](extension-interfaces.md).</span></span> <span data-ttu-id="7a751-127">這些介面可讓 ADSI 用戶端擴充現有 ADSI 類別的功能，為目錄服務提供自訂的解決方案。</span><span class="sxs-lookup"><span data-stu-id="7a751-127">These interfaces allow ADSI clients to extend the features of existing ADSI classes to offer customized solutions to directory services.</span></span>
-   <span data-ttu-id="7a751-128">[公用程式](utility-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="7a751-128">[Utility](utility-interfaces.md).</span></span> <span data-ttu-id="7a751-129">這些介面提供管理 ADSI 物件的 advanced helper 函數。</span><span class="sxs-lookup"><span data-stu-id="7a751-129">These interfaces provide advanced helper functions for managing ADSI objects.</span></span>
-   <span data-ttu-id="7a751-130">[資料類型](data-type-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="7a751-130">[Data Type](data-type-interfaces.md).</span></span> <span data-ttu-id="7a751-131">這些介面會提供存取 ADSI 資料類型的方法。</span><span class="sxs-lookup"><span data-stu-id="7a751-131">These interfaces provide methods to access ADSI data types.</span></span>

 

 




