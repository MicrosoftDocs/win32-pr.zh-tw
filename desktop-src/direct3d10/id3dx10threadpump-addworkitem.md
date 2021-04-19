---
description: 將工作專案加入至執行緒抽取。
ms.assetid: f07789dc-a3d5-4bad-9768-527e701271b8
title: 'ID3DX10ThreadPump：： Azuretasks 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.AddWorkItem
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aaf5286ca6cf7b61b0027b176d9a9261bd0beaa8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988623"
---
# <a name="id3dx10threadpumpaddworkitem-method"></a><span data-ttu-id="8a432-103">ID3DX10ThreadPump：： Azuretasks 方法</span><span class="sxs-lookup"><span data-stu-id="8a432-103">ID3DX10ThreadPump::AddWorkItem method</span></span>

<span data-ttu-id="8a432-104">將工作專案加入至執行緒抽取。</span><span class="sxs-lookup"><span data-stu-id="8a432-104">Add a work item to the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a432-105">語法</span><span class="sxs-lookup"><span data-stu-id="8a432-105">Syntax</span></span>


```C++
HRESULT AddWorkItem(
  [in]  ID3DX10DataLoader    *pDataLoader,
  [in]  ID3DX10DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a><span data-ttu-id="8a432-106">參數</span><span class="sxs-lookup"><span data-stu-id="8a432-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a432-107">*pDataLoader* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8a432-107">*pDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a432-108">類型： **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a432-108">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\***</span></span>

<span data-ttu-id="8a432-109">當工作專案需要載入資料時，執行緒抽取將使用的載入器。</span><span class="sxs-lookup"><span data-stu-id="8a432-109">The loader that the thread pump will use when a work item requires data to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="8a432-110">*pDataProcessor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8a432-110">*pDataProcessor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a432-111">類型： **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a432-111">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***</span></span>

<span data-ttu-id="8a432-112">當工作專案需要處理資料時，執行緒抽取將使用的處理器。</span><span class="sxs-lookup"><span data-stu-id="8a432-112">The processor that the thread pump will use when a work item requires data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="8a432-113">*pHResult* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8a432-113">*pHResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a432-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="8a432-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="8a432-115">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="8a432-115">A pointer to the return value.</span></span> <span data-ttu-id="8a432-116">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8a432-116">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8a432-117">*ppDeviceObject* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8a432-117">*ppDeviceObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a432-118">類型： **void \* \***</span><span class="sxs-lookup"><span data-stu-id="8a432-118">Type: **void\*\***</span></span>

<span data-ttu-id="8a432-119">使用物件的裝置。</span><span class="sxs-lookup"><span data-stu-id="8a432-119">The device that uses the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a432-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a432-120">Return value</span></span>

<span data-ttu-id="8a432-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8a432-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8a432-122">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8a432-122">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a432-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a432-123">Requirements</span></span>



| <span data-ttu-id="8a432-124">需求</span><span class="sxs-lookup"><span data-stu-id="8a432-124">Requirement</span></span> | <span data-ttu-id="8a432-125">值</span><span class="sxs-lookup"><span data-stu-id="8a432-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a432-126">標頭</span><span class="sxs-lookup"><span data-stu-id="8a432-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8a432-127"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="8a432-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a432-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="8a432-128">Library</span></span><br/> | <dl> <span data-ttu-id="8a432-129"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a432-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a432-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a432-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a432-131">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="8a432-131">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="8a432-132">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="8a432-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




