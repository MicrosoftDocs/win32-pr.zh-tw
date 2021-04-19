---
title: 'glIndexi 函式 (Gl) '
description: GlIndexi 函數會設定目前的色彩索引。
ms.assetid: c57d2316-4081-40d8-af50-ae0299597803
keywords:
- glIndexi 函式 OpenGL
topic_type:
- apiref
api_name:
- glIndexi
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6b40d8d0d96aac17c852fb266b23dec23d26c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965703"
---
# <a name="glindexi-function"></a><span data-ttu-id="3d094-104">glIndexi 函式</span><span class="sxs-lookup"><span data-stu-id="3d094-104">glIndexi function</span></span>

<span data-ttu-id="3d094-105">**GlIndexi** 函數會設定目前的色彩索引。</span><span class="sxs-lookup"><span data-stu-id="3d094-105">The **glIndexi** function sets the current color index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d094-106">語法</span><span class="sxs-lookup"><span data-stu-id="3d094-106">Syntax</span></span>


```C++
void WINAPI glIndexi(
   GLint c
);
```



## <a name="parameters"></a><span data-ttu-id="3d094-107">參數</span><span class="sxs-lookup"><span data-stu-id="3d094-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d094-108">*c*</span><span class="sxs-lookup"><span data-stu-id="3d094-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="3d094-109">目前色彩索引的新值。</span><span class="sxs-lookup"><span data-stu-id="3d094-109">The new value for the current color index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d094-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d094-110">Return value</span></span>

<span data-ttu-id="3d094-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3d094-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d094-112">備註</span><span class="sxs-lookup"><span data-stu-id="3d094-112">Remarks</span></span>

<span data-ttu-id="3d094-113">**GlIndexi** 函式會更新目前 (單一值) 色彩索引。</span><span class="sxs-lookup"><span data-stu-id="3d094-113">The **glIndexi** function updates the current (single-valued) color index.</span></span> <span data-ttu-id="3d094-114">它會採用一個引數：目前色彩索引的新值。</span><span class="sxs-lookup"><span data-stu-id="3d094-114">It takes one argument: the new value for the current color index.</span></span>

<span data-ttu-id="3d094-115">目前的索引會儲存為浮點值。</span><span class="sxs-lookup"><span data-stu-id="3d094-115">The current index is stored as a floating-point value.</span></span> <span data-ttu-id="3d094-116">整數值會直接轉換為浮點值，沒有特殊對應。</span><span class="sxs-lookup"><span data-stu-id="3d094-116">Integer values are converted directly to floating-point values, with no special mapping.</span></span>

<span data-ttu-id="3d094-117">未壓制在色彩索引緩衝區可表示範圍之外的索引值。</span><span class="sxs-lookup"><span data-stu-id="3d094-117">Index values outside the representable range of the color-index buffer are not clamped.</span></span> <span data-ttu-id="3d094-118">不過，索引在遞色之前 (如果啟用) 並寫入至畫面格緩衝區，則會轉換成固定點格式。</span><span class="sxs-lookup"><span data-stu-id="3d094-118">However, before an index is dithered (if enabled) and written to the framebuffer, it is converted to fixed-point format.</span></span> <span data-ttu-id="3d094-119">在結果固定點值（未對應到畫面格緩衝區中的位）的整數部分中，任何位都會被遮罩掉。</span><span class="sxs-lookup"><span data-stu-id="3d094-119">Any bits in the integer portion of the resulting fixed-point value that do not correspond to bits in the framebuffer are masked out.</span></span>

<span data-ttu-id="3d094-120">您可以隨時更新目前的索引。</span><span class="sxs-lookup"><span data-stu-id="3d094-120">The current index can be updated at any time.</span></span> <span data-ttu-id="3d094-121">尤其是，在呼叫 [**glBegin**](/windows/desktop/OpenGL/glbegin)和對應的 [**glEnd**](glend.md)呼叫之間，可以呼叫 **glIndexi** 。</span><span class="sxs-lookup"><span data-stu-id="3d094-121">In particular, **glIndexi** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](glend.md).</span></span>

<span data-ttu-id="3d094-122">下列函式會抓取 **glIndexi** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="3d094-122">The following function retrieves information related to **glIndexi**:</span></span>

<span data-ttu-id="3d094-123">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 索引的 glGet</span><span class="sxs-lookup"><span data-stu-id="3d094-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_INDEX</span></span>

## <a name="requirements"></a><span data-ttu-id="3d094-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d094-124">Requirements</span></span>



| <span data-ttu-id="3d094-125">需求</span><span class="sxs-lookup"><span data-stu-id="3d094-125">Requirement</span></span> | <span data-ttu-id="3d094-126">值</span><span class="sxs-lookup"><span data-stu-id="3d094-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d094-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d094-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3d094-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d094-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3d094-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d094-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3d094-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d094-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3d094-131">標頭</span><span class="sxs-lookup"><span data-stu-id="3d094-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d094-132"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="3d094-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3d094-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="3d094-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="3d094-134"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d094-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3d094-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3d094-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d094-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d094-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d094-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d094-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d094-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3d094-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3d094-139">**glColor**</span><span class="sxs-lookup"><span data-stu-id="3d094-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="3d094-140">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3d094-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3d094-141">**glGet**</span><span class="sxs-lookup"><span data-stu-id="3d094-141">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

