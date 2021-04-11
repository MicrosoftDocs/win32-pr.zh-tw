---
description: PATCHWIZ.DLL Windows Installer&160 版發行的版本， \# 3.0 可以自動產生修補程式順序資訊，並將新的修補程式新增至 MsiPatchSequence 資料表。
ms.assetid: 03e7eea6-1a37-4c86-a9da-109fbaf20728
title: " (PATCHWIZ.DLL) 產生修補程式順序資訊"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff82166f33266a58cd3ef299b2546b04a94ebb14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944544"
---
# <a name="generating-patch-sequence-information-patchwizdll"></a><span data-ttu-id="502c7-103"> (PATCHWIZ.DLL) 產生修補程式順序資訊</span><span class="sxs-lookup"><span data-stu-id="502c7-103">Generating Patch Sequence Information (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="502c7-104">使用 Windows Installer 3.0 發行的 [PATCHWIZ.DLL](patchwiz-dll.md) 版本可以自動產生修補程式順序資訊，並將新的修補程式新增至 [MsiPatchSequence 資料表](msipatchsequence-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="502c7-104">The version of [PATCHWIZ.DLL](patchwiz-dll.md) released with Windows Installer 3.0 can automatically generate patch sequencing information and add to the [MsiPatchSequence Table](msipatchsequence-table.md) a new patch.</span></span>

<span data-ttu-id="502c7-105">在 pcp 檔案 \_ 的 [屬性] 資料表中，將 [將資料 \_ 產生 \_ 停用順序] 屬性設定為 1 (一個) ，以防止自動產生修補程式排序資訊。 [](properties-table-patchwiz-dll-.md)</span><span class="sxs-lookup"><span data-stu-id="502c7-105">Set the SEQUENCE\_DATA\_GENERATION\_DISABLED property to 1 (one) in the [Properties Table](properties-table-patchwiz-dll-.md) of the .pcp file to prevent the automatic generation of patch sequencing information.</span></span> <span data-ttu-id="502c7-106">如果這個屬性不存在，則會自動產生和新增資訊。</span><span class="sxs-lookup"><span data-stu-id="502c7-106">If this property is absent, the information is automatically generated and added.</span></span>

<span data-ttu-id="502c7-107">使用 Windows Installer 3.0 發行的 [PATCHWIZ.DLL](patchwiz-dll.md) 用來自動產生修補程式排序資訊時，會發生下列情況：</span><span class="sxs-lookup"><span data-stu-id="502c7-107">When the [PATCHWIZ.DLL](patchwiz-dll.md) released with Windows Installer 3.0 is used to automatically generate the patch sequencing information, the following occurs:</span></span>

-   <span data-ttu-id="502c7-108">針對[TargetImages 資料表](targetimages-table-patchwiz-dll-.md)中所列之目標影像的每個產品代碼，會將新的資料列新增至[MsiPatchSequence 資料表](msipatchsequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="502c7-108">A new row is added to the [MsiPatchSequence Table](msipatchsequence-table.md) for each product code of a target image that is listed in the [TargetImages Table](targetimages-table-patchwiz-dll-.md).</span></span>
-   <span data-ttu-id="502c7-109">在新資料列中加入至 PatchFamily 資料行的值，會對應到 [TargetImages 資料表](targetimages-table-patchwiz-dll-.md)中所列之目標影像的目標產品代碼。</span><span class="sxs-lookup"><span data-stu-id="502c7-109">The values added to the PatchFamily column in the new rows correspond to the target product codes of the target images that are listed in the [TargetImages Table](targetimages-table-patchwiz-dll-.md).</span></span>
-   <span data-ttu-id="502c7-110">在新資料列中加入順序資料行的值，會使用 patch 的目標最高產品版本和產生 patch 的 UTC 時間產生。</span><span class="sxs-lookup"><span data-stu-id="502c7-110">The values added to the Sequence columns in the new rows are generated using the highest product version targeted by the patch and the UTC time when the patch is generated.</span></span> <span data-ttu-id="502c7-111">序號為 <Product Minor Version> 。 <Build Major Number><時間戳記 1>。 <時間戳記 2>。</span><span class="sxs-lookup"><span data-stu-id="502c7-111">The sequence number is <Product Minor Version>.<Build Major Number>.<Time Stamp 1>.<Time Stamp 2>.</span></span>
    -   <span data-ttu-id="502c7-112">第一個欄位是修補程式設為目標之最高版本產品的產品版本。</span><span class="sxs-lookup"><span data-stu-id="502c7-112">The first field is the product version of the highest version of the product that is targeted by the patch.</span></span>
    -   <span data-ttu-id="502c7-113">第二個欄位是修補程式設為目標之最高版本產品的組建主要編號。</span><span class="sxs-lookup"><span data-stu-id="502c7-113">The second field is the build major number of the highest version of the product that is targeted by the patch.</span></span>

    <span data-ttu-id="502c7-114">這兩個時間戳記欄位會用於計算國際標準時間 (UTC) 的秒數所需的32位時間戳記。</span><span class="sxs-lookup"><span data-stu-id="502c7-114">The two time stamp fields account for the 32 bit time stamp that is needed to count the seconds in Coordinated Universal Time (UTC).</span></span>
    > [!Note]  
    > <span data-ttu-id="502c7-115">產品版本的格式如下： <Product Major Version> ... <Product Minor Version> <Build Major Number> <Build Minor Number> ，而且版本號碼為2.1.0.0 的產品版本比產品版本號碼更高1.2.0。0</span><span class="sxs-lookup"><span data-stu-id="502c7-115">Product versions have the following format: <Product Major Version>.<Product Minor Version>.<Build Major Number>.<Build Minor Number> and a product with a version number 2.1.0.0 is a higher version than a product with version number 1.2.0.0</span></span>

     

-   <span data-ttu-id="502c7-116">MsidbPatchSequenceSupersedeEarlier 屬性會輸入至為 service pack (SP) 或次要升級修補程式所產生的新資料列之 [屬性] 資料行中。</span><span class="sxs-lookup"><span data-stu-id="502c7-116">The msidbPatchSequenceSupersedeEarlier attribute is entered into the Attribute column of new rows that are generated for service packs (SP) or minor upgrade patches.</span></span> <span data-ttu-id="502c7-117">MsidbPatchSequenceSupersedeEarlier 屬性不會加入至 QFE 或小型更新修補程式。</span><span class="sxs-lookup"><span data-stu-id="502c7-117">The msidbPatchSequenceSupersedeEarlier attribute is not added to a QFE or small update patch.</span></span>
    > [!Note]  
    > <span data-ttu-id="502c7-118"> (SP) 的 service pack 應該包含之前發行的所有 Qfe 的修正程式。</span><span class="sxs-lookup"><span data-stu-id="502c7-118">A service pack (SP) should contain the fixes of all the QFEs that were released prior to it.</span></span> <span data-ttu-id="502c7-119">但是，如果 patch author 將 [順序 \_ 資料 \_ 取代] 屬性設定為 0 (零) 或 1 (pcp 檔案中的一個) ，則 MsiPatchSequence 資料表中所有資料列的 [屬性] 資料行會設定為 [順序資料取代] 所指定的值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="502c7-119">However, if a patch author sets the SEQUENCE\_DATA\_SUPERSEDENCE property to 0 (zero) or 1 (one) in the .pcp file, the Attributes column of all rows in the MsiPatchSequence table is set to the value that is specified for SEQUENCE\_DATA\_SUPERSEDENCE.</span></span> <span data-ttu-id="502c7-120">需要更多控制的修補程式作者必須手動撰寫 [屬性] 資料行。</span><span class="sxs-lookup"><span data-stu-id="502c7-120">Patch authors who require more control must author the Attributes column manually.</span></span>

     

<span data-ttu-id="502c7-121">如果您在 pcp 檔案中包含 [PatchSequence 資料表](patchsequence-table--patchwiz-dll-.md) ，則 \_ 會忽略 [順序資料 \_ 產生 \_ 已停用] 屬性，並將 PatchSequence 資料表中提供的資訊新增至 patch 的 [MsiPatchSequence 資料表](msipatchsequence-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="502c7-121">If you include a [PatchSequence Table](patchsequence-table--patchwiz-dll-.md) in the .pcp file, the SEQUENCE\_DATA\_GENERATION\_DISABLED property is ignored and the information provided in the PatchSequence Table can be added to the [MsiPatchSequence Table](msipatchsequence-table.md) of the patch.</span></span>

 

 



