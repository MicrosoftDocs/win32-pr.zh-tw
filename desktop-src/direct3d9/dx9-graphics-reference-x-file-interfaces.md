---
description: 本節包含用來讀取和寫入 DirectX. x 檔案的 COM 介面參考資訊。 已取代。
ms.assetid: 66e3476a-4ee8-48ac-aab8-6653793e0ef3
title: X 檔案介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6e47325a4912faeb919cb60571de3cccbbe265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510145"
---
# <a name="x-file-interfaces"></a><span data-ttu-id="38ded-104">X 檔案介面</span><span class="sxs-lookup"><span data-stu-id="38ded-104">X File Interfaces</span></span>

<span data-ttu-id="38ded-105">本節包含用來讀取和寫入 DirectX. x 檔案的 COM 介面參考資訊。</span><span class="sxs-lookup"><span data-stu-id="38ded-105">This section contains reference information for the COM interfaces used to read to and write from DirectX .x files.</span></span> <span data-ttu-id="38ded-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="38ded-106">Deprecated.</span></span>

-   [<span data-ttu-id="38ded-107">**IDirectXFile**</span><span class="sxs-lookup"><span data-stu-id="38ded-107">**IDirectXFile**</span></span>](idirectxfile.md)
-   [<span data-ttu-id="38ded-108">**IDirectXFileBinary**</span><span class="sxs-lookup"><span data-stu-id="38ded-108">**IDirectXFileBinary**</span></span>](idirectxfilebinary.md)
-   [<span data-ttu-id="38ded-109">**IDirectXFileData**</span><span class="sxs-lookup"><span data-stu-id="38ded-109">**IDirectXFileData**</span></span>](idirectxfiledata.md)
-   [<span data-ttu-id="38ded-110">**IDirectXFileDataReference**</span><span class="sxs-lookup"><span data-stu-id="38ded-110">**IDirectXFileDataReference**</span></span>](idirectxfiledatareference.md)
-   [<span data-ttu-id="38ded-111">**IDirectXFileEnumObject**</span><span class="sxs-lookup"><span data-stu-id="38ded-111">**IDirectXFileEnumObject**</span></span>](idirectxfileenumobject.md)
-   [<span data-ttu-id="38ded-112">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="38ded-112">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
-   [<span data-ttu-id="38ded-113">**IDirectXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="38ded-113">**IDirectXFileSaveObject**</span></span>](idirectxfilesaveobject.md)

<span data-ttu-id="38ded-114">下表說明. x 檔案介面之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="38ded-114">The following tables illustrate the relationship between the .x file interfaces.</span></span>



| <span data-ttu-id="38ded-115">介面</span><span class="sxs-lookup"><span data-stu-id="38ded-115">Interface</span></span>             | <span data-ttu-id="38ded-116">來自</span><span class="sxs-lookup"><span data-stu-id="38ded-116">Derives from</span></span>           | <span data-ttu-id="38ded-117">來自</span><span class="sxs-lookup"><span data-stu-id="38ded-117">Derives from</span></span> |
|-----------------------|------------------------|--------------|
|                       | <span data-ttu-id="38ded-118">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="38ded-118">IDirectXFile</span></span>           | <span data-ttu-id="38ded-119">IUnknown</span><span class="sxs-lookup"><span data-stu-id="38ded-119">IUnknown</span></span>     |
| <span data-ttu-id="38ded-120">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="38ded-120">IDirectXFileBinary</span></span>    | <span data-ttu-id="38ded-121">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="38ded-121">IDirectXFileObject</span></span>     | <span data-ttu-id="38ded-122">IUnknown</span><span class="sxs-lookup"><span data-stu-id="38ded-122">IUnknown</span></span>     |
| <span data-ttu-id="38ded-123">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="38ded-123">IDirectXFileData</span></span>      | <span data-ttu-id="38ded-124">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="38ded-124">IDirectXFileObject</span></span>     | <span data-ttu-id="38ded-125">IUnknown</span><span class="sxs-lookup"><span data-stu-id="38ded-125">IUnknown</span></span>     |
| <span data-ttu-id="38ded-126">IDirectXFileReference</span><span class="sxs-lookup"><span data-stu-id="38ded-126">IDirectXFileReference</span></span> | <span data-ttu-id="38ded-127">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="38ded-127">IDirectXFileObject</span></span>     | <span data-ttu-id="38ded-128">IUnknown</span><span class="sxs-lookup"><span data-stu-id="38ded-128">IUnknown</span></span>     |
|                       | <span data-ttu-id="38ded-129">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="38ded-129">IDirectXFileSaveObject</span></span> | <span data-ttu-id="38ded-130">IUnknown</span><span class="sxs-lookup"><span data-stu-id="38ded-130">IUnknown</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="38ded-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="38ded-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38ded-132"> (舊版) 的 X 檔案參考 </span><span class="sxs-lookup"><span data-stu-id="38ded-132">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



