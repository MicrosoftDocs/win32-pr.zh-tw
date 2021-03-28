---
title: 'ID3DX11ThreadPump 介面 (D3DX11core .h) '
description: 執行緒抽取會以非同步方式執行工作。
ms.assetid: 1a99f728-149d-4800-a6e4-e3a00cf8cf4f
keywords:
- ID3DX11ThreadPump 介面 Direct3D 11
- ID3DX11ThreadPump 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60cedaa4ef84cb9f3ea31cd619d7335cc09324e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094019"
---
# <a name="id3dx11threadpump-interface"></a><span data-ttu-id="91139-105">ID3DX11ThreadPump 介面</span><span class="sxs-lookup"><span data-stu-id="91139-105">ID3DX11ThreadPump interface</span></span>

> [!Note]  
> <span data-ttu-id="91139-106">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="91139-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="91139-107">執行緒抽取會以非同步方式執行工作。</span><span class="sxs-lookup"><span data-stu-id="91139-107">A thread pump executes tasks asynchronously.</span></span> <span data-ttu-id="91139-108">它是透過呼叫 [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md)來建立。</span><span class="sxs-lookup"><span data-stu-id="91139-108">It is created by calling [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md).</span></span> <span data-ttu-id="91139-109">有數個 Api 會採用選擇性的執行緒抽取作為參數，例如 [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) 和 [**D3DX11CompileFromFile**](d3dx11compilefromfile.md);如果您將執行緒抽取介面傳遞至這些 Api，函式將會在個別的執行緒上以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="91139-109">There are several APIs that take an optional thread pump as a parameter, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); if you pass a thread pump interface into these APIs, the functions will execute asynchronously on a separate thread.</span></span> <span data-ttu-id="91139-110">尤其是在多處理器的電腦上，執行緒抽取可以載入資源並處理資料，而不會明顯降低效能。</span><span class="sxs-lookup"><span data-stu-id="91139-110">Particularly on multiprocessor machines, a thread pump can load resources and process data without a noticeable decrease in performance.</span></span>

## <a name="members"></a><span data-ttu-id="91139-111">成員</span><span class="sxs-lookup"><span data-stu-id="91139-111">Members</span></span>

<span data-ttu-id="91139-112">**ID3DX11ThreadPump** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="91139-112">The **ID3DX11ThreadPump** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="91139-113">**ID3DX11ThreadPump** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="91139-113">**ID3DX11ThreadPump** also has these types of members:</span></span>

-   [<span data-ttu-id="91139-114">方法</span><span class="sxs-lookup"><span data-stu-id="91139-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="91139-115">方法</span><span class="sxs-lookup"><span data-stu-id="91139-115">Methods</span></span>

<span data-ttu-id="91139-116">**ID3DX11ThreadPump** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="91139-116">The **ID3DX11ThreadPump** interface has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="91139-117">方法</span><span class="sxs-lookup"><span data-stu-id="91139-117">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="91139-118">描述</span><span class="sxs-lookup"><span data-stu-id="91139-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="91139-119"><a href="id3dx11threadpump-addworkitem.md"><strong>Azuretasks</strong></a></span><span class="sxs-lookup"><span data-stu-id="91139-119"><a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="91139-120">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="91139-120">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="91139-121">將工作專案加入至執行緒抽取。</span><span class="sxs-lookup"><span data-stu-id="91139-121">Adds a work item to the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="91139-122"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="91139-122"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="91139-123">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="91139-123">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="91139-124">取得執行緒抽取內三個佇列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="91139-124">Gets the number of items in each of the three queues inside the thread pump.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="91139-125"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="91139-125"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="91139-126">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="91139-126">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="91139-127">取得執行緒抽取中的工作專案數。</span><span class="sxs-lookup"><span data-stu-id="91139-127">Gets the number of work items in the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="91139-128"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="91139-128"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="91139-129">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="91139-129">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="91139-130">在裝置完成載入和處理之後，將工作專案設定為裝置。</span><span class="sxs-lookup"><span data-stu-id="91139-130">Sets work items to the device after they have finished loading and processing.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="91139-131"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="91139-131"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="91139-132">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="91139-132">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="91139-133">清除執行緒抽取中的所有工作專案。</span><span class="sxs-lookup"><span data-stu-id="91139-133">Clears all work items from the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="91139-134"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="91139-134"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="91139-135">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="91139-135">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="91139-136">等候執行緒抽取中的所有工作專案完成。</span><span class="sxs-lookup"><span data-stu-id="91139-136">Waits for all work items in the thread pump to finish.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="91139-137">備註</span><span class="sxs-lookup"><span data-stu-id="91139-137">Remarks</span></span>

### <a name="using-a-thread-pump"></a><span data-ttu-id="91139-138">使用執行緒抽取</span><span class="sxs-lookup"><span data-stu-id="91139-138">Using a Thread Pump</span></span>

<span data-ttu-id="91139-139">執行緒抽取會使用下列三個步驟的處理常式來載入和處理資料：</span><span class="sxs-lookup"><span data-stu-id="91139-139">The thread pump loads and processes data using the following three-step process:</span></span>

1.  <span data-ttu-id="91139-140">使用 [**資料載入**](id3dx11dataloader.md)器載入和解壓縮資料。</span><span class="sxs-lookup"><span data-stu-id="91139-140">Load and decompress the data with a [**Data Loader**](id3dx11dataloader.md).</span></span> <span data-ttu-id="91139-141">資料載入器物件有三個方法，當執行緒提取在載入和解壓縮資料時，會在內部呼叫： [**ID3DX11DataLoader：： Load**](id3dx11dataloader-load.md)、 [**ID3DX11DataLoader：:D ecompress**](id3dx11dataloader-decompress.md)和 [**ID3DX11DataLoader：:D estroy**](id3dx11dataloader-destroy.md)。</span><span class="sxs-lookup"><span data-stu-id="91139-141">The data loader object has three methods that the thread pump will call internally as it is loading and decompressing the data: [**ID3DX11DataLoader::Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::Decompress**](id3dx11dataloader-decompress.md), and [**ID3DX11DataLoader::Destroy**](id3dx11dataloader-destroy.md).</span></span> <span data-ttu-id="91139-142">這三個 Api 的特定功能會根據所載入和解壓縮的資料類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="91139-142">The specific functionality of these three APIs differs depending on the type of data being loaded and decompressed.</span></span> <span data-ttu-id="91139-143">資料載入器介面也可以被繼承，而且如果載入的資料檔是以一個自訂格式來定義，則可以變更其 Api。</span><span class="sxs-lookup"><span data-stu-id="91139-143">The data loader interface can also be inherited and its APIs can be changed if one is loading a data file defined in one's own custom format.</span></span>
2.  <span data-ttu-id="91139-144">使用 [**資料處理器**](id3dx11dataprocessor.md)來處理資料。</span><span class="sxs-lookup"><span data-stu-id="91139-144">Process the data with a [**Data Processor**](id3dx11dataprocessor.md).</span></span> <span data-ttu-id="91139-145">資料處理器物件有三個方法，當執行緒在處理資料時，會在內部呼叫： [**ID3DX11DataProcessor：:P rocess**](id3dx11dataprocessor-process.md)、 [**ID3DX11DataProcessor：： CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)和 [**ID3DX11DataProcessor：:D estroy**](id3dx11dataprocessor-destroy.md)。</span><span class="sxs-lookup"><span data-stu-id="91139-145">The data processor object has three methods that the thread pump will call internally as it is processing the data: [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md), and [**ID3DX11DataProcessor::Destroy**](id3dx11dataprocessor-destroy.md).</span></span> <span data-ttu-id="91139-146">根據資料的類型而定，處理資料的方式會有所不同。</span><span class="sxs-lookup"><span data-stu-id="91139-146">The way it processes the data will be different depending on the type of data.</span></span> <span data-ttu-id="91139-147">例如，如果資料是儲存為 JPEG 的材質，則 [**ID3DX11DataProcessor：:P rocess**](id3dx11dataprocessor-process.md) 會執行 JPEG 解壓縮，以取得影像的原始影像位。</span><span class="sxs-lookup"><span data-stu-id="91139-147">For example, if the data is a texture stored as a JPEG, then [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md) will do JPEG decompression to get the image's raw image bits.</span></span> <span data-ttu-id="91139-148">如果資料是著色器，則 [**ID3DX11DataProcessor：:P rocess**](id3dx11dataprocessor-process.md) 會將 HLSL 編譯成位元組程式碼。</span><span class="sxs-lookup"><span data-stu-id="91139-148">If the data is a shader, then [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md) will compile the HLSL into bytecode.</span></span> <span data-ttu-id="91139-149">處理資料之後，將會針對該資料 (使用 [**ID3DX11DataProcessor：：) CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md) 建立裝置物件，並將該物件新增至裝置物件的佇列。</span><span class="sxs-lookup"><span data-stu-id="91139-149">After the data has been processed a device object will be created for that data (with [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)) and the object will be added to a queue of device objects.</span></span> <span data-ttu-id="91139-150">您也可以繼承資料處理器介面，如果其中一個應用程式的 Api 是以一個自訂格式來處理的資料檔案，則可以變更其 Api。</span><span class="sxs-lookup"><span data-stu-id="91139-150">The data processor interface can also be inherited and its APIs can be changed if one is processing a data file defined in one's own custom format.</span></span>
3.  <span data-ttu-id="91139-151">將裝置物件系結至裝置。</span><span class="sxs-lookup"><span data-stu-id="91139-151">Bind the device object to the device.</span></span> <span data-ttu-id="91139-152">當其中一個應用程式呼叫 ID3DX11ThreadPump 時，就會執行此動作 [**：:P rocessdeviceworkitems**](id3dx11threadpump-processdeviceworkitems.md)，這會將裝置物件佇列中指定的物件數目系結至裝置。</span><span class="sxs-lookup"><span data-stu-id="91139-152">This is done when one's application calls [**ID3DX11ThreadPump::ProcessDeviceWorkItems**](id3dx11threadpump-processdeviceworkitems.md), which will bind a specified number of objects in the queue of device objects to the device.</span></span>

<span data-ttu-id="91139-153">執行緒抽取可以用兩種方式之一來載入資料：藉由呼叫接受執行緒提取的 API 做為參數，例如 [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) 和 [**D3DX11CompileFromFile**](d3dx11compilefromfile.md)，或呼叫 [**ID3DX11ThreadPump：： azuretasks**](id3dx11threadpump-addworkitem.md)。</span><span class="sxs-lookup"><span data-stu-id="91139-153">The thread pump can be used to load data in one of two ways: by calling an API that takes a thread pump as a parameter, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), or by calling [**ID3DX11ThreadPump::AddWorkItem**](id3dx11threadpump-addworkitem.md).</span></span> <span data-ttu-id="91139-154">如果是採用執行緒抽取的 Api，則會在內部建立資料載入器和資料處理器。</span><span class="sxs-lookup"><span data-stu-id="91139-154">In the case of the APIs that take a thread pump, the data loader and data processor are created internally.</span></span> <span data-ttu-id="91139-155">在 Azuretasks 的案例中，資料載入器和資料處理器必須事先建立，然後再傳遞至 Azuretasks。</span><span class="sxs-lookup"><span data-stu-id="91139-155">In the case of AddWorkItem, the data loader and data processor must be created beforehand and are then passed into AddWorkItem.</span></span> <span data-ttu-id="91139-156">D3DX11 提供一組 Api，可用來建立可載入和處理一般資料格式的資料載入器和資料處理器。</span><span class="sxs-lookup"><span data-stu-id="91139-156">D3DX11 provides a set of APIs for creating data loaders and data processors that have functionality for loading and processing common data formats.</span></span> <span data-ttu-id="91139-157">針對自訂資料格式，必須繼承資料載入器和資料處理器介面，而且必須重新定義它們的方法。</span><span class="sxs-lookup"><span data-stu-id="91139-157">For custom data formats, the data loader and data processor interfaces must be inherited and their methods must be redefined.</span></span>

<span data-ttu-id="91139-158">執行緒抽取物件佔用大量的資源，因此通常每個應用程式只能建立一個資源。</span><span class="sxs-lookup"><span data-stu-id="91139-158">The thread pump object takes up a substantial amount of resources, so generally only one should be created per application.</span></span>

## <a name="requirements"></a><span data-ttu-id="91139-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="91139-159">Requirements</span></span>



| <span data-ttu-id="91139-160">需求</span><span class="sxs-lookup"><span data-stu-id="91139-160">Requirement</span></span> | <span data-ttu-id="91139-161">值</span><span class="sxs-lookup"><span data-stu-id="91139-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91139-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91139-162">Minimum supported client</span></span><br/> | <span data-ttu-id="91139-163">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91139-163">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="91139-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91139-164">Minimum supported server</span></span><br/> | <span data-ttu-id="91139-165">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91139-165">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="91139-166">標頭</span><span class="sxs-lookup"><span data-stu-id="91139-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="91139-167"><dt>D3DX11core。h</dt></span><span class="sxs-lookup"><span data-stu-id="91139-167"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="91139-168">程式庫</span><span class="sxs-lookup"><span data-stu-id="91139-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="91139-169"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="91139-169"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="91139-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91139-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91139-171">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="91139-171">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

