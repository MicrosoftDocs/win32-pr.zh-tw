---
description: 深入瞭解：封包 API 宏
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: 封包 API 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390fa42e0293e5d47c405e8e99986538b8f26254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510378"
---
# <a name="cabinet-api-macros"></a><span data-ttu-id="79488-103">封包 API 宏</span><span class="sxs-lookup"><span data-stu-id="79488-103">Cabinet API Macros</span></span>

<span data-ttu-id="79488-104">本節將詳細說明 Cabinet API 所使用的宏：</span><span class="sxs-lookup"><span data-stu-id="79488-104">This section details the macros used by the Cabinet API:</span></span>

## <a name="fci-macros"></a><span data-ttu-id="79488-105">FCI 宏</span><span class="sxs-lookup"><span data-stu-id="79488-105">FCI Macros</span></span>

<span data-ttu-id="79488-106">FCI 會使用下列宏：</span><span class="sxs-lookup"><span data-stu-id="79488-106">The following macros are used by FCI:</span></span>



| <span data-ttu-id="79488-107">巨集</span><span class="sxs-lookup"><span data-stu-id="79488-107">Macro</span></span>                                              | <span data-ttu-id="79488-108">Description</span><span class="sxs-lookup"><span data-stu-id="79488-108">Description</span></span>                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79488-109">**FNFCIALLOC**</span><span class="sxs-lookup"><span data-stu-id="79488-109">**FNFCIALLOC**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | <span data-ttu-id="79488-110">用來在 FCI 內容中配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="79488-110">Used to allocate memory in an FCI context.</span></span><br/>                                          |
| [<span data-ttu-id="79488-111">**FNFCICLOSE**</span><span class="sxs-lookup"><span data-stu-id="79488-111">**FNFCICLOSE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | <span data-ttu-id="79488-112">用來關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="79488-112">Used to close a file.</span></span><br/>                                                               |
| [<span data-ttu-id="79488-113">**FNFCIDELETE**</span><span class="sxs-lookup"><span data-stu-id="79488-113">**FNFCIDELETE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | <span data-ttu-id="79488-114">用來刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="79488-114">Used to delete a file.</span></span><br/>                                                              |
| [<span data-ttu-id="79488-115">**FNFCIFILEPLACED**</span><span class="sxs-lookup"><span data-stu-id="79488-115">**FNFCIFILEPLACED**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | <span data-ttu-id="79488-116">用來在檔案放入封包時通知。</span><span class="sxs-lookup"><span data-stu-id="79488-116">Used to notify when a file is placed in the cabinet.</span></span><br/>                                |
| [<span data-ttu-id="79488-117">**FNFCIFREE**</span><span class="sxs-lookup"><span data-stu-id="79488-117">**FNFCIFREE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | <span data-ttu-id="79488-118">用來釋放先前在 FCI 內容中配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="79488-118">Used to free previously allocated memory in an FCI context.</span></span><br/>                         |
| [<span data-ttu-id="79488-119">**FNFCIGETNEXTCABINET**</span><span class="sxs-lookup"><span data-stu-id="79488-119">**FNFCIGETNEXTCABINET**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | <span data-ttu-id="79488-120">用來要求下一個封包的資訊。</span><span class="sxs-lookup"><span data-stu-id="79488-120">Used to request information for the next cabinet.</span></span><br/>                                   |
| [<span data-ttu-id="79488-121">**FNFCIGETOPENINFO**</span><span class="sxs-lookup"><span data-stu-id="79488-121">**FNFCIGETOPENINFO**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | <span data-ttu-id="79488-122">用來開啟檔案並取出檔案日期、時間和屬性。</span><span class="sxs-lookup"><span data-stu-id="79488-122">Used to open a file and retrieve file date, time, and attributes.</span></span><br/>                   |
| [<span data-ttu-id="79488-123">**FNFCIGETTEMPFILE**</span><span class="sxs-lookup"><span data-stu-id="79488-123">**FNFCIGETTEMPFILE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | <span data-ttu-id="79488-124">用來取得暫存檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="79488-124">Used to obtain a temporary file name.</span></span><br/>                                               |
| [<span data-ttu-id="79488-125">**FNFCIOPEN**</span><span class="sxs-lookup"><span data-stu-id="79488-125">**FNFCIOPEN**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | <span data-ttu-id="79488-126">用來在 FCI 內容中開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="79488-126">Used to open a file in an FCI context.</span></span><br/>                                              |
| [<span data-ttu-id="79488-127">**FNFCIREAD**</span><span class="sxs-lookup"><span data-stu-id="79488-127">**FNFCIREAD**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciread)                     | <span data-ttu-id="79488-128">用來從檔案讀取資料。</span><span class="sxs-lookup"><span data-stu-id="79488-128">Used to read data from a file.</span></span><br/>                                                      |
| [<span data-ttu-id="79488-129">**FNFCISEEK**</span><span class="sxs-lookup"><span data-stu-id="79488-129">**FNFCISEEK**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | <span data-ttu-id="79488-130">用來將檔案指標移至指定的位置。</span><span class="sxs-lookup"><span data-stu-id="79488-130">Used to move a file pointer to a specified location.</span></span><br/>                                |
| [<span data-ttu-id="79488-131">**FNFCISTATUS**</span><span class="sxs-lookup"><span data-stu-id="79488-131">**FNFCISTATUS**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | <span data-ttu-id="79488-132">用來更新使用者。</span><span class="sxs-lookup"><span data-stu-id="79488-132">Used to update the user.</span></span><br/>                                                            |
| [<span data-ttu-id="79488-133">**FNFCIWRITE**</span><span class="sxs-lookup"><span data-stu-id="79488-133">**FNFCIWRITE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | <span data-ttu-id="79488-134">用來將資料寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="79488-134">Used to write data to a file.</span></span><br/>                                                       |
| [<span data-ttu-id="79488-135">**TCOMPfromLZXWindow**</span><span class="sxs-lookup"><span data-stu-id="79488-135">**TCOMPfromLZXWindow**</span></span>](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | <span data-ttu-id="79488-136">將 windows 大小轉換成 [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile)的 LXZ TCOMP 值。</span><span class="sxs-lookup"><span data-stu-id="79488-136">Converts windows size into an LXZ TCOMP value for [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile).</span></span><br/> |



 

## <a name="fdi-macros"></a><span data-ttu-id="79488-137">FDI 宏</span><span class="sxs-lookup"><span data-stu-id="79488-137">FDI Macros</span></span>

<span data-ttu-id="79488-138">FDI 會使用下列宏：</span><span class="sxs-lookup"><span data-stu-id="79488-138">The following macros are used by FDI:</span></span>



| <span data-ttu-id="79488-139">巨集</span><span class="sxs-lookup"><span data-stu-id="79488-139">Macro</span></span>                              | <span data-ttu-id="79488-140">Description</span><span class="sxs-lookup"><span data-stu-id="79488-140">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="79488-141">**FNALLOC**</span><span class="sxs-lookup"><span data-stu-id="79488-141">**FNALLOC**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | <span data-ttu-id="79488-142">用來在 FDI 內容中配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="79488-142">Used to allocate memory in an FDI context.</span></span><br/>                               |
| [<span data-ttu-id="79488-143">**FNCLOSE**</span><span class="sxs-lookup"><span data-stu-id="79488-143">**FNCLOSE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnclose)         | <span data-ttu-id="79488-144">用來關閉 FDI 內容中的檔案。</span><span class="sxs-lookup"><span data-stu-id="79488-144">Used to close a file in an FDI context.</span></span><br/>                                  |
| [<span data-ttu-id="79488-145">**FNFDINOTIFY**</span><span class="sxs-lookup"><span data-stu-id="79488-145">**FNFDINOTIFY**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | <span data-ttu-id="79488-146">用來更新解碼器狀態的應用程式。</span><span class="sxs-lookup"><span data-stu-id="79488-146">Used to update the application on the status of the decoder.</span></span><br/>             |
| [<span data-ttu-id="79488-147">**FNFREE**</span><span class="sxs-lookup"><span data-stu-id="79488-147">**FNFREE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnfree)           | <span data-ttu-id="79488-148">用來釋放先前在 FDI 內容中配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="79488-148">Used to free previously allocated memory in an FDI context.</span></span><br/>              |
| [<span data-ttu-id="79488-149">**FNOPEN**</span><span class="sxs-lookup"><span data-stu-id="79488-149">**FNOPEN**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnopen)           | <span data-ttu-id="79488-150">用來在 FDI 內容中開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="79488-150">Used to open a file in an FDI context.</span></span><br/>                                   |
| [<span data-ttu-id="79488-151">**FNREAD**</span><span class="sxs-lookup"><span data-stu-id="79488-151">**FNREAD**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnread)           | <span data-ttu-id="79488-152">用來從 FDI 內容中的檔案讀取資料。</span><span class="sxs-lookup"><span data-stu-id="79488-152">Used to read data from a file in an FDI context.</span></span><br/>                         |
| [<span data-ttu-id="79488-153">**FNSEEK**</span><span class="sxs-lookup"><span data-stu-id="79488-153">**FNSEEK**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnseek)           | <span data-ttu-id="79488-154">用來將檔案指標移至 FDI 內容中的指定位置。</span><span class="sxs-lookup"><span data-stu-id="79488-154">Used to move a file pointer to the specified location in an FDI context.</span></span><br/> |
| [<span data-ttu-id="79488-155">**FNWRITE**</span><span class="sxs-lookup"><span data-stu-id="79488-155">**FNWRITE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | <span data-ttu-id="79488-156">用來將資料寫入 FDI 內容中的檔案。</span><span class="sxs-lookup"><span data-stu-id="79488-156">Used to write data to a file in an FDI context.</span></span><br/>                          |



 

## <a name="related-topics"></a><span data-ttu-id="79488-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="79488-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79488-158">封包 API 參考</span><span class="sxs-lookup"><span data-stu-id="79488-158">Cabinet API Reference</span></span>](cabinet-api-reference.md)
</dt> <dt>

[<span data-ttu-id="79488-159">使用封包 API</span><span class="sxs-lookup"><span data-stu-id="79488-159">Using the Cabinet API</span></span>](using-the-cabinet-api.md)
</dt> </dl>

 

 




