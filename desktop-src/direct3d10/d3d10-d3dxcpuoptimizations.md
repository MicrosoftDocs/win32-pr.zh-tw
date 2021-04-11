---
description: 啟用或停用 CPU 優化。
ms.assetid: 6f73df12-f2fc-4651-b0f7-f7a55e534d3d
title: 'D3DXCpuOptimizations 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCpuOptimizations
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0ef276e6d3303acd77c9580b55a9aa49dbe2087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696744"
---
# <a name="d3dxcpuoptimizations-function"></a><span data-ttu-id="960fa-103">D3DXCpuOptimizations 函式</span><span class="sxs-lookup"><span data-stu-id="960fa-103">D3DXCpuOptimizations function</span></span>

<span data-ttu-id="960fa-104">啟用或停用 CPU 優化。</span><span class="sxs-lookup"><span data-stu-id="960fa-104">Enables or disables CPU optimizations.</span></span>

## <a name="syntax"></a><span data-ttu-id="960fa-105">語法</span><span class="sxs-lookup"><span data-stu-id="960fa-105">Syntax</span></span>


```C++
D3DX_CPU_OPTIMIZATION D3DXCpuOptimizations(
  _In_ BOOL Enable
);
```



## <a name="parameters"></a><span data-ttu-id="960fa-106">參數</span><span class="sxs-lookup"><span data-stu-id="960fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="960fa-107">*啟用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="960fa-107">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="960fa-108">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="960fa-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="960fa-109">**TRUE** 表示啟用 CPU 優化;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="960fa-109">**TRUE** to enable CPU optimizations; otherwise **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="960fa-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="960fa-110">Return value</span></span>

<span data-ttu-id="960fa-111">類型： **[ **D3DX \_ CPU \_ 優化**](d3dx-cpu-optimization.md)**</span><span class="sxs-lookup"><span data-stu-id="960fa-111">Type: **[**D3DX\_CPU\_OPTIMIZATION**](d3dx-cpu-optimization.md)**</span></span>

<span data-ttu-id="960fa-112">傳回偵測到的 CPU 類型，以及有哪些優化 (參閱 [**D3DX \_ CPU \_ 優化**](d3dx-cpu-optimization.md)) 。</span><span class="sxs-lookup"><span data-stu-id="960fa-112">Returns the type of CPU detected, and for which optimizations exist (see [**D3DX\_CPU\_OPTIMIZATION**](d3dx-cpu-optimization.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="960fa-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="960fa-113">Requirements</span></span>



| <span data-ttu-id="960fa-114">需求</span><span class="sxs-lookup"><span data-stu-id="960fa-114">Requirement</span></span> | <span data-ttu-id="960fa-115">值</span><span class="sxs-lookup"><span data-stu-id="960fa-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="960fa-116">標頭</span><span class="sxs-lookup"><span data-stu-id="960fa-116">Header</span></span><br/>  | <dl> <span data-ttu-id="960fa-117"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="960fa-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="960fa-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="960fa-118">Library</span></span><br/> | <dl> <span data-ttu-id="960fa-119"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="960fa-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="960fa-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="960fa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="960fa-121">數學函數</span><span class="sxs-lookup"><span data-stu-id="960fa-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
