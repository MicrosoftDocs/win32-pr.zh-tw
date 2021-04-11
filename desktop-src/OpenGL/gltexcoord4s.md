---
title: 'glTexCoord4s 函式 (Gl) '
description: '設定目前的材質座標。 |glTexCoord4s 函式 (Gl) '
ms.assetid: 948c63f5-a94d-4e55-9aa4-a320452fc29f
keywords:
- glTexCoord4s 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a164b091c62b31523baa5be96d1578e1cbfa80
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853839"
---
# <a name="gltexcoord4s-function"></a><span data-ttu-id="8e610-105">glTexCoord4s 函式</span><span class="sxs-lookup"><span data-stu-id="8e610-105">glTexCoord4s function</span></span>

<span data-ttu-id="8e610-106">設定目前的材質座標。</span><span class="sxs-lookup"><span data-stu-id="8e610-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e610-107">語法</span><span class="sxs-lookup"><span data-stu-id="8e610-107">Syntax</span></span>


```C++
void WINAPI glTexCoord4s(
   GLshort s,
   GLshort t,
   GLshort r,
   GLshort q
);
```



## <a name="parameters"></a><span data-ttu-id="8e610-108">參數</span><span class="sxs-lookup"><span data-stu-id="8e610-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e610-109">*s*</span><span class="sxs-lookup"><span data-stu-id="8e610-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="8e610-110">S 材質座標。</span><span class="sxs-lookup"><span data-stu-id="8e610-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="8e610-111">*t*</span><span class="sxs-lookup"><span data-stu-id="8e610-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="8e610-112">T 材質座標。</span><span class="sxs-lookup"><span data-stu-id="8e610-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="8e610-113">*r*</span><span class="sxs-lookup"><span data-stu-id="8e610-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="8e610-114">R 材質座標。</span><span class="sxs-lookup"><span data-stu-id="8e610-114">The r texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="8e610-115">*問*</span><span class="sxs-lookup"><span data-stu-id="8e610-115">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="8e610-116">Q 紋理座標。</span><span class="sxs-lookup"><span data-stu-id="8e610-116">The q texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e610-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e610-117">Return value</span></span>

<span data-ttu-id="8e610-118">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8e610-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e610-119">備註</span><span class="sxs-lookup"><span data-stu-id="8e610-119">Remarks</span></span>

<span data-ttu-id="8e610-120">[**GlTexCoord**](gltexcoord-functions.md)函式會將目前的材質座標設定為與多邊形頂點相關聯之資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="8e610-120">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="8e610-121">**GlTexCoord** 函數會指定一、二、三或四個維度中的材質座標。</span><span class="sxs-lookup"><span data-stu-id="8e610-121">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="8e610-122">GlTexCoord1 函式會將目前的材質座標設定為 (s、0、0、1) ;對 glTexCoord2 的呼叫會將它們設定為 (s、t、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="8e610-122">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="8e610-123">同樣地，glTexCoord3 會將材質座標指定為 (s、t、r、1) ，而 glTexCoord4 會將所有四個元件明確定義為 (s、t、r、q) 。</span><span class="sxs-lookup"><span data-stu-id="8e610-123">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="8e610-124">您可以隨時更新目前的材質座標。</span><span class="sxs-lookup"><span data-stu-id="8e610-124">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="8e610-125">尤其是，您可以呼叫 [**glBegin**](glbegin.md) 的呼叫與 [**glEnd**](glend.md)的對應呼叫之間的 glTexCoord。</span><span class="sxs-lookup"><span data-stu-id="8e610-125">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="8e610-126">下列函式會抓取 **glTexCoord** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="8e610-126">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="8e610-127">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 材質 \_ COORDS 的 glGet</span><span class="sxs-lookup"><span data-stu-id="8e610-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="8e610-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e610-128">Requirements</span></span>



| <span data-ttu-id="8e610-129">需求</span><span class="sxs-lookup"><span data-stu-id="8e610-129">Requirement</span></span> | <span data-ttu-id="8e610-130">值</span><span class="sxs-lookup"><span data-stu-id="8e610-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e610-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e610-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8e610-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e610-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8e610-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e610-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8e610-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e610-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8e610-135">標頭</span><span class="sxs-lookup"><span data-stu-id="8e610-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e610-136"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="8e610-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8e610-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="8e610-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="8e610-138"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e610-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8e610-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8e610-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e610-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e610-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e610-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e610-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e610-142">glVertex</span><span class="sxs-lookup"><span data-stu-id="8e610-142">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





