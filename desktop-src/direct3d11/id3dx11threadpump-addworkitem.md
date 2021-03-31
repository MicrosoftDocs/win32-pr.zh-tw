---
title: 'ID3DX11ThreadPump Azuretasks 方法 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 將工作專案加入至執行緒抽取。
ms.assetid: 2578506c-6175-457a-bf10-94929bb3c0c4
keywords:
- Azuretasks 方法 Direct3D 11
- Azuretasks 方法 Direct3D 11，ID3DX11ThreadPump 介面
- ID3DX11ThreadPump 介面 Direct3D 11，Azuretasks 方法
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.AddWorkItem
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf249405bd71287f93444ae8d23dab694027360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322687"
---
# <a name="id3dx11threadpumpaddworkitem-method"></a><span data-ttu-id="7ef34-107">ID3DX11ThreadPump：： Azuretasks 方法</span><span class="sxs-lookup"><span data-stu-id="7ef34-107">ID3DX11ThreadPump::AddWorkItem method</span></span>

> [!Note]  
> <span data-ttu-id="7ef34-108">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="7ef34-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="7ef34-109">將工作專案加入至執行緒抽取。</span><span class="sxs-lookup"><span data-stu-id="7ef34-109">Adds a work item to the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ef34-110">語法</span><span class="sxs-lookup"><span data-stu-id="7ef34-110">Syntax</span></span>


```C++
HRESULT AddWorkItem(
  [in]  ID3DX11DataLoader    *pDataLoader,
  [in]  ID3DX11DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a><span data-ttu-id="7ef34-111">參數</span><span class="sxs-lookup"><span data-stu-id="7ef34-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ef34-112">*pDataLoader* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ef34-112">*pDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ef34-113">類型： **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ef34-113">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\***</span></span>

<span data-ttu-id="7ef34-114">當工作專案需要載入資料時，執行緒抽取將使用的載入器。</span><span class="sxs-lookup"><span data-stu-id="7ef34-114">The loader that the thread pump will use when a work item requires data to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="7ef34-115">*pDataProcessor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ef34-115">*pDataProcessor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ef34-116">類型： **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ef34-116">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***</span></span>

<span data-ttu-id="7ef34-117">當工作專案需要處理資料時，執行緒抽取將使用的處理器。</span><span class="sxs-lookup"><span data-stu-id="7ef34-117">The processor that the thread pump will use when a work item requires data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="7ef34-118">*pHResult* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ef34-118">*pHResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ef34-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="7ef34-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="7ef34-120">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="7ef34-120">A pointer to the return value.</span></span> <span data-ttu-id="7ef34-121">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7ef34-121">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7ef34-122">*ppDeviceObject* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7ef34-122">*ppDeviceObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ef34-123">類型： **void \* \***</span><span class="sxs-lookup"><span data-stu-id="7ef34-123">Type: **void\*\***</span></span>

<span data-ttu-id="7ef34-124">使用物件的裝置。</span><span class="sxs-lookup"><span data-stu-id="7ef34-124">The device that uses the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ef34-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ef34-125">Return value</span></span>

<span data-ttu-id="7ef34-126">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ef34-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ef34-127">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7ef34-127">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ef34-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ef34-128">Requirements</span></span>



| <span data-ttu-id="7ef34-129">需求</span><span class="sxs-lookup"><span data-stu-id="7ef34-129">Requirement</span></span> | <span data-ttu-id="7ef34-130">值</span><span class="sxs-lookup"><span data-stu-id="7ef34-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ef34-131">標頭</span><span class="sxs-lookup"><span data-stu-id="7ef34-131">Header</span></span><br/>  | <dl> <span data-ttu-id="7ef34-132"><dt>D3DX11core。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ef34-132"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="7ef34-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="7ef34-133">Library</span></span><br/> | <dl> <span data-ttu-id="7ef34-134"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ef34-134"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7ef34-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ef34-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ef34-136">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="7ef34-136">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="7ef34-137">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="7ef34-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





