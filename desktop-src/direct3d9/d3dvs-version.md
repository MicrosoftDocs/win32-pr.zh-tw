---
description: 建立頂點著色器版本號碼權杖。
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: 'D3DVS_VERSION 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 915d5b843287602c80572d739d8b369d8c301770
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991479"
---
# <a name="d3dvs_version-macro"></a><span data-ttu-id="5ba3a-103">D3DVS \_ 版本宏</span><span class="sxs-lookup"><span data-stu-id="5ba3a-103">D3DVS\_VERSION macro</span></span>

<span data-ttu-id="5ba3a-104">建立頂點著色器版本號碼權杖。</span><span class="sxs-lookup"><span data-stu-id="5ba3a-104">Create a vertex shader version number token.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ba3a-105">語法</span><span class="sxs-lookup"><span data-stu-id="5ba3a-105">Syntax</span></span>


```C++
DWORD D3DVS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a><span data-ttu-id="5ba3a-106">參數</span><span class="sxs-lookup"><span data-stu-id="5ba3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ba3a-107">*\_主要*</span><span class="sxs-lookup"><span data-stu-id="5ba3a-107">*\_Major*</span></span> 
</dt> <dd>

<span data-ttu-id="5ba3a-108">主要頂點著色器版本。</span><span class="sxs-lookup"><span data-stu-id="5ba3a-108">The major vertex shader version.</span></span> <span data-ttu-id="5ba3a-109">請參閱備註以取得適當的值。</span><span class="sxs-lookup"><span data-stu-id="5ba3a-109">See remarks for appropriate values.</span></span>

</dd> <dt>

<span data-ttu-id="5ba3a-110">*\_Minor*</span><span class="sxs-lookup"><span data-stu-id="5ba3a-110">*\_Minor*</span></span> 
</dt> <dd>

<span data-ttu-id="5ba3a-111">次要頂點著色器版本。</span><span class="sxs-lookup"><span data-stu-id="5ba3a-111">The minor vertex shader version.</span></span> <span data-ttu-id="5ba3a-112">請參閱備註以取得適當的值。</span><span class="sxs-lookup"><span data-stu-id="5ba3a-112">See remarks for appropriate values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ba3a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5ba3a-113">Return value</span></span>

<span data-ttu-id="5ba3a-114">傳回做為頂點著色器版本的 DWORD 值。</span><span class="sxs-lookup"><span data-stu-id="5ba3a-114">Returns a DWORD value that is a vertex shader version.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ba3a-115">備註</span><span class="sxs-lookup"><span data-stu-id="5ba3a-115">Remarks</span></span>

<span data-ttu-id="5ba3a-116">版本號碼</span><span class="sxs-lookup"><span data-stu-id="5ba3a-116">Version Numbers</span></span>

<span data-ttu-id="5ba3a-117">版本號碼是主要版本和次要頂點著色器版本號碼的組合。</span><span class="sxs-lookup"><span data-stu-id="5ba3a-117">The version number is a combination of the major version and the minor vertex shader version numbers.</span></span> <span data-ttu-id="5ba3a-118">有效的數位會顯示在表格中。</span><span class="sxs-lookup"><span data-stu-id="5ba3a-118">Valid numbers are shown in the table.</span></span>



| <span data-ttu-id="5ba3a-119">主要</span><span class="sxs-lookup"><span data-stu-id="5ba3a-119">Major</span></span> | <span data-ttu-id="5ba3a-120">Minor</span><span class="sxs-lookup"><span data-stu-id="5ba3a-120">Minor</span></span> | <span data-ttu-id="5ba3a-121">範例</span><span class="sxs-lookup"><span data-stu-id="5ba3a-121">Example</span></span>             |
|-------|-------|---------------------|
| <span data-ttu-id="5ba3a-122">1</span><span class="sxs-lookup"><span data-stu-id="5ba3a-122">1</span></span>     | <span data-ttu-id="5ba3a-123">1</span><span class="sxs-lookup"><span data-stu-id="5ba3a-123">1</span></span>     | <span data-ttu-id="5ba3a-124">D3DVS \_ 版本 (1，1) </span><span class="sxs-lookup"><span data-stu-id="5ba3a-124">D3DVS\_VERSION(1,1)</span></span> |
| <span data-ttu-id="5ba3a-125">2</span><span class="sxs-lookup"><span data-stu-id="5ba3a-125">2</span></span>     | <span data-ttu-id="5ba3a-126">0</span><span class="sxs-lookup"><span data-stu-id="5ba3a-126">0</span></span>     | <span data-ttu-id="5ba3a-127">D3DVS \_ 版本 (2，0) </span><span class="sxs-lookup"><span data-stu-id="5ba3a-127">D3DVS\_VERSION(2,0)</span></span> |
| <span data-ttu-id="5ba3a-128">3</span><span class="sxs-lookup"><span data-stu-id="5ba3a-128">3</span></span>     | <span data-ttu-id="5ba3a-129">0</span><span class="sxs-lookup"><span data-stu-id="5ba3a-129">0</span></span>     | <span data-ttu-id="5ba3a-130">D3DVS \_ 版本 (3，0) </span><span class="sxs-lookup"><span data-stu-id="5ba3a-130">D3DVS\_VERSION(3,0)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="5ba3a-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ba3a-131">Requirements</span></span>



| <span data-ttu-id="5ba3a-132">需求</span><span class="sxs-lookup"><span data-stu-id="5ba3a-132">Requirement</span></span> | <span data-ttu-id="5ba3a-133">值</span><span class="sxs-lookup"><span data-stu-id="5ba3a-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ba3a-134">標頭</span><span class="sxs-lookup"><span data-stu-id="5ba3a-134">Header</span></span><br/> | <dl> <span data-ttu-id="5ba3a-135"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="5ba3a-135"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ba3a-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ba3a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ba3a-137">巨集</span><span class="sxs-lookup"><span data-stu-id="5ba3a-137">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




