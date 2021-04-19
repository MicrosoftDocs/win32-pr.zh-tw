---
description: X 檔案格式、載入和儲存選項。
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073887c6cc93754ead01ce379310a9be09edc88f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106980304"
---
# <a name="d3dxf"></a><span data-ttu-id="04e1d-103">D3DXF</span><span class="sxs-lookup"><span data-stu-id="04e1d-103">D3DXF</span></span>

<span data-ttu-id="04e1d-104">X 檔案格式、載入和儲存選項。</span><span class="sxs-lookup"><span data-stu-id="04e1d-104">X file format, load, and save options.</span></span>

## <a name="file-formats"></a><span data-ttu-id="04e1d-105">檔案格式</span><span class="sxs-lookup"><span data-stu-id="04e1d-105">File Formats</span></span>

<span data-ttu-id="04e1d-106">下表指定檔資料的類型：</span><span class="sxs-lookup"><span data-stu-id="04e1d-106">The following table specifies the type of file data:</span></span>



| <span data-ttu-id="04e1d-107">\#定義檔案格式</span><span class="sxs-lookup"><span data-stu-id="04e1d-107">\#defines for File Format</span></span>     | <span data-ttu-id="04e1d-108">值</span><span class="sxs-lookup"><span data-stu-id="04e1d-108">Value</span></span> | <span data-ttu-id="04e1d-109">描述</span><span class="sxs-lookup"><span data-stu-id="04e1d-109">Description</span></span>                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04e1d-110">D3DXF \_ >fileformat \_ 二進位檔</span><span class="sxs-lookup"><span data-stu-id="04e1d-110">D3DXF\_FILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="04e1d-111">0</span><span class="sxs-lookup"><span data-stu-id="04e1d-111">0</span></span>     | <span data-ttu-id="04e1d-112">舊版格式的二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="04e1d-112">Legacy-format binary file.</span></span> <span data-ttu-id="04e1d-113">請參閱 [X 檔案參考 (舊版) ](dx9-graphics-reference-x-file.md)。</span><span class="sxs-lookup"><span data-stu-id="04e1d-113">See [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span> |
| <span data-ttu-id="04e1d-114">D3DXF \_ >fileformat \_ 文字</span><span class="sxs-lookup"><span data-stu-id="04e1d-114">D3DXF\_FILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="04e1d-115">1</span><span class="sxs-lookup"><span data-stu-id="04e1d-115">1</span></span>     | <span data-ttu-id="04e1d-116">文字檔。</span><span class="sxs-lookup"><span data-stu-id="04e1d-116">Text file.</span></span>                                                                                     |
| <span data-ttu-id="04e1d-117">D3DXF \_ >fileformat \_ 壓縮</span><span class="sxs-lookup"><span data-stu-id="04e1d-117">D3DXF\_FILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="04e1d-118">2</span><span class="sxs-lookup"><span data-stu-id="04e1d-118">2</span></span>     | <span data-ttu-id="04e1d-119">壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="04e1d-119">Compressed file.</span></span> <span data-ttu-id="04e1d-120">使用這個旗標時，您也必須指定二進位格式或文字格式。</span><span class="sxs-lookup"><span data-stu-id="04e1d-120">With this flag, you must also specify the binary format or the text format.</span></span>   |



 

## <a name="file-load-options"></a><span data-ttu-id="04e1d-121">檔案載入選項</span><span class="sxs-lookup"><span data-stu-id="04e1d-121">File Load Options</span></span>

<span data-ttu-id="04e1d-122">下表指定副檔名為 x 的檔案載入選項：</span><span class="sxs-lookup"><span data-stu-id="04e1d-122">The following table specifies file load options with .x files:</span></span>



| <span data-ttu-id="04e1d-123">\#定義</span><span class="sxs-lookup"><span data-stu-id="04e1d-123">\#define</span></span>                      | <span data-ttu-id="04e1d-124">值</span><span class="sxs-lookup"><span data-stu-id="04e1d-124">Value</span></span> | <span data-ttu-id="04e1d-125">描述</span><span class="sxs-lookup"><span data-stu-id="04e1d-125">Description</span></span>                |
|-------------------------------|-------|----------------------------|
| <span data-ttu-id="04e1d-126">D3DXF \_ FILELOAD \_ FromFile</span><span class="sxs-lookup"><span data-stu-id="04e1d-126">D3DXF\_FILELOAD\_FromFile</span></span>     | <span data-ttu-id="04e1d-127">0</span><span class="sxs-lookup"><span data-stu-id="04e1d-127">0</span></span>     | <span data-ttu-id="04e1d-128">從檔案載入資料。</span><span class="sxs-lookup"><span data-stu-id="04e1d-128">Load data from a file.</span></span>     |
| <span data-ttu-id="04e1d-129">D3DXF \_ FILELOAD \_ FROMWFILE</span><span class="sxs-lookup"><span data-stu-id="04e1d-129">D3DXF\_FILELOAD\_FROMWFILE</span></span>    | <span data-ttu-id="04e1d-130">1</span><span class="sxs-lookup"><span data-stu-id="04e1d-130">1</span></span>     | <span data-ttu-id="04e1d-131">從檔案載入資料。</span><span class="sxs-lookup"><span data-stu-id="04e1d-131">Load data from a file.</span></span>     |
| <span data-ttu-id="04e1d-132">D3DXF \_ FILELOAD \_ FROMRESOURCE</span><span class="sxs-lookup"><span data-stu-id="04e1d-132">D3DXF\_FILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="04e1d-133">2</span><span class="sxs-lookup"><span data-stu-id="04e1d-133">2</span></span>     | <span data-ttu-id="04e1d-134">從資源載入資料。</span><span class="sxs-lookup"><span data-stu-id="04e1d-134">Load data from a resource.</span></span> |
| <span data-ttu-id="04e1d-135">D3DXF \_ FILELOAD \_ FROMMEMORY</span><span class="sxs-lookup"><span data-stu-id="04e1d-135">D3DXF\_FILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="04e1d-136">3</span><span class="sxs-lookup"><span data-stu-id="04e1d-136">3</span></span>     | <span data-ttu-id="04e1d-137">從記憶體載入資料。</span><span class="sxs-lookup"><span data-stu-id="04e1d-137">Load data from memory.</span></span>     |



 

## <a name="file-save-options"></a><span data-ttu-id="04e1d-138">檔儲存選項</span><span class="sxs-lookup"><span data-stu-id="04e1d-138">File Save Options</span></span>

<span data-ttu-id="04e1d-139">下表指定 file save 和 load 選項與. x 檔案：</span><span class="sxs-lookup"><span data-stu-id="04e1d-139">The following table specifies file save and load options with .x files:</span></span>



| <span data-ttu-id="04e1d-140">\#定義</span><span class="sxs-lookup"><span data-stu-id="04e1d-140">\#define</span></span>                 | <span data-ttu-id="04e1d-141">值</span><span class="sxs-lookup"><span data-stu-id="04e1d-141">Value</span></span> | <span data-ttu-id="04e1d-142">描述</span><span class="sxs-lookup"><span data-stu-id="04e1d-142">Description</span></span>                    |
|--------------------------|-------|--------------------------------|
| <span data-ttu-id="04e1d-143">D3DXF \_ FILESAVE \_ TOFILE</span><span class="sxs-lookup"><span data-stu-id="04e1d-143">D3DXF\_FILESAVE\_TOFILE</span></span>  | <span data-ttu-id="04e1d-144">0</span><span class="sxs-lookup"><span data-stu-id="04e1d-144">0</span></span>     | <span data-ttu-id="04e1d-145">儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="04e1d-145">Save to a file.</span></span>                |
| <span data-ttu-id="04e1d-146">D3DXF \_ FILESAVE \_ TOWFILE</span><span class="sxs-lookup"><span data-stu-id="04e1d-146">D3DXF\_FILESAVE\_TOWFILE</span></span> | <span data-ttu-id="04e1d-147">1</span><span class="sxs-lookup"><span data-stu-id="04e1d-147">1</span></span>     | <span data-ttu-id="04e1d-148">儲存至寬字元的檔案。</span><span class="sxs-lookup"><span data-stu-id="04e1d-148">Save to a wide-character file.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="04e1d-149">常數資訊</span><span class="sxs-lookup"><span data-stu-id="04e1d-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="04e1d-150">標頭</span><span class="sxs-lookup"><span data-stu-id="04e1d-150">Header</span></span>                   | <span data-ttu-id="04e1d-151">d3dx9xof。h</span><span class="sxs-lookup"><span data-stu-id="04e1d-151">d3dx9xof.h</span></span> |
| <span data-ttu-id="04e1d-152">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="04e1d-152">Minimum operating system</span></span> | <span data-ttu-id="04e1d-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="04e1d-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="04e1d-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="04e1d-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04e1d-155">D3DX X 檔案常數</span><span class="sxs-lookup"><span data-stu-id="04e1d-155">D3DX X File Constants</span></span>](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[<span data-ttu-id="04e1d-156">**D3DXSaveMeshToX**</span><span class="sxs-lookup"><span data-stu-id="04e1d-156">**D3DXSaveMeshToX**</span></span>](d3dxsavemeshtox.md)
</dt> </dl>

 

 



