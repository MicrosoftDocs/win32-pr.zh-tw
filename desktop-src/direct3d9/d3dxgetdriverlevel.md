---
description: 傳回驅動程式層級。
ms.assetid: e8c85201-7850-4c8d-a124-ceb76d4e24d5
title: 'D3DXGetDriverLevel 函式 (D3dx9core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDriverLevel
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83f756f6b6ab5864f14e797879be243f871fb9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982012"
---
# <a name="d3dxgetdriverlevel-function"></a><span data-ttu-id="592fe-103">D3DXGetDriverLevel 函式</span><span class="sxs-lookup"><span data-stu-id="592fe-103">D3DXGetDriverLevel function</span></span>

<span data-ttu-id="592fe-104">傳回驅動程式層級。</span><span class="sxs-lookup"><span data-stu-id="592fe-104">Returns the driver level.</span></span>

## <a name="syntax"></a><span data-ttu-id="592fe-105">語法</span><span class="sxs-lookup"><span data-stu-id="592fe-105">Syntax</span></span>


```C++
UINT D3DXGetDriverLevel(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="592fe-106">參數</span><span class="sxs-lookup"><span data-stu-id="592fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="592fe-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="592fe-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="592fe-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="592fe-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="592fe-109">代表裝置之 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="592fe-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="592fe-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="592fe-110">Return value</span></span>

<span data-ttu-id="592fe-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="592fe-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="592fe-112">驅動程式層級。</span><span class="sxs-lookup"><span data-stu-id="592fe-112">The driver level.</span></span> <span data-ttu-id="592fe-113">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="592fe-113">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="592fe-114">備註</span><span class="sxs-lookup"><span data-stu-id="592fe-114">Remarks</span></span>

<span data-ttu-id="592fe-115">這個方法會傳回驅動程式版本，也就是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="592fe-115">This method returns the driver version, which is one of the following:</span></span>

-   <span data-ttu-id="592fe-116">700-Direct3D 7 層級驅動程式</span><span class="sxs-lookup"><span data-stu-id="592fe-116">700 - Direct3D 7 level driver</span></span>
-   <span data-ttu-id="592fe-117">800-Direct3D 8 層級驅動程式</span><span class="sxs-lookup"><span data-stu-id="592fe-117">800 - Direct3D 8 level driver</span></span>
-   <span data-ttu-id="592fe-118">900-Direct3D 9 層級的驅動程式</span><span class="sxs-lookup"><span data-stu-id="592fe-118">900 - Direct3D 9 level driver</span></span>

## <a name="requirements"></a><span data-ttu-id="592fe-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="592fe-119">Requirements</span></span>



| <span data-ttu-id="592fe-120">需求</span><span class="sxs-lookup"><span data-stu-id="592fe-120">Requirement</span></span> | <span data-ttu-id="592fe-121">值</span><span class="sxs-lookup"><span data-stu-id="592fe-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="592fe-122">標頭</span><span class="sxs-lookup"><span data-stu-id="592fe-122">Header</span></span><br/>  | <dl> <span data-ttu-id="592fe-123"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="592fe-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="592fe-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="592fe-124">Library</span></span><br/> | <dl> <span data-ttu-id="592fe-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="592fe-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="592fe-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="592fe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="592fe-127">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="592fe-127">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
