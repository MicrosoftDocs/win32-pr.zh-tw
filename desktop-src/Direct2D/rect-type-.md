---
title: 'Rect 類型函數 (D2d1helper .h) '
description: 使用指定的資料類型，建立儲存其座標的矩形結構。
ms.assetid: b152efaf-0779-4024-b998-82a347abba71
keywords:
- Rect 型別函式 Direct2D
topic_type:
- apiref
api_name:
- Rect Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ed16ecd5a79c73ecb7341b9aa7f3378854dd4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968186"
---
# <a name="recttype-function"></a><span data-ttu-id="b2ca5-104">Rect <Type> 函數</span><span class="sxs-lookup"><span data-stu-id="b2ca5-104">Rect<Type> Function</span></span>

<span data-ttu-id="b2ca5-105">使用指定的資料類型，建立儲存其座標的矩形結構。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-105">Creates a rectangle structure that stores its coordinates using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Rect Rect(
  Type left,
  Type top,
  Type right,
  Type bottom
);
```

## <a name="template-parameters"></a><span data-ttu-id="b2ca5-106">範本參數</span><span class="sxs-lookup"><span data-stu-id="b2ca5-106">Template Parameters</span></span>



| <span data-ttu-id="b2ca5-107">參數</span><span class="sxs-lookup"><span data-stu-id="b2ca5-107">Parameter</span></span> | <span data-ttu-id="b2ca5-108">描述</span><span class="sxs-lookup"><span data-stu-id="b2ca5-108">Description</span></span>                                                                                                |
|-----------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2ca5-109">類型</span><span class="sxs-lookup"><span data-stu-id="b2ca5-109">Type</span></span>      | <span data-ttu-id="b2ca5-110">用來儲存矩形維度的資料類型。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-110">The data type used to store the dimensions of the rectangle.</span></span> <span data-ttu-id="b2ca5-111">可能的值為 **FLOAT** 和 **UINT32**。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-111">Possible values are **FLOAT** and **UINT32**.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="b2ca5-112">參數</span><span class="sxs-lookup"><span data-stu-id="b2ca5-112">Parameters</span></span>



| <span data-ttu-id="b2ca5-113">參數</span><span class="sxs-lookup"><span data-stu-id="b2ca5-113">Parameter</span></span> | <span data-ttu-id="b2ca5-114">描述</span><span class="sxs-lookup"><span data-stu-id="b2ca5-114">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="b2ca5-115">left</span><span class="sxs-lookup"><span data-stu-id="b2ca5-115">left</span></span>      | <span data-ttu-id="b2ca5-116">矩形左上角的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-116">The x-coordinate of the rectangle's upper-left corner.</span></span>  |
| <span data-ttu-id="b2ca5-117">top</span><span class="sxs-lookup"><span data-stu-id="b2ca5-117">top</span></span>       | <span data-ttu-id="b2ca5-118">矩形左上角的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-118">The y-coordinate of the rectangle's upper-left corner.</span></span>  |
| <span data-ttu-id="b2ca5-119">向右</span><span class="sxs-lookup"><span data-stu-id="b2ca5-119">right</span></span>     | <span data-ttu-id="b2ca5-120">矩形右下角的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-120">The x-coordinate of the rectangle's lower-right corner.</span></span> |
| <span data-ttu-id="b2ca5-121">下</span><span class="sxs-lookup"><span data-stu-id="b2ca5-121">bottom</span></span>    | <span data-ttu-id="b2ca5-122">矩形右下角的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-122">The y-coordinate of the rectangle's lower-right corner.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="b2ca5-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2ca5-123">Return Value</span></span>

<span data-ttu-id="b2ca5-124">包含指定座標的矩形結構。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-124">A rectangle structure that contains the specified coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2ca5-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2ca5-125">Requirements</span></span>



| <span data-ttu-id="b2ca5-126">需求</span><span class="sxs-lookup"><span data-stu-id="b2ca5-126">Requirement</span></span> | <span data-ttu-id="b2ca5-127">值</span><span class="sxs-lookup"><span data-stu-id="b2ca5-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2ca5-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2ca5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b2ca5-129">Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="b2ca5-129">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="b2ca5-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2ca5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b2ca5-131">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2ca5-131">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="b2ca5-132">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="b2ca5-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="b2ca5-133">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2ca5-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="b2ca5-134">標頭</span><span class="sxs-lookup"><span data-stu-id="b2ca5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2ca5-135"><dt>D2d1helper。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2ca5-135"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="b2ca5-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="b2ca5-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="b2ca5-137"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2ca5-137"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="b2ca5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b2ca5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2ca5-139"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2ca5-139"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





