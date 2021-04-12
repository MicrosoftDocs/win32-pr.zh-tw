---
title: 在幕後進行的晚期繫結
description: 本主題說明在 ADSI 中晚期繫結的運作方式。
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- 延伸模組 ADSI、晚期繫結、幕後的進展
- binding AD，晚期繫結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299b715325e4eda88a0eeaca2b22b4bdaa15a96
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463700"
---
# <a name="late-binding-whats-happening-under-the-hood"></a><span data-ttu-id="7d62a-105">晚期繫結：幕後有什麼進展？</span><span class="sxs-lookup"><span data-stu-id="7d62a-105">Late Binding: What's Happening Under the Hood?</span></span>

<span data-ttu-id="7d62a-106">下列清單概述執行晚期繫結的一般程式：</span><span class="sxs-lookup"><span data-stu-id="7d62a-106">The following list outlines the general process for performing a late bind:</span></span>

-   <span data-ttu-id="7d62a-107">某些系結至 ADSI 目錄物件。</span><span class="sxs-lookup"><span data-stu-id="7d62a-107">Something binds to an ADSI directory object.</span></span> <span data-ttu-id="7d62a-108">例如，"LDAP：//CN = Jeffsmith，OU = Sales，DC = Fabrikam，DC = COM" 使用 COM 晚期繫結來系結。</span><span class="sxs-lookup"><span data-stu-id="7d62a-108">For example, "LDAP://CN=Jeffsmith,OU=Sales,DC=Fabrikam,DC=COM" binds using COM late binding.</span></span> <span data-ttu-id="7d62a-109">這會導致 ADSI 在 **IDispatch** 介面上呼叫 [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch)方法。</span><span class="sxs-lookup"><span data-stu-id="7d62a-109">This causes ADSI to call the [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) method on the **IDispatch** interface.</span></span>
-   <span data-ttu-id="7d62a-110">ADSI 會在使用者類別中尋找物件，並建立支援適當介面的物件，例如 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)、 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)。</span><span class="sxs-lookup"><span data-stu-id="7d62a-110">ADSI finds an object in the user class and creates an object that supports the appropriate interfaces, such as [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).</span></span>
-   <span data-ttu-id="7d62a-111">ADSI 會在登錄中執行查閱，並尋找使用者的延伸 Clsid。</span><span class="sxs-lookup"><span data-stu-id="7d62a-111">ADSI performs a lookup in the registry and finds extension CLSIDs for user.</span></span> <span data-ttu-id="7d62a-112">請注意，ADSI 會快取此資料。</span><span class="sxs-lookup"><span data-stu-id="7d62a-112">Be aware that ADSI caches this data.</span></span>
-   <span data-ttu-id="7d62a-113">它會呼叫 **MyNewMethod** 方法。</span><span class="sxs-lookup"><span data-stu-id="7d62a-113">Something makes a call to the **MyNewMethod** method.</span></span> <span data-ttu-id="7d62a-114">ADSI 會查閱其分派識別碼和其他 ADSI 擴充功能的分派識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d62a-114">ADSI looks up its dispatch ID and the dispatch IDs for other ADSI extensions.</span></span> <span data-ttu-id="7d62a-115">ADSI 接著會尋找提供此呼叫的延伸模組，並呼叫該擴充功能的 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) 介面。</span><span class="sxs-lookup"><span data-stu-id="7d62a-115">ADSI then finds the extension that serves this call, and calls the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for that extension.</span></span>
-   <span data-ttu-id="7d62a-116">擴充功能會執行函式。</span><span class="sxs-lookup"><span data-stu-id="7d62a-116">The extension executes the function.</span></span>
-   <span data-ttu-id="7d62a-117">現在，用戶端寫入器會使用目前延伸模組的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面叫用 **YourNewMethod** 方法。</span><span class="sxs-lookup"><span data-stu-id="7d62a-117">Now, the client writer invokes the **YourNewMethod** method using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface for the current extension.</span></span> <span data-ttu-id="7d62a-118">延伸模組的 **idispatch** 執行會委派回 **idispatch** for ADSI。</span><span class="sxs-lookup"><span data-stu-id="7d62a-118">The extension's **IDispatch** implementation delegates back to the **IDispatch** for ADSI.</span></span>
-   <span data-ttu-id="7d62a-119">[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)會再次搜尋適當的副檔名或本身，然後使用該延伸模組的 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)介面呼叫適當的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="7d62a-119">The [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) for ADSI again searches for the appropriate extension, or itself, then it calls the appropriate extension using the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for that extension.</span></span>

 

 