---
description: 在裝置完成載入和處理之後，將工作專案設定為裝置。
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: 'ID3DX10ThreadPump：:P rocessDeviceWorkItems 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.ProcessDeviceWorkItems
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 88b98d68e4e0e47b2c8e7f9a2e095565c53e2561
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116300"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a><span data-ttu-id="f0900-103">ID3DX10ThreadPump：:P rocessDeviceWorkItems 方法</span><span class="sxs-lookup"><span data-stu-id="f0900-103">ID3DX10ThreadPump::ProcessDeviceWorkItems method</span></span>

<span data-ttu-id="f0900-104">在裝置完成載入和處理之後，將工作專案設定為裝置。</span><span class="sxs-lookup"><span data-stu-id="f0900-104">Set work items to the device after they have finished loading and processing.</span></span> <span data-ttu-id="f0900-105">當執行緒抽取完成載入和處理資源或著色器時，它會將其保留在佇列中，直到呼叫此 API 為止，此時已處理的專案將會設定為裝置。</span><span class="sxs-lookup"><span data-stu-id="f0900-105">When the thread pump has finished loading and processing a resource or shader, it will hold it in a queue until this API is called, at which point the processed items will be set to the device.</span></span> <span data-ttu-id="f0900-106">這對於控制每個畫面系將資源系結至裝置所花費的處理量相當有用。</span><span class="sxs-lookup"><span data-stu-id="f0900-106">This is useful for controlling the amount of processing that is spent on binding resources to the device for each frame.</span></span> <span data-ttu-id="f0900-107">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f0900-107">See remarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0900-108">語法</span><span class="sxs-lookup"><span data-stu-id="f0900-108">Syntax</span></span>


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a><span data-ttu-id="f0900-109">參數</span><span class="sxs-lookup"><span data-stu-id="f0900-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0900-110">*iWorkItemCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0900-110">*iWorkItemCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0900-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0900-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0900-112">要設定至裝置的工作專案數。</span><span class="sxs-lookup"><span data-stu-id="f0900-112">The number of work items to set to the device.</span></span> <span data-ttu-id="f0900-113">ProcessDeviceObjectCreation 會建立最多 iWorkItemCount 的物件。</span><span class="sxs-lookup"><span data-stu-id="f0900-113">ProcessDeviceObjectCreation will create at most iWorkItemCount objects.</span></span> <span data-ttu-id="f0900-114">如果佇列中沒有足夠的工作專案來處理 iWorkItemCount 物件，ProcessDeviceObjectCreation 將會建立與佇列中的專案數目一樣多的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="f0900-114">If there are not enough work items in the queue to process iWorkItemCount objects, ProcessDeviceObjectCreation will create as many device objects as there are items in the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0900-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0900-115">Return value</span></span>

<span data-ttu-id="f0900-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f0900-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f0900-117">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f0900-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f0900-118">備註</span><span class="sxs-lookup"><span data-stu-id="f0900-118">Remarks</span></span>

<span data-ttu-id="f0900-119">例如，假設您接近遊戲的某個層級，而且您想要開始預先載入紋理、著色器和其他資源，以進行下一個層級。</span><span class="sxs-lookup"><span data-stu-id="f0900-119">As an example of how one might use this API, say you are nearing the end of one level in your game and you want to begin preloading the textures, shaders, and other resources for the next level.</span></span> <span data-ttu-id="f0900-120">執行緒抽取將開始在個別執行緒上載入、解壓縮和處理資源和著色器，直到它們準備好設定至裝置為止，此時會將它們保留在佇列中。</span><span class="sxs-lookup"><span data-stu-id="f0900-120">The thread pump will begin loading, decompressing, and processing the resources and shaders on a separate thread until they are ready to be set to the device, at which point it will leave them in a queue.</span></span> <span data-ttu-id="f0900-121">您可能不想要一次將所有資源和著色器設定為裝置，因為這可能會導致遊戲效能的明顯暫時變慢。</span><span class="sxs-lookup"><span data-stu-id="f0900-121">One may not want to set all the resources and shaders to the device at once because this may cause a noticable temporary slow down in the game's performance.</span></span> <span data-ttu-id="f0900-122">因此，每個框架可呼叫此 API 一次，如此一來，就只會在每個畫面上將一個小數位的工作專案設定為裝置，藉此將系結資源的工作負載分散到裝置上的數個框架，並將遊戲效能降低明顯的可能性降至最低。</span><span class="sxs-lookup"><span data-stu-id="f0900-122">So, this API could be called once per frame so that only a small number work items would be set to the device on each frame, thereby spreading the work load of binding resources to the device over several frames and minimizing the possibility of a noticable slow down in the game's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0900-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0900-123">Requirements</span></span>



| <span data-ttu-id="f0900-124">需求</span><span class="sxs-lookup"><span data-stu-id="f0900-124">Requirement</span></span> | <span data-ttu-id="f0900-125">值</span><span class="sxs-lookup"><span data-stu-id="f0900-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0900-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f0900-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f0900-127"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0900-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0900-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="f0900-128">Library</span></span><br/> | <dl> <span data-ttu-id="f0900-129"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0900-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0900-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0900-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0900-131">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="f0900-131">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="f0900-132">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="f0900-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
