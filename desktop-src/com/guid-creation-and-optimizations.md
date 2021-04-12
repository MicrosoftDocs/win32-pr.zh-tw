---
title: 建立和優化 GUID
description: 建立和優化 GUID
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc113675bae329d862c0b504851d4732243a84c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372587"
---
# <a name="guid-creation-and-optimizations"></a><span data-ttu-id="53413-103">建立和優化 GUID</span><span class="sxs-lookup"><span data-stu-id="53413-103">GUID Creation and Optimizations</span></span>

<span data-ttu-id="53413-104">因為 CLSID （例如 (IID) 的介面識別碼）是 GUID，所以沒有其他類別，無論誰寫入，都有重複的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="53413-104">Because a CLSID, like an interface identifier (IID), is a GUID, no other class, no matter who writes it, has a duplicate CLSID.</span></span> <span data-ttu-id="53413-105">伺服器實作者通常會透過 [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) 函數取得 clsid。</span><span class="sxs-lookup"><span data-stu-id="53413-105">Server implementers generally obtain CLSIDs through the [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) function.</span></span> <span data-ttu-id="53413-106">這項功能保證會產生獨特的 Clsid，因此全球的伺服器實施者可以獨立開發和部署其軟體，而不會干擾其他人所撰寫的軟體。</span><span class="sxs-lookup"><span data-stu-id="53413-106">This function is guaranteed to produce unique CLSIDs, so server implementers across the world can independently develop and deploy their software without fear of accidental collision with software written by others.</span></span>

<span data-ttu-id="53413-107">使用唯一的 Clsid 可避免類別之間發生名稱衝突的可能性，因為 Clsid 無法連接到基礎執行中使用的名稱。</span><span class="sxs-lookup"><span data-stu-id="53413-107">Using unique CLSIDs avoids the possibility of name collisions among classes because CLSIDs are in no way connected to the names used in the underlying implementation.</span></span> <span data-ttu-id="53413-108">例如，兩個不同的廠商可以撰寫稱為 "StackClass" 的類別，但每個都有唯一的 CLSID，因此不會混淆。</span><span class="sxs-lookup"><span data-stu-id="53413-108">For example, two different vendors can write classes called "StackClass," but each would have a unique CLSID and therefore could not be confused.</span></span>

<span data-ttu-id="53413-109">COM 經常必須將 Guid (Iid 和 Clsid) 對應至某些任意大型的其他值集。</span><span class="sxs-lookup"><span data-stu-id="53413-109">COM frequently must map GUIDs (IIDs and CLSIDs) to some arbitrarily large set of other values.</span></span> <span data-ttu-id="53413-110">作為應用程式開發人員，您可以藉由將應用程式的 Guid 產生為連續值的區塊，以協助加速這類搜尋，進而提升系統效能。</span><span class="sxs-lookup"><span data-stu-id="53413-110">As an application developer, you can help speed up such searches, and thereby enhance system performance, by generating the GUIDs for your application as a block of consecutive values.</span></span>

<span data-ttu-id="53413-111">產生連續 Guid 區塊最有效率的方法，是使用-n 和-x 參數來執行 uuidgen.exe 公用程式，這會產生一個 Uuid 區塊，其中每一個都是由其第一個 DWORD 值遞增。</span><span class="sxs-lookup"><span data-stu-id="53413-111">The most efficient way to generate a block of consecutive GUIDs is to run the uuidgen utility using the -n and -x switches, which generates a block of UUIDs, each of whose first DWORD value is incremented by one.</span></span>

<span data-ttu-id="53413-112">例如，如果您要輸入</span><span class="sxs-lookup"><span data-stu-id="53413-112">For example, if you were to type</span></span>

<span data-ttu-id="53413-113">**uuidgen.exe-n5-x**</span><span class="sxs-lookup"><span data-stu-id="53413-113">**uuidgen -n5 -x**</span></span>

<span data-ttu-id="53413-114">uuidgen.exe 公用程式會產生類似下列的 Uuid 區塊：</span><span class="sxs-lookup"><span data-stu-id="53413-114">the uuidgen utility would generate a block of UUIDs similar to the following:</span></span>

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

<span data-ttu-id="53413-115">針對整個專案產生和追蹤 Guid 的一個方法，一開始會產生一些任意數目的 Uuid，例如500。</span><span class="sxs-lookup"><span data-stu-id="53413-115">One method for generating and tracking GUIDs for an entire project begins with generating a block of some arbitrarily large number of UUIDs, say 500.</span></span> <span data-ttu-id="53413-116">例如，如果您要輸入</span><span class="sxs-lookup"><span data-stu-id="53413-116">For example, if you were to type</span></span>

<span data-ttu-id="53413-117">**uuidgen.exe-n500-x > guids.txt**</span><span class="sxs-lookup"><span data-stu-id="53413-117">**uuidgen -n500 -x > guids.txt**</span></span>

<span data-ttu-id="53413-118">公用程式會產生500個連續的 Uuid，並將它們寫入指定的文字檔。</span><span class="sxs-lookup"><span data-stu-id="53413-118">the utility would generate 500 consecutive UUIDs and write them to the specified text file.</span></span> <span data-ttu-id="53413-119">然後，您可以將此檔案簽入您的來源樹狀結構中，為專案中使用的所有 Guid 提供單一存放庫。</span><span class="sxs-lookup"><span data-stu-id="53413-119">You could then check this file into your source tree, providing a single repository for all GUIDs to be used in a project.</span></span> <span data-ttu-id="53413-120">當人們要求專案的部分需要 Guid 時，他們就可以簽出檔案，但需要有許多需要的 Guid，將它們標示為已使用，並在程式碼或「規格」中使用它們的位置留下附注。</span><span class="sxs-lookup"><span data-stu-id="53413-120">As people require GUIDs for their portions of the project, they can check out the file, take however many GUIDs they need, marking them as taken and leaving a note about where in the code or "spec" they are using them.</span></span>

<span data-ttu-id="53413-121">除了改善系統效能，以這種方式產生連續 Guid 區塊的優點如下：</span><span class="sxs-lookup"><span data-stu-id="53413-121">In addition to improving system performance, generating blocks of consecutive GUIDs in this way has the following benefits:</span></span>

-   <span data-ttu-id="53413-122">中央檔案包含應用程式的所有 Guid，可讓您輕鬆追蹤哪些 Guid 適用于哪些 Guid 以及哪些使用者正在使用它們。</span><span class="sxs-lookup"><span data-stu-id="53413-122">A central file containing all GUIDs for an application makes it easy to keep track of which GUIDs are for what and which people are using them.</span></span>
-   <span data-ttu-id="53413-123">與特定應用程式相關聯的連續 Guid 區塊，可協助開發人員和測試人員在偵錯工具期間辨識內部 Guid，並讓您更輕鬆地在系統登錄中找到它們，因為它們會依序儲存。</span><span class="sxs-lookup"><span data-stu-id="53413-123">A block of consecutive GUIDs associated with a particular application helps developers and testers recognize internal GUIDs during debugging and makes it easier to find them in the system registry because they are stored sequentially.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53413-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="53413-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53413-125">COM 伺服器責任</span><span class="sxs-lookup"><span data-stu-id="53413-125">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> </dl>

 

 




