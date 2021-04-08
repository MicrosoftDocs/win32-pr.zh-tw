---
title: 路由器資訊函式
description: 使用下列功能來操作路由器資訊標頭和區塊。 資訊標頭是由私用中繼資料和資訊區塊所組成。 資訊區塊是各種類型之資訊結構的陣列。
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f694d2dcd140d8af8950fa7a2a4ae5049a679ff8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020717"
---
# <a name="router-information-functions"></a><span data-ttu-id="2f8d1-105">路由器資訊函式</span><span class="sxs-lookup"><span data-stu-id="2f8d1-105">Router Information Functions</span></span>

<span data-ttu-id="2f8d1-106">使用下列功能來操作路由器資訊標頭和區塊。</span><span class="sxs-lookup"><span data-stu-id="2f8d1-106">Use the following functions to manipulate router information headers and blocks.</span></span> <span data-ttu-id="2f8d1-107">資訊標頭是由私用中繼資料和資訊區塊所組成。</span><span class="sxs-lookup"><span data-stu-id="2f8d1-107">An information header is composed of private meta-data and information blocks.</span></span> <span data-ttu-id="2f8d1-108">資訊區塊是各種[類型](router-information-enumerations.md)之[資訊結構](router-information-structures.md)的陣列。</span><span class="sxs-lookup"><span data-stu-id="2f8d1-108">Information blocks are arrays of [information structures](router-information-structures.md) of various [types](router-information-enumerations.md).</span></span>

<span data-ttu-id="2f8d1-109">下列函式會操作資訊標頭：</span><span class="sxs-lookup"><span data-stu-id="2f8d1-109">The following functions manipulate information headers:</span></span>

-   [<span data-ttu-id="2f8d1-110">**MprInfoCreate**</span><span class="sxs-lookup"><span data-stu-id="2f8d1-110">**MprInfoCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfocreate)
-   [<span data-ttu-id="2f8d1-111">**MprInfoDelete**</span><span class="sxs-lookup"><span data-stu-id="2f8d1-111">**MprInfoDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfodelete)
-   [<span data-ttu-id="2f8d1-112">**MprInfoDuplicate**</span><span class="sxs-lookup"><span data-stu-id="2f8d1-112">**MprInfoDuplicate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoduplicate)
-   [<span data-ttu-id="2f8d1-113">**MprInfoRemoveAll**</span><span class="sxs-lookup"><span data-stu-id="2f8d1-113">**MprInfoRemoveAll**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinforemoveall)

<span data-ttu-id="2f8d1-114">下列函式會操作資訊標頭中的資訊區塊：</span><span class="sxs-lookup"><span data-stu-id="2f8d1-114">The following functions manipulate information blocks within an information header:</span></span>

-   [<span data-ttu-id="2f8d1-115">**MprInfoBlockAdd**</span><span class="sxs-lookup"><span data-stu-id="2f8d1-115">**MprInfoBlockAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd)
-   [<span data-ttu-id="2f8d1-116">**MprInfoBlockFind**</span><span class="sxs-lookup"><span data-stu-id="2f8d1-116">**MprInfoBlockFind**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind)
-   [<span data-ttu-id="2f8d1-117">**MprInfoBlockQuerySize**</span><span class="sxs-lookup"><span data-stu-id="2f8d1-117">**MprInfoBlockQuerySize**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockquerysize)
-   [<span data-ttu-id="2f8d1-118">**MprInfoBlockRemove**</span><span class="sxs-lookup"><span data-stu-id="2f8d1-118">**MprInfoBlockRemove**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove)
-   [<span data-ttu-id="2f8d1-119">**MprInfoBlockSet**</span><span class="sxs-lookup"><span data-stu-id="2f8d1-119">**MprInfoBlockSet**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset)

<span data-ttu-id="2f8d1-120">許多 [路由器管理和設定函數](understanding-mprinfo-functions-and-information-headers.md) 都會使用資訊標頭。</span><span class="sxs-lookup"><span data-stu-id="2f8d1-120">Many of the [router administration and configuration functions](understanding-mprinfo-functions-and-information-headers.md) use information headers.</span></span>

 

 




