---
description: 網路監視器二進位大型物件 (BLOB) 是一般資料結構，其中包含網路介面卡 (Nic) 的設定和位置資訊。
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: 網路監視器 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce6dd6ca8643eabe8ab49387c0ef39eb49b6f2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985163"
---
# <a name="network-monitor-blobs"></a><span data-ttu-id="56689-103">網路監視器 Blob</span><span class="sxs-lookup"><span data-stu-id="56689-103">Network Monitor BLOBs</span></span>

<span data-ttu-id="56689-104">網路監視器二進位大型物件 (BLOB) 是一般資料結構，其中包含網路介面卡 (Nic) 的設定和位置資訊。</span><span class="sxs-lookup"><span data-stu-id="56689-104">The Network Monitor binary large object (BLOB) is a generic data structure that contains configuration and location information of network interface cards (NICs).</span></span> <span data-ttu-id="56689-105">使用 Blob 來代表 Nic，並篩選 Nic 清單中的專案。</span><span class="sxs-lookup"><span data-stu-id="56689-105">Use BLOBs to represent NICs and to filter entries in a list of NICs.</span></span> <span data-ttu-id="56689-106">BLOB 也可以包含應用程式特定的資料，而不會影響它們所保留的其他資料。</span><span class="sxs-lookup"><span data-stu-id="56689-106">BLOBS can also contain application-specific data without affecting the other data that they hold.</span></span> <span data-ttu-id="56689-107">BLOB 實作為所有必須使用 BLOB Api 存取 Blob 的層級不透明。</span><span class="sxs-lookup"><span data-stu-id="56689-107">BLOB implementation is opaque to all levels that must access BLOBs with BLOB APIs.</span></span>

## <a name="blob-structure"></a><span data-ttu-id="56689-108">BLOB 結構</span><span class="sxs-lookup"><span data-stu-id="56689-108">BLOB Structure</span></span>

<span data-ttu-id="56689-109">BLOB 可視為用來指定字串的階層式樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="56689-109">A BLOB can be considered as a hierarchical tree used to designate strings.</span></span> <span data-ttu-id="56689-110">此樹狀結構有三個層級：擁有者、類別和標記。</span><span class="sxs-lookup"><span data-stu-id="56689-110">This tree has three layers: Owner, Category, and Tag.</span></span> <span data-ttu-id="56689-111">擁有者是一種字串，通常表示讀取專案的物件。</span><span class="sxs-lookup"><span data-stu-id="56689-111">Owner is a string that indicates, in general, who reads an entry.</span></span> <span data-ttu-id="56689-112">此類別也是字串，它會指定擁有者底下的一般功能群組標記。</span><span class="sxs-lookup"><span data-stu-id="56689-112">The Category is also a string, which designates a general functional grouping of tags under the owner.</span></span> <span data-ttu-id="56689-113">標記是專案的實際名稱。</span><span class="sxs-lookup"><span data-stu-id="56689-113">The Tag is the actual name of the entry.</span></span>

<span data-ttu-id="56689-114">Blob 的結構化特性包括：</span><span class="sxs-lookup"><span data-stu-id="56689-114">The structural characteristics of BLOBs include:</span></span>

-   <span data-ttu-id="56689-115">一個進程內的 BLOB 協助程式會由每個 BLOB 內建的 mutex 彼此保護。</span><span class="sxs-lookup"><span data-stu-id="56689-115">BLOB helpers within one process are protected from one another by a mutex built into each BLOB.</span></span>
-   <span data-ttu-id="56689-116">每個 BLOB 都有內部版本號碼，讓協助專家可以處理目前和未來的 BLOB 表單。</span><span class="sxs-lookup"><span data-stu-id="56689-116">Each BLOB has an internal version number so that the helpers can handle both present and future BLOB forms.</span></span> <span data-ttu-id="56689-117">如果您透過遠端程序呼叫將 BLOB 傳送到另一部電腦，可能會發生版本衝突。</span><span class="sxs-lookup"><span data-stu-id="56689-117">Version conflicts may occur if you send a BLOB to another computer via a remote procedure call.</span></span>
-   <span data-ttu-id="56689-118">BLOB 本身是 void 的指標。</span><span class="sxs-lookup"><span data-stu-id="56689-118">The BLOB itself is a pointer to a void.</span></span> <span data-ttu-id="56689-119">請注意，應用程式應該使用 **const** 修飾詞來配置 blob，以避免變更內容。</span><span class="sxs-lookup"><span data-stu-id="56689-119">Be aware that applications should allocate BLOBs with the **const** modifier to avoid altering the contents.</span></span>
-   <span data-ttu-id="56689-120">每個指示項及其值都是字串。</span><span class="sxs-lookup"><span data-stu-id="56689-120">Each of the designators, as well as their values, are strings.</span></span> <span data-ttu-id="56689-121">請注意， **GetString** 函式所傳回的字串實際上是指向 BLOB 的指標，不應該變更。</span><span class="sxs-lookup"><span data-stu-id="56689-121">Be aware that the strings returned by **GetString** functions are actually pointers into the BLOB and should not be changed.</span></span> <span data-ttu-id="56689-122">基於這個理由，必須將這些字串指定為 **const char** _ \_ pX \*，讓應用程式不會意外變更它們。</span><span class="sxs-lookup"><span data-stu-id="56689-122">For this reason, these strings must be specified as **const char** _\_pX\* to keep applications from accidentally changing them.</span></span>

<span data-ttu-id="56689-123">一般情況下，所有具有 **const** 指示項的參數都鼓勵呼叫端避免變更值，而不是禁止 helper 函式變更它們。</span><span class="sxs-lookup"><span data-stu-id="56689-123">In general, all parameters with the **const** designator encourage the caller to refrain from changing the values rather than prohibit the helper functions from changing them.</span></span> <span data-ttu-id="56689-124">事實上，helper 函數通常會變更這些值。</span><span class="sxs-lookup"><span data-stu-id="56689-124">In fact, the helper functions will usually change those values.</span></span>

 

 



