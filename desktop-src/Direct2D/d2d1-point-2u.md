---
title: 'D2D1_POINT_2U (D2DBaseTypes) '
description: '表示在二維空間中的 x 座標和 y 座標組。 |D2D1_POINT_2U (D2DBaseTypes) '
ms.assetid: 652c0dd7-c24d-4941-ae23-2be21b53af69
keywords:
- D2D1_POINT_2U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050cf6372a1b84ed72647c8c5a5d76e352f4960f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195984"
---
# <a name="d2d1_point_2u"></a><span data-ttu-id="a249c-105">D2D1 \_ 點 \_ 2u</span><span class="sxs-lookup"><span data-stu-id="a249c-105">D2D1\_POINT\_2U</span></span>

<span data-ttu-id="a249c-106">表示在二維空間中的 x 座標和 y 座標組。</span><span class="sxs-lookup"><span data-stu-id="a249c-106">Represents an x-coordinate and y-coordinate pair in two-dimensional space.</span></span>


```C++
typedef D2D_POINT_2U D2D1_POINT_2U;
```



## <a name="remarks"></a><span data-ttu-id="a249c-107">備註</span><span class="sxs-lookup"><span data-stu-id="a249c-107">Remarks</span></span>

<span data-ttu-id="a249c-108">Direct2D 中的點會以 [**D2D1 \_ 點 \_ 2f**](d2d1-point-2f.md) 或 **D2D1 \_ 點 \_ 2u** 結構表示。</span><span class="sxs-lookup"><span data-stu-id="a249c-108">Points in Direct2D are represented by the [**D2D1\_POINT\_2F**](d2d1-point-2f.md) or **D2D1\_POINT\_2U** structures.</span></span> <span data-ttu-id="a249c-109">兩者都在二維空間中包含 x 座標和 y 座標組。</span><span class="sxs-lookup"><span data-stu-id="a249c-109">Both contain an x-coordinate and y-coordinate pair in two-dimensional space.</span></span> <span data-ttu-id="a249c-110">**D2D1 \_ 點 \_ 2f** 結構會將座標儲存為 **FLOAT** 值，而 **D2D1 \_ 點 \_ 2u** 結構會將這些座標儲存為 **UINT32** 值。</span><span class="sxs-lookup"><span data-stu-id="a249c-110">The **D2D1\_POINT\_2F** structure stores the coordinates as **FLOAT** values, and the **D2D1\_POINT\_2U** structure stores them as **UINT32** values.</span></span>

<span data-ttu-id="a249c-111">**D2D1 \_點 \_ 2u** 是已定義之型別 [**D2D \_ 點 \_ 2u**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u)的新名稱。</span><span class="sxs-lookup"><span data-stu-id="a249c-111">**D2D1\_POINT\_2U** is a new name for the already defined type [**D2D\_POINT\_2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u).</span></span>

## <a name="requirements"></a><span data-ttu-id="a249c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a249c-112">Requirements</span></span>



| <span data-ttu-id="a249c-113">需求</span><span class="sxs-lookup"><span data-stu-id="a249c-113">Requirement</span></span> | <span data-ttu-id="a249c-114">值</span><span class="sxs-lookup"><span data-stu-id="a249c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a249c-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a249c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a249c-116">Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="a249c-116">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="a249c-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a249c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a249c-118">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a249c-118">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a249c-119">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="a249c-119">Minimum supported phone</span></span><br/>  | <span data-ttu-id="a249c-120">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a249c-120">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="a249c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="a249c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a249c-122"><dt>D2DBaseTypes (包含 D2d1) </dt></span><span class="sxs-lookup"><span data-stu-id="a249c-122"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a249c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a249c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a249c-124">**D2D \_ 點 \_ 2u**</span><span class="sxs-lookup"><span data-stu-id="a249c-124">**D2D\_POINT\_2U**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u)
</dt> <dt>

[<span data-ttu-id="a249c-125">**D2D \_ 點 \_ 2f**</span><span class="sxs-lookup"><span data-stu-id="a249c-125">**D2D\_POINT\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

 





