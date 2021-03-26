---
title: 'ID3DX11ThreadPump ProcessDeviceWorkItems 方法 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 在裝置完成載入和處理之後，將工作專案設定為裝置。
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- ProcessDeviceWorkItems 方法 Direct3D 11
- ProcessDeviceWorkItems 方法 Direct3D 11，ID3DX11ThreadPump 介面
- ID3DX11ThreadPump 介面 Direct3D 11，ProcessDeviceWorkItems 方法
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.ProcessDeviceWorkItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad570785ac7dc36fb5dd9d464e97ef46f52ca93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974528"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a><span data-ttu-id="94f72-107">ID3DX11ThreadPump：:P rocessDeviceWorkItems 方法</span><span class="sxs-lookup"><span data-stu-id="94f72-107">ID3DX11ThreadPump::ProcessDeviceWorkItems method</span></span>

> [!Note]  
> <span data-ttu-id="94f72-108">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="94f72-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="94f72-109">在裝置完成載入和處理之後，將工作專案設定為裝置。</span><span class="sxs-lookup"><span data-stu-id="94f72-109">Sets work items to the device after they have finished loading and processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="94f72-110">語法</span><span class="sxs-lookup"><span data-stu-id="94f72-110">Syntax</span></span>


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a><span data-ttu-id="94f72-111">參數</span><span class="sxs-lookup"><span data-stu-id="94f72-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94f72-112">*iWorkItemCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="94f72-112">*iWorkItemCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94f72-113">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="94f72-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="94f72-114">要設定至裝置的工作專案數。</span><span class="sxs-lookup"><span data-stu-id="94f72-114">The number of work items to set to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94f72-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="94f72-115">Return value</span></span>

<span data-ttu-id="94f72-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="94f72-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="94f72-117">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="94f72-117">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="94f72-118">備註</span><span class="sxs-lookup"><span data-stu-id="94f72-118">Remarks</span></span>

<span data-ttu-id="94f72-119">當執行緒抽取完成載入和處理資源或著色器時，它會將其保留在佇列中，直到呼叫此 API 為止，此時已處理的專案將會設定為裝置。</span><span class="sxs-lookup"><span data-stu-id="94f72-119">When the thread pump has finished loading and processing a resource or shader, it will hold it in a queue until this API is called, at which point the processed items will be set to the device.</span></span> <span data-ttu-id="94f72-120">這對於控制每個畫面系將資源系結至裝置所花費的處理量相當有用。</span><span class="sxs-lookup"><span data-stu-id="94f72-120">This is useful for controlling the amount of processing that is spent on binding resources to the device for each frame.</span></span>

<span data-ttu-id="94f72-121">例如，假設您接近遊戲的某個層級，而且您想要開始預先載入紋理、著色器和其他資源，以進行下一個層級。</span><span class="sxs-lookup"><span data-stu-id="94f72-121">As an example of how one might use this API, say you are nearing the end of one level in your game and you want to begin preloading the textures, shaders, and other resources for the next level.</span></span> <span data-ttu-id="94f72-122">執行緒抽取將開始在個別執行緒上載入、解壓縮和處理資源和著色器，直到它們準備好設定至裝置為止，此時會將它們保留在佇列中。</span><span class="sxs-lookup"><span data-stu-id="94f72-122">The thread pump will begin loading, decompressing, and processing the resources and shaders on a separate thread until they are ready to be set to the device, at which point it will leave them in a queue.</span></span> <span data-ttu-id="94f72-123">您可能不想要一次將所有資源和著色器設定為裝置，因為這可能會造成遊戲效能明顯降低的情況。</span><span class="sxs-lookup"><span data-stu-id="94f72-123">One may not want to set all the resources and shaders to the device at once because this may cause a noticeable temporary slow down in the game's performance.</span></span> <span data-ttu-id="94f72-124">因此，每個框架可呼叫此 API 一次，如此一來，就只會在每個畫面上將一個小數位的工作專案設定為裝置，藉此將系結資源的工作負載分散到數個畫面上的裝置。</span><span class="sxs-lookup"><span data-stu-id="94f72-124">So, this API could be called once per frame so that only a small number work items would be set to the device on each frame, thereby spreading the work load of binding resources to the device over several frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="94f72-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="94f72-125">Requirements</span></span>



| <span data-ttu-id="94f72-126">需求</span><span class="sxs-lookup"><span data-stu-id="94f72-126">Requirement</span></span> | <span data-ttu-id="94f72-127">值</span><span class="sxs-lookup"><span data-stu-id="94f72-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94f72-128">標頭</span><span class="sxs-lookup"><span data-stu-id="94f72-128">Header</span></span><br/>  | <dl> <span data-ttu-id="94f72-129"><dt>D3DX11core。h</dt></span><span class="sxs-lookup"><span data-stu-id="94f72-129"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="94f72-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="94f72-130">Library</span></span><br/> | <dl> <span data-ttu-id="94f72-131"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="94f72-131"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="94f72-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94f72-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94f72-133">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="94f72-133">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="94f72-134">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="94f72-134">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

