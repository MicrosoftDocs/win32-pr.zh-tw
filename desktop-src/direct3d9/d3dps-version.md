---
description: 建立圖元著色器版本戳記。
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: 'D3DPS_VERSION 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3f30d673145ec9dfe38bd8e2a636ac04c9a195a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322996"
---
# <a name="d3dps_version-macro"></a><span data-ttu-id="5c8eb-103">D3DPS \_ 版本宏</span><span class="sxs-lookup"><span data-stu-id="5c8eb-103">D3DPS\_VERSION macro</span></span>

<span data-ttu-id="5c8eb-104">建立圖元著色器版本戳記。</span><span class="sxs-lookup"><span data-stu-id="5c8eb-104">Create a pixel shader version token.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c8eb-105">語法</span><span class="sxs-lookup"><span data-stu-id="5c8eb-105">Syntax</span></span>


```C++
DWORD D3DPS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a><span data-ttu-id="5c8eb-106">參數</span><span class="sxs-lookup"><span data-stu-id="5c8eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c8eb-107">*\_主要*</span><span class="sxs-lookup"><span data-stu-id="5c8eb-107">*\_Major*</span></span> 
</dt> <dd>

<span data-ttu-id="5c8eb-108">主要圖元著色器版本。</span><span class="sxs-lookup"><span data-stu-id="5c8eb-108">The major pixel shader version.</span></span>

</dd> <dt>

<span data-ttu-id="5c8eb-109">*\_Minor*</span><span class="sxs-lookup"><span data-stu-id="5c8eb-109">*\_Minor*</span></span> 
</dt> <dd>

<span data-ttu-id="5c8eb-110">次要圖元著色器版本。</span><span class="sxs-lookup"><span data-stu-id="5c8eb-110">The minor pixel shader version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c8eb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c8eb-111">Return value</span></span>

<span data-ttu-id="5c8eb-112">傳回是圖元著色器版本的 DWORD 值。</span><span class="sxs-lookup"><span data-stu-id="5c8eb-112">Returns a DWORD value that is a pixel shader version.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c8eb-113">備註</span><span class="sxs-lookup"><span data-stu-id="5c8eb-113">Remarks</span></span>

<span data-ttu-id="5c8eb-114">版本號碼</span><span class="sxs-lookup"><span data-stu-id="5c8eb-114">Version Numbers</span></span>

<span data-ttu-id="5c8eb-115">版本號碼是主要版本和次要頂點著色器版本號碼的組合。</span><span class="sxs-lookup"><span data-stu-id="5c8eb-115">The version number is a combination of the major version and the minor vertex shader version numbers.</span></span> <span data-ttu-id="5c8eb-116">有效的數位會顯示在表格中。</span><span class="sxs-lookup"><span data-stu-id="5c8eb-116">Valid numbers are shown in the table.</span></span>



| <span data-ttu-id="5c8eb-117">主要</span><span class="sxs-lookup"><span data-stu-id="5c8eb-117">Major</span></span> | <span data-ttu-id="5c8eb-118">Minor</span><span class="sxs-lookup"><span data-stu-id="5c8eb-118">Minor</span></span> | <span data-ttu-id="5c8eb-119">範例</span><span class="sxs-lookup"><span data-stu-id="5c8eb-119">Example</span></span>             |
|-------|-------|---------------------|
| <span data-ttu-id="5c8eb-120">1</span><span class="sxs-lookup"><span data-stu-id="5c8eb-120">1</span></span>     | <span data-ttu-id="5c8eb-121">1</span><span class="sxs-lookup"><span data-stu-id="5c8eb-121">1</span></span>     | <span data-ttu-id="5c8eb-122">D3DPS \_ 版本 (1，1) </span><span class="sxs-lookup"><span data-stu-id="5c8eb-122">D3DPS\_VERSION(1,1)</span></span> |
| <span data-ttu-id="5c8eb-123">1</span><span class="sxs-lookup"><span data-stu-id="5c8eb-123">1</span></span>     | <span data-ttu-id="5c8eb-124">2</span><span class="sxs-lookup"><span data-stu-id="5c8eb-124">2</span></span>     | <span data-ttu-id="5c8eb-125">D3DPS \_ 版本 (1、2) </span><span class="sxs-lookup"><span data-stu-id="5c8eb-125">D3DPS\_VERSION(1,2)</span></span> |
| <span data-ttu-id="5c8eb-126">1</span><span class="sxs-lookup"><span data-stu-id="5c8eb-126">1</span></span>     | <span data-ttu-id="5c8eb-127">3</span><span class="sxs-lookup"><span data-stu-id="5c8eb-127">3</span></span>     | <span data-ttu-id="5c8eb-128">D3DPS \_ 版本 (1，3) </span><span class="sxs-lookup"><span data-stu-id="5c8eb-128">D3DPS\_VERSION(1,3)</span></span> |
| <span data-ttu-id="5c8eb-129">1</span><span class="sxs-lookup"><span data-stu-id="5c8eb-129">1</span></span>     | <span data-ttu-id="5c8eb-130">4</span><span class="sxs-lookup"><span data-stu-id="5c8eb-130">4</span></span>     | <span data-ttu-id="5c8eb-131">D3DPS \_ 版本 (1、4) </span><span class="sxs-lookup"><span data-stu-id="5c8eb-131">D3DPS\_VERSION(1,4)</span></span> |
| <span data-ttu-id="5c8eb-132">2</span><span class="sxs-lookup"><span data-stu-id="5c8eb-132">2</span></span>     | <span data-ttu-id="5c8eb-133">0</span><span class="sxs-lookup"><span data-stu-id="5c8eb-133">0</span></span>     | <span data-ttu-id="5c8eb-134">D3DPS \_ 版本 (2，0) </span><span class="sxs-lookup"><span data-stu-id="5c8eb-134">D3DPS\_VERSION(2,0)</span></span> |
| <span data-ttu-id="5c8eb-135">3</span><span class="sxs-lookup"><span data-stu-id="5c8eb-135">3</span></span>     | <span data-ttu-id="5c8eb-136">0</span><span class="sxs-lookup"><span data-stu-id="5c8eb-136">0</span></span>     | <span data-ttu-id="5c8eb-137">D3DPS \_ 版本 (3，0) </span><span class="sxs-lookup"><span data-stu-id="5c8eb-137">D3DPS\_VERSION(3,0)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="5c8eb-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c8eb-138">Requirements</span></span>



| <span data-ttu-id="5c8eb-139">需求</span><span class="sxs-lookup"><span data-stu-id="5c8eb-139">Requirement</span></span> | <span data-ttu-id="5c8eb-140">值</span><span class="sxs-lookup"><span data-stu-id="5c8eb-140">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c8eb-141">標頭</span><span class="sxs-lookup"><span data-stu-id="5c8eb-141">Header</span></span><br/> | <dl> <span data-ttu-id="5c8eb-142"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c8eb-142"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c8eb-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c8eb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c8eb-144">巨集</span><span class="sxs-lookup"><span data-stu-id="5c8eb-144">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="5c8eb-145">D3DCAPS9</span><span class="sxs-lookup"><span data-stu-id="5c8eb-145">D3DCAPS9</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




