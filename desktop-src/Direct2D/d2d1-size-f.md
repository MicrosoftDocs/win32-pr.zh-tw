---
title: 'D2D1_SIZE_F (D2DBaseTypes) '
description: 儲存一組排序的浮點數，通常是矩形的寬度和高度。
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a031e1e6a1e9ad7d6975f3dea63427655aa92f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464741"
---
# <a name="d2d1_size_f"></a><span data-ttu-id="ea9ed-104">D2D1 \_ 大小 \_ F</span><span class="sxs-lookup"><span data-stu-id="ea9ed-104">D2D1\_SIZE\_F</span></span>

<span data-ttu-id="ea9ed-105">儲存一組排序的浮點數，通常是矩形的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="ea9ed-105">Stores an ordered pair of floats, typically the width and height of a rectangle.</span></span>


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a><span data-ttu-id="ea9ed-106">備註</span><span class="sxs-lookup"><span data-stu-id="ea9ed-106">Remarks</span></span>

<span data-ttu-id="ea9ed-107">就像點一樣，大小是另一個重要的圖形概念。</span><span class="sxs-lookup"><span data-stu-id="ea9ed-107">Like points, sizes are another important graphics concept.</span></span> <span data-ttu-id="ea9ed-108">在 Direct2D 中，大小是以 **D2D1 \_ 大小 \_ F** 或 [**D2D1 \_ 大小 \_ U**](d2d1-size-u.md) 結構表示。</span><span class="sxs-lookup"><span data-stu-id="ea9ed-108">In Direct2D, sizes are represented by the **D2D1\_SIZE\_F** or [**D2D1\_SIZE\_U**](d2d1-size-u.md) structures.</span></span> <span data-ttu-id="ea9ed-109">兩者都包含一組已排序的數位，通常是矩形的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="ea9ed-109">Both contain an ordered pair of numbers, typically the width and height of a rectangle.</span></span> <span data-ttu-id="ea9ed-110">**D2D1 \_ size \_ F** 結構包含一組排序的 **FLOAT** 值，而 **D2D1 \_ 大小 \_ U** 結構包含一對 **UINT32** 值的排序。</span><span class="sxs-lookup"><span data-stu-id="ea9ed-110">The **D2D1\_SIZE\_F** structure contains an ordered pair of **FLOAT** values, and the **D2D1\_SIZE\_U** structure contains an ordered pair of **UINT32** values.</span></span>

<span data-ttu-id="ea9ed-111">**D2D1 \_\_F 大小** 是已定義的類型 **D2D \_ \_ f 大小** 的新名稱。</span><span class="sxs-lookup"><span data-stu-id="ea9ed-111">**D2D1\_SIZE\_F** is a new name for an already defined type **D2D\_SIZE\_F**.</span></span> <span data-ttu-id="ea9ed-112">如需 **D2D1 \_ 大小 \_ f** 所提供的欄位清單，請參閱 **D2D \_ 大小 \_ f**。</span><span class="sxs-lookup"><span data-stu-id="ea9ed-112">For a list of the fields provided by **D2D1\_SIZE\_F**, see **D2D\_SIZE\_F**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea9ed-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea9ed-113">Requirements</span></span>



| <span data-ttu-id="ea9ed-114">需求</span><span class="sxs-lookup"><span data-stu-id="ea9ed-114">Requirement</span></span> | <span data-ttu-id="ea9ed-115">值</span><span class="sxs-lookup"><span data-stu-id="ea9ed-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9ed-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea9ed-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ea9ed-117">Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="ea9ed-117">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="ea9ed-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea9ed-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ea9ed-119">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea9ed-119">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="ea9ed-120">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="ea9ed-120">Minimum supported phone</span></span><br/>  | <span data-ttu-id="ea9ed-121">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea9ed-121">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="ea9ed-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ea9ed-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea9ed-123"><dt>D2DBaseTypes (包含 D2d1) </dt></span><span class="sxs-lookup"><span data-stu-id="ea9ed-123"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ea9ed-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea9ed-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea9ed-125">**D2D \_ 大小 \_ F**</span><span class="sxs-lookup"><span data-stu-id="ea9ed-125">**D2D\_SIZE\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[<span data-ttu-id="ea9ed-126">**D2D1 \_ 大小 \_ U**</span><span class="sxs-lookup"><span data-stu-id="ea9ed-126">**D2D1\_SIZE\_U**</span></span>](d2d1-size-u.md)
</dt> <dt>

[<span data-ttu-id="ea9ed-127">**D2D1 \_ 點 \_ 2f**</span><span class="sxs-lookup"><span data-stu-id="ea9ed-127">**D2D1\_POINT\_2F**</span></span>](d2d1-point-2f.md)
</dt> </dl>

 

