---
title: 'D2D1_SIZE_U (D2DBaseTypes) '
description: 儲存已排序的整數配對，通常是矩形的寬度和高度。
ms.assetid: e28da5ee-7d68-4ec5-b477-c6ead0c725e6
keywords:
- D2D1_SIZE_U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b5c317a98169957402dd125c054b8f6e0bc69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094155"
---
# <a name="d2d1_size_u"></a><span data-ttu-id="a3a1a-104">D2D1 \_ 大小 \_ U</span><span class="sxs-lookup"><span data-stu-id="a3a1a-104">D2D1\_SIZE\_U</span></span>

<span data-ttu-id="a3a1a-105">儲存已排序的整數配對，通常是矩形的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="a3a1a-105">Stores an ordered pair of integers, typically the width and height of a rectangle.</span></span>


```C++
typedef D2D_SIZE_U D2D1_SIZE_U;
```



## <a name="remarks"></a><span data-ttu-id="a3a1a-106">備註</span><span class="sxs-lookup"><span data-stu-id="a3a1a-106">Remarks</span></span>

<span data-ttu-id="a3a1a-107">就像點一樣，大小是另一個重要的圖形概念。</span><span class="sxs-lookup"><span data-stu-id="a3a1a-107">Like points, sizes are another important graphics concept.</span></span> <span data-ttu-id="a3a1a-108">在 Direct2D 中，大小會以 **D2D1 \_ 大小 \_ U** 或 [**D2D1 大小的 \_ \_ F**](d2d1-size-f.md) 結構表示。</span><span class="sxs-lookup"><span data-stu-id="a3a1a-108">In Direct2D, sizes are represented by the **D2D1\_SIZE\_U** or [**D2D1\_SIZE\_F**](d2d1-size-f.md) structures.</span></span> <span data-ttu-id="a3a1a-109">它們都包含一組已排序的數位。</span><span class="sxs-lookup"><span data-stu-id="a3a1a-109">They both contain an ordered pair of numbers.</span></span> <span data-ttu-id="a3a1a-110">**D2D1 \_ 大小 \_ U** 結構包含 **UINT32** 值的排序配對，而 **D2D1 \_ 大小 \_ F** 結構包含一組已排序的 **FLOAT** 值配對。</span><span class="sxs-lookup"><span data-stu-id="a3a1a-110">The **D2D1\_SIZE\_U** structure contains an ordered pair of **UINT32** values, and the **D2D1\_SIZE\_F** structure contains an ordered pair of **FLOAT** values.</span></span>

<span data-ttu-id="a3a1a-111">**D2D1 \_ 大小 \_ U** 結構提供一個便利的方式，讓您儲存一組已排序的數位，例如矩形的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="a3a1a-111">The **D2D1\_SIZE\_U** structure provides a convenient way for you to store an ordered pair of numbers, such as the width and height of a rectangle.</span></span>

<span data-ttu-id="a3a1a-112">**D2D1 \_大小 \_ u** 是已定義的類型 **D2D \_ 大小 \_ u** 的新名稱。</span><span class="sxs-lookup"><span data-stu-id="a3a1a-112">**D2D1\_SIZE\_U** is a new name for an already defined type **D2D\_SIZE\_U**.</span></span> <span data-ttu-id="a3a1a-113">您可以使用 **D2D1：： SizeU** 函數來建立 **D2D1 \_ 大小 \_ U** 結構。</span><span class="sxs-lookup"><span data-stu-id="a3a1a-113">You can use the **D2D1::SizeU** function to create a **D2D1\_SIZE\_U** structure.</span></span> <span data-ttu-id="a3a1a-114">此結構的常見用法是指定 [**D2D1 \_ HWND 轉譯 \_ \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) 結構的圖元大小。</span><span class="sxs-lookup"><span data-stu-id="a3a1a-114">A common use for this structure is to specify the pixel size of a [**D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) structure.</span></span> <span data-ttu-id="a3a1a-115">以下提供使用此結構的範例。</span><span class="sxs-lookup"><span data-stu-id="a3a1a-115">The following provides an example of using this structure.</span></span>


```C++
    if (!m_pRenderTarget)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top
            );

        // Create a Direct2D render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



## <a name="requirements"></a><span data-ttu-id="a3a1a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3a1a-116">Requirements</span></span>



| <span data-ttu-id="a3a1a-117">需求</span><span class="sxs-lookup"><span data-stu-id="a3a1a-117">Requirement</span></span> | <span data-ttu-id="a3a1a-118">值</span><span class="sxs-lookup"><span data-stu-id="a3a1a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3a1a-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3a1a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a3a1a-120">Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="a3a1a-120">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="a3a1a-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3a1a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a3a1a-122">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3a1a-122">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a3a1a-123">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="a3a1a-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="a3a1a-124">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3a1a-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="a3a1a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a3a1a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3a1a-126"><dt>D2DBaseTypes (包含 D2d1) </dt></span><span class="sxs-lookup"><span data-stu-id="a3a1a-126"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a3a1a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3a1a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3a1a-128">**D2D \_ 大小 \_ U**</span><span class="sxs-lookup"><span data-stu-id="a3a1a-128">**D2D\_SIZE\_U**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u)
</dt> <dt>

[<span data-ttu-id="a3a1a-129">**D2D1 \_ 大小 \_ F**</span><span class="sxs-lookup"><span data-stu-id="a3a1a-129">**D2D1\_SIZE\_F**</span></span>](d2d1-size-f.md)
</dt> <dt>

[<span data-ttu-id="a3a1a-130">**D2D1::HwndRenderTargetProperties**</span><span class="sxs-lookup"><span data-stu-id="a3a1a-130">**D2D1::HwndRenderTargetProperties**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties)
</dt> </dl>

 

