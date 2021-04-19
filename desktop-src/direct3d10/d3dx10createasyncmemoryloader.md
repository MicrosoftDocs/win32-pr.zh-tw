---
description: 建立異步記憶體載入器。
ms.assetid: 92177390-cb09-445e-9828-806a23ef91b5
title: 'D3DX10CreateAsyncMemoryLoader 函式 (D3DX10Async) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncMemoryLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 0219026eabfcff6dfcec0df4721716302f09f5e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986104"
---
# <a name="d3dx10createasyncmemoryloader-function"></a><span data-ttu-id="6b601-103">D3DX10CreateAsyncMemoryLoader 函式</span><span class="sxs-lookup"><span data-stu-id="6b601-103">D3DX10CreateAsyncMemoryLoader function</span></span>

<span data-ttu-id="6b601-104">建立異步記憶體載入器。</span><span class="sxs-lookup"><span data-stu-id="6b601-104">Create an asynchronous-memory loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b601-105">語法</span><span class="sxs-lookup"><span data-stu-id="6b601-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="6b601-106">參數</span><span class="sxs-lookup"><span data-stu-id="6b601-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b601-107">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6b601-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b601-108">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b601-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b601-109">資料的指標。</span><span class="sxs-lookup"><span data-stu-id="6b601-109">Pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="6b601-110">*cbData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6b601-110">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b601-111">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b601-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b601-112">資料的大小。</span><span class="sxs-lookup"><span data-stu-id="6b601-112">Size of the data.</span></span>

</dd> <dt>

<span data-ttu-id="6b601-113">*ppDataLoader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6b601-113">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b601-114">類型： **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6b601-114">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="6b601-115">非同步資料處理器指標的位址 (參閱 [**ID3DX10DataProcessor 介面**](id3dx10dataprocessor.md)) 。</span><span class="sxs-lookup"><span data-stu-id="6b601-115">The address of a pointer to the asynchronous-data processor (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b601-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b601-116">Return value</span></span>

<span data-ttu-id="6b601-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6b601-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6b601-118">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6b601-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b601-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b601-119">Requirements</span></span>



| <span data-ttu-id="6b601-120">需求</span><span class="sxs-lookup"><span data-stu-id="6b601-120">Requirement</span></span> | <span data-ttu-id="6b601-121">值</span><span class="sxs-lookup"><span data-stu-id="6b601-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b601-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6b601-122">Header</span></span><br/> | <dl> <span data-ttu-id="6b601-123"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="6b601-123"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b601-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b601-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b601-125">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="6b601-125">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
