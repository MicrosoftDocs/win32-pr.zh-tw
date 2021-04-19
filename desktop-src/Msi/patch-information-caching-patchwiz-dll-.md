---
description: 產生新的修補程式可能需要很長的時間。
ms.assetid: 8be9a83a-8c36-43f5-8dda-05fc2f3ce0d2
title: '修補資訊快取 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7000efceea62e9eef122a34f7700622e1e6e2e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996648"
---
# <a name="patch-information-caching-patchwizdll"></a><span data-ttu-id="1136a-103">修補資訊快取 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="1136a-103">Patch Information Caching (Patchwiz.dll)</span></span>

<span data-ttu-id="1136a-104">產生新的修補程式可能需要很長的時間。</span><span class="sxs-lookup"><span data-stu-id="1136a-104">Generating a new patch may require significant time.</span></span> <span data-ttu-id="1136a-105">使用 [Patchwiz.dll](patchwiz-dll.md)產生修補程式之後，您可能需要再次變更更新映射，並產生另一個修補程式。</span><span class="sxs-lookup"><span data-stu-id="1136a-105">After you have generated a patch using [Patchwiz.dll](patchwiz-dll.md), you may need to change the update image again and generate another patch.</span></span> <span data-ttu-id="1136a-106">修補資訊快取可以藉由重複使用現有的修補程式，來減少產生後續修補程式所需的時間。</span><span class="sxs-lookup"><span data-stu-id="1136a-106">Patch information caching can reduce the time required to generate subsequent patches by reusing existing patches.</span></span> <span data-ttu-id="1136a-107">例如，您可以使用先前修補程式所產生的二進位修補程式，來減少建立 service pack 所需的時間。</span><span class="sxs-lookup"><span data-stu-id="1136a-107">For example, the time required to create service packs can be reduced by using the binary patches generated from previous patches.</span></span> <span data-ttu-id="1136a-108">Patchwiz.dll 可以使用 PATCH \_ CACHE \_ DIR 找出現有的二進位修補程式，並將它新增至 service pack 的封包，而不需要重新建立二進位修補程式。</span><span class="sxs-lookup"><span data-stu-id="1136a-108">Patchwiz.dll can use PATCH\_CACHE\_DIR to find an existing binary patch and add it to the service pack's cabinet without having to re-create the binary patch.</span></span>

<span data-ttu-id="1136a-109">修補資訊快取需要使用 [Patchwiz.dll](patchwiz-dll.md)。</span><span class="sxs-lookup"><span data-stu-id="1136a-109">Patch information caching requires the use of [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="1136a-110">若要啟動修補程式快取， \_ 請 \_ \_ \_ 在 pcp 檔案) 的 patch 建立 ( 屬性檔 [ (Patchwiz.dll) ](properties-table-patchwiz-dll-.md) 中，將 [已啟用修補快取] 和 [修補快取目錄] 屬性設定為 [內容] 資料表。</span><span class="sxs-lookup"><span data-stu-id="1136a-110">To activate patch caching, set the PATCH\_CACHE\_ENABLED and PATCH\_CACHE\_DIR properties in the [Properties Table (Patchwiz.dll)](properties-table-patchwiz-dll-.md) of the patch creation properties file (.pcp file).</span></span> <span data-ttu-id="1136a-111">Patchwiz 會將所有修補程式建立資訊儲存在 PATCH CACHE DIR 屬性所識別的資料夾中 \_ \_ ，並視需要建立此資料夾。</span><span class="sxs-lookup"><span data-stu-id="1136a-111">Patchwiz stores all patch creation information in the folder identified by the PATCH\_CACHE\_DIR property and creates this folder if necessary.</span></span> <span data-ttu-id="1136a-112">下次當您嘗試建立修補程式時，Patchwiz 會檢查此資料夾，以查看要比較的檔案是否符合快取中的檔案。</span><span class="sxs-lookup"><span data-stu-id="1136a-112">The next time you attempt to create a patch, Patchwiz checks this folder to see whether the files to be compared match the files in the cache.</span></span> <span data-ttu-id="1136a-113">如果檔案相符，Patchwiz 會使用快取的資訊，而不是重新產生檔案的二進位修補程式。</span><span class="sxs-lookup"><span data-stu-id="1136a-113">If the files match, Patchwiz uses the cached information rather than regenerating the binary patch for the file.</span></span> <span data-ttu-id="1136a-114">如果檔案不相符，或快取中缺少資訊，Patchwiz 會產生檔案的修補程式。</span><span class="sxs-lookup"><span data-stu-id="1136a-114">If the files do not match, or if the information is missing from the cache, Patchwiz generates the patch for the file.</span></span>

<span data-ttu-id="1136a-115">若要使用修補程式資訊快取， \_ 建立 .msp 檔之後，必須保留 patch CACHE DIR 所指定的資料夾 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1136a-115">To use patch information caching, the folder specified by PATCH\_CACHE\_DIR must be preserved after creating a .msp file.</span></span> <span data-ttu-id="1136a-116">如果刪除資料夾，PatchWiz 必須重新產生二進位修補程式，以取得後續的 .msp 檔案。</span><span class="sxs-lookup"><span data-stu-id="1136a-116">If the folder is deleted, PatchWiz has to re-generate binary patches for subsequent .msp files.</span></span> <span data-ttu-id="1136a-117">如需在目標檔案的選定區域中保留資訊的詳細資訊，請參閱 [修補檔案的選取區域](patching-selected-regions-of-a-file.md)。</span><span class="sxs-lookup"><span data-stu-id="1136a-117">For more information about preserving information in selected regions of a target file see [Patching Selected Regions of a File](patching-selected-regions-of-a-file.md).</span></span>

 

 



