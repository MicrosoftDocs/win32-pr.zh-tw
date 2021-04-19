---
description: 本節包含用來讀取和寫入自. x 檔案的 COM 介面參考資訊。
ms.assetid: 54d8a02b-5376-49ac-a0d5-fc3cd8ab82e6
title: D3DX X 檔案介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c460a57435eee8844776b73f362c981c716d820e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972108"
---
# <a name="d3dx-x-file-interfaces"></a><span data-ttu-id="c6b1c-103">D3DX X 檔案介面</span><span class="sxs-lookup"><span data-stu-id="c6b1c-103">D3DX X File Interfaces</span></span>

<span data-ttu-id="c6b1c-104">本節包含用來讀取和寫入自. x 檔案的 COM 介面參考資訊。</span><span class="sxs-lookup"><span data-stu-id="c6b1c-104">This section contains reference information for the COM interfaces used to read to and write from .x files.</span></span>

-   [<span data-ttu-id="c6b1c-105">**ID3DXFile**</span><span class="sxs-lookup"><span data-stu-id="c6b1c-105">**ID3DXFile**</span></span>](id3dxfile.md)
-   [<span data-ttu-id="c6b1c-106">**ID3DXFileData**</span><span class="sxs-lookup"><span data-stu-id="c6b1c-106">**ID3DXFileData**</span></span>](id3dxfiledata.md)
-   [<span data-ttu-id="c6b1c-107">**ID3DXFileEnumObject**</span><span class="sxs-lookup"><span data-stu-id="c6b1c-107">**ID3DXFileEnumObject**</span></span>](id3dxfileenumobject.md)
-   [<span data-ttu-id="c6b1c-108">**ID3DXFileSaveData**</span><span class="sxs-lookup"><span data-stu-id="c6b1c-108">**ID3DXFileSaveData**</span></span>](id3dxfilesavedata.md)
-   [<span data-ttu-id="c6b1c-109">**ID3DXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="c6b1c-109">**ID3DXFileSaveObject**</span></span>](id3dxfilesaveobject.md)

<span data-ttu-id="c6b1c-110">下表說明. x 檔案介面之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="c6b1c-110">The following tables illustrate the relationship between the .x file interfaces.</span></span>



| <span data-ttu-id="c6b1c-111">介面</span><span class="sxs-lookup"><span data-stu-id="c6b1c-111">Interface</span></span>             | <span data-ttu-id="c6b1c-112">來自</span><span class="sxs-lookup"><span data-stu-id="c6b1c-112">Derives from</span></span>           | <span data-ttu-id="c6b1c-113">來自</span><span class="sxs-lookup"><span data-stu-id="c6b1c-113">Derives from</span></span> |
|-----------------------|------------------------|--------------|
|                       | <span data-ttu-id="c6b1c-114">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="c6b1c-114">IDirectXFile</span></span>           | <span data-ttu-id="c6b1c-115">IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6b1c-115">IUnknown</span></span>     |
| <span data-ttu-id="c6b1c-116">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="c6b1c-116">IDirectXFileBinary</span></span>    | <span data-ttu-id="c6b1c-117">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="c6b1c-117">IDirectXFileObject</span></span>     | <span data-ttu-id="c6b1c-118">IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6b1c-118">IUnknown</span></span>     |
| <span data-ttu-id="c6b1c-119">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="c6b1c-119">IDirectXFileData</span></span>      | <span data-ttu-id="c6b1c-120">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="c6b1c-120">IDirectXFileObject</span></span>     | <span data-ttu-id="c6b1c-121">IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6b1c-121">IUnknown</span></span>     |
| <span data-ttu-id="c6b1c-122">IDirectXFileReference</span><span class="sxs-lookup"><span data-stu-id="c6b1c-122">IDirectXFileReference</span></span> | <span data-ttu-id="c6b1c-123">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="c6b1c-123">IDirectXFileObject</span></span>     | <span data-ttu-id="c6b1c-124">IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6b1c-124">IUnknown</span></span>     |
|                       | <span data-ttu-id="c6b1c-125">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="c6b1c-125">IDirectXFileSaveObject</span></span> | <span data-ttu-id="c6b1c-126">IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6b1c-126">IUnknown</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="c6b1c-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="c6b1c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6b1c-128">X 檔案參考</span><span class="sxs-lookup"><span data-stu-id="c6b1c-128">X File Reference</span></span>](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 



