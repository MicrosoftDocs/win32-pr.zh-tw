---
title: 'ID2D1HwndRenderTarget 調整大小方法 (D2d1 .h) '
description: 將呈現目標的大小變更為指定的圖元大小。
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- 調整方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f15af87c59c943bd7d5dc8ece708d3603bddce6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980110"
---
# <a name="id2d1hwndrendertargetresize-methods"></a><span data-ttu-id="0fd84-104">ID2D1HwndRenderTarget：： Resize 方法</span><span class="sxs-lookup"><span data-stu-id="0fd84-104">ID2D1HwndRenderTarget::Resize methods</span></span>

<span data-ttu-id="0fd84-105">將呈現目標的大小變更為指定的圖元大小。</span><span class="sxs-lookup"><span data-stu-id="0fd84-105">Changes the size of the render target to the specified pixel size.</span></span>

### <a name="overload-list"></a><span data-ttu-id="0fd84-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="0fd84-106">Overload list</span></span>



| <span data-ttu-id="0fd84-107">方法</span><span class="sxs-lookup"><span data-stu-id="0fd84-107">Method</span></span>                                                                         | <span data-ttu-id="0fd84-108">描述</span><span class="sxs-lookup"><span data-stu-id="0fd84-108">Description</span></span>                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="0fd84-109">[**調整 (D2D1 \_ 大小 \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))</span><span class="sxs-lookup"><span data-stu-id="0fd84-109">[**Resize(D2D1\_SIZE\_U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))</span></span>  | <span data-ttu-id="0fd84-110">將呈現目標的大小變更為指定的圖元大小。</span><span class="sxs-lookup"><span data-stu-id="0fd84-110">Changes the size of the render target to the specified pixel size.</span></span> <br/> |
| <span data-ttu-id="0fd84-111">[**調整 (D2D1 \_ 大小 \_ U \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u))</span><span class="sxs-lookup"><span data-stu-id="0fd84-111">[**Resize(D2D1\_SIZE\_U\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u))</span></span> | <span data-ttu-id="0fd84-112">將呈現目標的大小變更為指定的圖元大小。</span><span class="sxs-lookup"><span data-stu-id="0fd84-112">Changes the size of the render target to the specified pixel size.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="0fd84-113">備註</span><span class="sxs-lookup"><span data-stu-id="0fd84-113">Remarks</span></span>

<span data-ttu-id="0fd84-114">呼叫這個方法之後，即使在建立轉譯目標時指定了 [ [**D2D1 \_ 目前的 \_ 選項 \_ 保留 \_ 內容**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) ] 選項，也不會定義轉譯目標的背景緩衝區內容。</span><span class="sxs-lookup"><span data-stu-id="0fd84-114">After this method is called, the contents of the render target's back-buffer are not defined, even if the [**D2D1\_PRESENT\_OPTIONS\_RETAIN\_CONTENTS**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) option was specified when the render target was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fd84-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fd84-115">Requirements</span></span>



| <span data-ttu-id="0fd84-116">需求</span><span class="sxs-lookup"><span data-stu-id="0fd84-116">Requirement</span></span> | <span data-ttu-id="0fd84-117">值</span><span class="sxs-lookup"><span data-stu-id="0fd84-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd84-118">標頭</span><span class="sxs-lookup"><span data-stu-id="0fd84-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0fd84-119"><dt>D2d1。h</dt></span><span class="sxs-lookup"><span data-stu-id="0fd84-119"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="0fd84-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="0fd84-120">Library</span></span><br/> | <dl> <span data-ttu-id="0fd84-121"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fd84-121"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="0fd84-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0fd84-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="0fd84-123"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fd84-123"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fd84-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0fd84-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="0fd84-125">[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0fd84-125">[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span></span>
</dt> </dl>

<span data-ttu-id="0fd84-126">�</span><span class="sxs-lookup"><span data-stu-id="0fd84-126">�</span></span>

<span data-ttu-id="0fd84-127">�</span><span class="sxs-lookup"><span data-stu-id="0fd84-127">�</span></span>
