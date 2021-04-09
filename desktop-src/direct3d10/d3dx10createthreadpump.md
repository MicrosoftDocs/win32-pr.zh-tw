---
description: 建立執行緒抽取。
ms.assetid: a7a016e2-784d-4d7a-8058-88895bf3c4e2
title: 'D3DX10CreateThreadPump 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateThreadPump
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a27f8df1f4eaa8e7f41e863d703063308f9c595
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946219"
---
# <a name="d3dx10createthreadpump-function"></a><span data-ttu-id="8b5ff-103">D3DX10CreateThreadPump 函式</span><span class="sxs-lookup"><span data-stu-id="8b5ff-103">D3DX10CreateThreadPump function</span></span>

<span data-ttu-id="8b5ff-104">建立執行緒抽取。</span><span class="sxs-lookup"><span data-stu-id="8b5ff-104">Create a thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b5ff-105">語法</span><span class="sxs-lookup"><span data-stu-id="8b5ff-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX10ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a><span data-ttu-id="8b5ff-106">參數</span><span class="sxs-lookup"><span data-stu-id="8b5ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b5ff-107">*cIoThreads* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b5ff-107">*cIoThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5ff-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5ff-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b5ff-109">要建立的 i/o 執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="8b5ff-109">The number of I/O threads to create.</span></span> <span data-ttu-id="8b5ff-110">如果指定0，Direct3D 將會根據硬體設定嘗試計算最佳的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="8b5ff-110">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="8b5ff-111">*cProcThreads* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b5ff-111">*cProcThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5ff-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5ff-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b5ff-113">要建立的進程執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="8b5ff-113">The number of process threads to create.</span></span> <span data-ttu-id="8b5ff-114">如果指定0，Direct3D 將會根據硬體設定嘗試計算最佳的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="8b5ff-114">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="8b5ff-115">*ppThreadPump* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8b5ff-115">*ppThreadPump* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5ff-116">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="8b5ff-116">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***</span></span>

<span data-ttu-id="8b5ff-117">建立的執行緒抽取。</span><span class="sxs-lookup"><span data-stu-id="8b5ff-117">The created thread pump.</span></span> <span data-ttu-id="8b5ff-118">請參閱 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)。</span><span class="sxs-lookup"><span data-stu-id="8b5ff-118">See [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b5ff-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b5ff-119">Return value</span></span>

<span data-ttu-id="8b5ff-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8b5ff-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8b5ff-121">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8b5ff-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8b5ff-122">備註</span><span class="sxs-lookup"><span data-stu-id="8b5ff-122">Remarks</span></span>

<span data-ttu-id="8b5ff-123">執行緒抽取是非常耗費資源的物件。</span><span class="sxs-lookup"><span data-stu-id="8b5ff-123">A thread pump is a very resource-intensive object.</span></span> <span data-ttu-id="8b5ff-124">每個應用程式只應建立一個執行緒抽取。</span><span class="sxs-lookup"><span data-stu-id="8b5ff-124">Only one thread pump should be created per application.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b5ff-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b5ff-125">Requirements</span></span>



| <span data-ttu-id="8b5ff-126">需求</span><span class="sxs-lookup"><span data-stu-id="8b5ff-126">Requirement</span></span> | <span data-ttu-id="8b5ff-127">值</span><span class="sxs-lookup"><span data-stu-id="8b5ff-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b5ff-128">標頭</span><span class="sxs-lookup"><span data-stu-id="8b5ff-128">Header</span></span><br/>  | <dl> <span data-ttu-id="8b5ff-129"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="8b5ff-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b5ff-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="8b5ff-130">Library</span></span><br/> | <dl> <span data-ttu-id="8b5ff-131"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b5ff-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b5ff-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b5ff-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b5ff-133">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="8b5ff-133">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
