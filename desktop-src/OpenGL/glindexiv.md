---
title: 'glIndexiv 函式 (Gl) '
description: GlIndexiv 函數會設定目前的色彩索引。
ms.assetid: 642c243f-046d-474e-8075-ef5692797020
keywords:
- glIndexiv 函式 OpenGL
topic_type:
- apiref
api_name:
- glIndexiv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf4a4f4bb798a1a93e9d3e31c66b9245a868afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969570"
---
# <a name="glindexiv-function"></a><span data-ttu-id="687d4-104">glIndexiv 函式</span><span class="sxs-lookup"><span data-stu-id="687d4-104">glIndexiv function</span></span>

<span data-ttu-id="687d4-105">**GlIndexiv** 函數會設定目前的色彩索引。</span><span class="sxs-lookup"><span data-stu-id="687d4-105">The **glIndexiv** function sets the current color index.</span></span>

## <a name="syntax"></a><span data-ttu-id="687d4-106">語法</span><span class="sxs-lookup"><span data-stu-id="687d4-106">Syntax</span></span>


```C++
void WINAPI glIndexiv(
   const GLint *c
);
```



## <a name="parameters"></a><span data-ttu-id="687d4-107">參數</span><span class="sxs-lookup"><span data-stu-id="687d4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="687d4-108">*c*</span><span class="sxs-lookup"><span data-stu-id="687d4-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="687d4-109">一個元素陣列的指標，其中包含目前色彩索引的新值。</span><span class="sxs-lookup"><span data-stu-id="687d4-109">A pointer to a one-element array that contains the new value for the current color index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="687d4-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="687d4-110">Return value</span></span>

<span data-ttu-id="687d4-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="687d4-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="687d4-112">備註</span><span class="sxs-lookup"><span data-stu-id="687d4-112">Remarks</span></span>

<span data-ttu-id="687d4-113">**GlIndexiv** 函式會更新目前 (單一值) 色彩索引。</span><span class="sxs-lookup"><span data-stu-id="687d4-113">The **glIndexiv** function updates the current (single-valued) color index.</span></span> <span data-ttu-id="687d4-114">它會採用一個引數：目前色彩索引的新值。</span><span class="sxs-lookup"><span data-stu-id="687d4-114">It takes one argument: the new value for the current color index.</span></span>

<span data-ttu-id="687d4-115">目前的索引會儲存為浮點值。</span><span class="sxs-lookup"><span data-stu-id="687d4-115">The current index is stored as a floating-point value.</span></span> <span data-ttu-id="687d4-116">整數值會直接轉換為浮點值，沒有特殊對應。</span><span class="sxs-lookup"><span data-stu-id="687d4-116">Integer values are converted directly to floating-point values, with no special mapping.</span></span>

<span data-ttu-id="687d4-117">未壓制在色彩索引緩衝區可表示範圍之外的索引值。</span><span class="sxs-lookup"><span data-stu-id="687d4-117">Index values outside the representable range of the color-index buffer are not clamped.</span></span> <span data-ttu-id="687d4-118">不過，索引在遞色之前 (如果啟用) 並寫入至畫面格緩衝區，則會轉換成固定點格式。</span><span class="sxs-lookup"><span data-stu-id="687d4-118">However, before an index is dithered (if enabled) and written to the framebuffer, it is converted to fixed-point format.</span></span> <span data-ttu-id="687d4-119">在結果固定點值（未對應到畫面格緩衝區中的位）的整數部分中，任何位都會被遮罩掉。</span><span class="sxs-lookup"><span data-stu-id="687d4-119">Any bits in the integer portion of the resulting fixed-point value that do not correspond to bits in the framebuffer are masked out.</span></span>

<span data-ttu-id="687d4-120">您可以隨時更新目前的索引。</span><span class="sxs-lookup"><span data-stu-id="687d4-120">The current index can be updated at any time.</span></span> <span data-ttu-id="687d4-121">尤其是，在呼叫 [**glBegin**](/windows/desktop/OpenGL/glbegin)和對應的 [**glEnd**](glend.md)呼叫之間，可以呼叫 **glIndexiv** 。</span><span class="sxs-lookup"><span data-stu-id="687d4-121">In particular, **glIndexiv** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](glend.md).</span></span>

<span data-ttu-id="687d4-122">下列函式會抓取 **glIndexiv** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="687d4-122">The following function retrieves information related to **glIndexiv**:</span></span>

<span data-ttu-id="687d4-123">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 索引的 glGet</span><span class="sxs-lookup"><span data-stu-id="687d4-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_INDEX</span></span>

## <a name="requirements"></a><span data-ttu-id="687d4-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="687d4-124">Requirements</span></span>



| <span data-ttu-id="687d4-125">需求</span><span class="sxs-lookup"><span data-stu-id="687d4-125">Requirement</span></span> | <span data-ttu-id="687d4-126">值</span><span class="sxs-lookup"><span data-stu-id="687d4-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="687d4-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="687d4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="687d4-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="687d4-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="687d4-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="687d4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="687d4-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="687d4-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="687d4-131">標頭</span><span class="sxs-lookup"><span data-stu-id="687d4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="687d4-132"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="687d4-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="687d4-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="687d4-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="687d4-134"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="687d4-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="687d4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="687d4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="687d4-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="687d4-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="687d4-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="687d4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="687d4-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="687d4-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="687d4-139">**glColor**</span><span class="sxs-lookup"><span data-stu-id="687d4-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="687d4-140">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="687d4-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="687d4-141">**glGet**</span><span class="sxs-lookup"><span data-stu-id="687d4-141">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

