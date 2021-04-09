---
description: 預設系統存放區（包括 MY、CA 和 ROOT）會實作為邏輯集合存放區，其中包含許多預先定義的實體存放區做為其成員存放區。
ms.assetid: 1d82b94b-4842-454a-aca4-823cd264ac52
title: 邏輯與實體存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a5441bac91e39b7f4c124daecd3a6a569c323c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690747"
---
# <a name="logical-and-physical-stores"></a><span data-ttu-id="5a110-103">邏輯與實體存放區</span><span class="sxs-lookup"><span data-stu-id="5a110-103">Logical and Physical Stores</span></span>

<span data-ttu-id="5a110-104">預設系統存放區（包括 MY、CA 和 ROOT）會實作為邏輯集合存放區，其中包含許多預先定義的實體存放區做為其成員存放區。</span><span class="sxs-lookup"><span data-stu-id="5a110-104">Default system stores, including MY, CA, and ROOT, are implemented as logical collection stores with a number of predefined physical stores as their member stores.</span></span> <span data-ttu-id="5a110-105">系統存放區的成員實體存放區會在系統存放區開啟時自動開啟。</span><span class="sxs-lookup"><span data-stu-id="5a110-105">The member physical stores of a system store are opened automatically when the system store is opened.</span></span> <span data-ttu-id="5a110-106">使用者可以在任何系統存放區集合中新增其他實體存放區。</span><span class="sxs-lookup"><span data-stu-id="5a110-106">A user can add additional physical stores to any system store collection.</span></span> <span data-ttu-id="5a110-107">CryptoAPI 函數 [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore) 會將新的實體存放區加入至系統存放區集合。</span><span class="sxs-lookup"><span data-stu-id="5a110-107">The CryptoAPI function [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore) adds a new physical store to a system store collection.</span></span> <span data-ttu-id="5a110-108">[**CertUnregisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore) 會解除實體存放區與邏輯系統存放區的之間的解除。</span><span class="sxs-lookup"><span data-stu-id="5a110-108">[**CertUnregisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore) disassociates a physical store from a logical system store.</span></span> <span data-ttu-id="5a110-109">[**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore) 會在登錄 hKey 下建立新的系統存放區，而 [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore) 會從登錄中移除系統存放區。</span><span class="sxs-lookup"><span data-stu-id="5a110-109">[**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore) creates a new system store under a registry hKey, while [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore) removes a system store from the registry.</span></span>

<span data-ttu-id="5a110-110">在 CryptoAPI 中，系統存放區是具有相關聯實體存放區的邏輯存放區。</span><span class="sxs-lookup"><span data-stu-id="5a110-110">In CryptoAPI, system stores are logical stores with associated physical stores.</span></span> <span data-ttu-id="5a110-111">現有系統存放區中的所有憑證都會保持可用，而實體新增憑證則是在組成邏輯系統存放區的實體存放區中進行。</span><span class="sxs-lookup"><span data-stu-id="5a110-111">All the certificates in an existing system store remain available, and the physical addition of new certificates is made in the physical stores that make up the logical system store.</span></span>

<span data-ttu-id="5a110-112">如果使用者想要繼續使用實體系統存放區，而不是轉換成邏輯存放區，則可以使用 CERT \_ STORE \_ >prov \_ system \_ REGISTRY provider 開啟系統存放區。</span><span class="sxs-lookup"><span data-stu-id="5a110-112">Users who prefer to continue to use physical system stores and not convert to logical stores can open system stores with the CERT\_STORE\_PROV\_SYSTEM\_REGISTRY provider.</span></span> <span data-ttu-id="5a110-113">此提供者會繼續使用每個系統存放區做為單一實體存放區。</span><span class="sxs-lookup"><span data-stu-id="5a110-113">This provider will continue to use each system store as a single, physical store.</span></span>

<span data-ttu-id="5a110-114">函式 [**CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation)、 [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)和 [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore) 清單系統存放區位置、可用的系統存放區，以及屬於系統存放區成員的所有實體存放區。</span><span class="sxs-lookup"><span data-stu-id="5a110-114">The functions [**CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation), [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore), and [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore) list system store locations, available system stores, and all physical stores that are members of a system store.</span></span>

<span data-ttu-id="5a110-115">系統存放區也可以重新置放。</span><span class="sxs-lookup"><span data-stu-id="5a110-115">System stores can also be relocated.</span></span> <span data-ttu-id="5a110-116">根據預設，系統會根據預先定義的模式，開啟相對於登錄子機碼的系統存放區。</span><span class="sxs-lookup"><span data-stu-id="5a110-116">By default, a system store is opened relative to a registry subkey following a predefined pattern.</span></span> <span data-ttu-id="5a110-117">如需詳細資訊，請參閱 [系統存放區位置](system-store-locations.md)。</span><span class="sxs-lookup"><span data-stu-id="5a110-117">For more information, see [System Store Locations](system-store-locations.md).</span></span> <span data-ttu-id="5a110-118">\_ \_ \_ \_ 在傳遞至 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)的 *dwFlags* 參數中設定 CERT 系統存放區位置旗標，會將系統存放區放在登錄中使用者指定的登錄子機碼下，而不是預先定義的登錄子機碼。</span><span class="sxs-lookup"><span data-stu-id="5a110-118">Setting CERT\_SYSTEM\_STORE\_RELOCATE\_FLAG in the *dwFlags* parameter passed to [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) places a system store in the registry under a user-specified registry subkey instead of the predefined one.</span></span>

 

 



