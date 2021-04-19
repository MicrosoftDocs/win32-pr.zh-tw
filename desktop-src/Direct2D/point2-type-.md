---
title: 'Point2 類型函式 (D2d1helper .h) '
description: 使用指定的資料類型，建立儲存其座標的點。
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Point2 型別函數 Direct2D
topic_type:
- apiref
api_name:
- Point2 Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f614f49077ed198c5e85d17b9ee3c84a5e300670
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106976360"
---
# <a name="point2type-function"></a><span data-ttu-id="6b361-104">Point2 <Type> 函式</span><span class="sxs-lookup"><span data-stu-id="6b361-104">Point2<Type> Function</span></span>

<span data-ttu-id="6b361-105">使用指定的資料類型，建立儲存其座標的點。</span><span class="sxs-lookup"><span data-stu-id="6b361-105">Creates a point that stores its coordinates using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Point Point2(
  Type x,
  Type y
);
```

## <a name="template-parameters"></a><span data-ttu-id="6b361-106">範本參數</span><span class="sxs-lookup"><span data-stu-id="6b361-106">Template Parameters</span></span>



| <span data-ttu-id="6b361-107">參數</span><span class="sxs-lookup"><span data-stu-id="6b361-107">Parameter</span></span> | <span data-ttu-id="6b361-108">描述</span><span class="sxs-lookup"><span data-stu-id="6b361-108">Description</span></span>                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b361-109">類型</span><span class="sxs-lookup"><span data-stu-id="6b361-109">Type</span></span>      | <span data-ttu-id="6b361-110">用來儲存點之 x 座標和 y 座標的資料型別。</span><span class="sxs-lookup"><span data-stu-id="6b361-110">The data type used to store the x-coordinate and y-coordinate of the point.</span></span> <span data-ttu-id="6b361-111">可能的值為 FLOAT 和 UINT32。</span><span class="sxs-lookup"><span data-stu-id="6b361-111">Possible values are FLOAT and UINT32.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="6b361-112">參數</span><span class="sxs-lookup"><span data-stu-id="6b361-112">Parameters</span></span>



| <span data-ttu-id="6b361-113">參數</span><span class="sxs-lookup"><span data-stu-id="6b361-113">Parameter</span></span> | <span data-ttu-id="6b361-114">Description</span><span class="sxs-lookup"><span data-stu-id="6b361-114">Description</span></span>                    |
|-----------|--------------------------------|
| <span data-ttu-id="6b361-115">x</span><span class="sxs-lookup"><span data-stu-id="6b361-115">x</span></span>         | <span data-ttu-id="6b361-116">點的 X 座標。</span><span class="sxs-lookup"><span data-stu-id="6b361-116">The x-coordinate of the point.</span></span> |
| <span data-ttu-id="6b361-117">y</span><span class="sxs-lookup"><span data-stu-id="6b361-117">y</span></span>         | <span data-ttu-id="6b361-118">點的 Y 座標。</span><span class="sxs-lookup"><span data-stu-id="6b361-118">The y-coordinate of the point.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="6b361-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b361-119">Return Value</span></span>

<span data-ttu-id="6b361-120">包含指定之 x 座標和 y 座標的點。</span><span class="sxs-lookup"><span data-stu-id="6b361-120">A point that contains the specified x-coordinate and y-coordinate.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b361-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b361-121">Requirements</span></span>



| <span data-ttu-id="6b361-122">需求</span><span class="sxs-lookup"><span data-stu-id="6b361-122">Requirement</span></span> | <span data-ttu-id="6b361-123">值</span><span class="sxs-lookup"><span data-stu-id="6b361-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b361-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b361-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6b361-125">Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="6b361-125">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="6b361-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b361-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6b361-127">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b361-127">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="6b361-128">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="6b361-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="6b361-129">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b361-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="6b361-130">標頭</span><span class="sxs-lookup"><span data-stu-id="6b361-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b361-131"><dt>D2d1helper。h</dt></span><span class="sxs-lookup"><span data-stu-id="6b361-131"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="6b361-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="6b361-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="6b361-133"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b361-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="6b361-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6b361-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b361-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b361-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





