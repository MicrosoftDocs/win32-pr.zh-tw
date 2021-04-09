---
title: ADSI 如何整合延伸模組
description: 描述 ADSI 如何與延伸模組互動的指導方針。
ms.assetid: 00301551-ec56-4cb4-8e77-264c3ad48814
ms.tgt_platform: multiple
keywords:
- 擴充功能 ADSI
- adsi 和延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956a76954851ea54b4eae99bfa45102a3b2fefa5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024089"
---
# <a name="how-adsi-integrates-extensions"></a><span data-ttu-id="ba165-105">ADSI 如何整合延伸模組</span><span class="sxs-lookup"><span data-stu-id="ba165-105">How ADSI Integrates Extensions</span></span>

<span data-ttu-id="ba165-106">下列指導方針說明 ADSI 如何與延伸模組互動：</span><span class="sxs-lookup"><span data-stu-id="ba165-106">The following guidelines describe how ADSI interacts with extensions:</span></span>

-   <span data-ttu-id="ba165-107">某些系結至 ADSI 目錄物件。</span><span class="sxs-lookup"><span data-stu-id="ba165-107">Something binds to an ADSI directory object.</span></span> <span data-ttu-id="ba165-108">例如，"LDAP：//CN = JeffSmith，OU = Sales，DC = Fabrikam，DC = COM"。</span><span class="sxs-lookup"><span data-stu-id="ba165-108">For example, "LDAP://CN=JeffSmith,OU=Sales,DC=Fabrikam,DC=COM".</span></span>
-   <span data-ttu-id="ba165-109">ADSI 可識別物件位於 **使用者** 類別中。</span><span class="sxs-lookup"><span data-stu-id="ba165-109">ADSI identifies that the object is in the **user** class.</span></span>
-   <span data-ttu-id="ba165-110">ADSI 會在登錄中執行查閱，並識別 **使用者** 的延伸 clsid。</span><span class="sxs-lookup"><span data-stu-id="ba165-110">ADSI performs a lookup in the registry and identifies the extension CLSIDs for **user**.</span></span> <span data-ttu-id="ba165-111">請注意，ADSI 會快取此資料。</span><span class="sxs-lookup"><span data-stu-id="ba165-111">Be aware that ADSI caches this data.</span></span>
-   <span data-ttu-id="ba165-112">它會針對 IID IMyExtension 呼叫 **QueryInterface** 方法 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ba165-112">Something calls the **QueryInterface** method for IID\_IMyExtension.</span></span> <span data-ttu-id="ba165-113">ADSI 會搜尋與 **使用者** 物件相關聯的介面，從自己的介面開始，然後查看延伸模組介面。</span><span class="sxs-lookup"><span data-stu-id="ba165-113">ADSI searches the interfaces associated with the **user** object, starting with its own interfaces, then looking at extension interfaces.</span></span>
-   <span data-ttu-id="ba165-114">如果找到相符的，ADSI 會建立支援 IID IMyExtension 的元件實例 \_ ，並呼叫此延伸模組的 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="ba165-114">If a match is found, ADSI creates an instance of the component that supports IID\_IMyExtension, and calls **QueryInterface** for the extension.</span></span> <span data-ttu-id="ba165-115">會傳回產生的介面。</span><span class="sxs-lookup"><span data-stu-id="ba165-115">The resulting interface is returned.</span></span>
-   <span data-ttu-id="ba165-116">使用者會使用此介面來呼叫介面方法。</span><span class="sxs-lookup"><span data-stu-id="ba165-116">The user uses this interface to call the interface methods.</span></span>
-   <span data-ttu-id="ba165-117">接下來，用戶端會呼叫 IYourExtension 的 **QueryInterface** \_ ，這是在不同的元件中。</span><span class="sxs-lookup"><span data-stu-id="ba165-117">Next, the client calls **QueryInterface** for IID\_IYourExtension, which is in a different component.</span></span> <span data-ttu-id="ba165-118">這個元件會將這個 **QueryInterface** 呼叫委派給匯總工具的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面，這個介面剛好是 ADSI 本身。</span><span class="sxs-lookup"><span data-stu-id="ba165-118">This component delegates this **QueryInterface** call to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the aggregator, which happens to be ADSI itself.</span></span>
-   <span data-ttu-id="ba165-119">同樣地，ADSI 會搜尋介面並建立元件實例。</span><span class="sxs-lookup"><span data-stu-id="ba165-119">Again, ADSI searches the interfaces and creates the component instance.</span></span>

 

 