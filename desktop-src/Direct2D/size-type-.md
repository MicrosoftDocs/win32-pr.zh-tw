---
title: '大小類型函式 (D2d1helper .h) '
description: 使用指定的資料類型，建立儲存其寬度和高度的大小結構。
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- 大小類型函式 Direct2D
topic_type:
- apiref
api_name:
- Size Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a300ab0ce7da57440516733459f703379cf5a943
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465001"
---
# <a name="sizetype-function"></a><span data-ttu-id="60af6-104">Size <Type> 函數</span><span class="sxs-lookup"><span data-stu-id="60af6-104">Size<Type> Function</span></span>

<span data-ttu-id="60af6-105">使用指定的資料類型，建立儲存其寬度和高度的大小結構。</span><span class="sxs-lookup"><span data-stu-id="60af6-105">Creates a size structure that stores its width and height using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a><span data-ttu-id="60af6-106">範本參數</span><span class="sxs-lookup"><span data-stu-id="60af6-106">Template Parameters</span></span>



| <span data-ttu-id="60af6-107">參數</span><span class="sxs-lookup"><span data-stu-id="60af6-107">Parameter</span></span> | <span data-ttu-id="60af6-108">描述</span><span class="sxs-lookup"><span data-stu-id="60af6-108">Description</span></span>                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60af6-109">類型</span><span class="sxs-lookup"><span data-stu-id="60af6-109">Type</span></span>      | <span data-ttu-id="60af6-110">資料類型，用來儲存大小的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="60af6-110">The data type used to store the width and height of the size.</span></span> <span data-ttu-id="60af6-111">可能的值為 FLOAT 和 UINT32。</span><span class="sxs-lookup"><span data-stu-id="60af6-111">Possible values are FLOAT and UINT32.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="60af6-112">參數</span><span class="sxs-lookup"><span data-stu-id="60af6-112">Parameters</span></span>



| <span data-ttu-id="60af6-113">參數</span><span class="sxs-lookup"><span data-stu-id="60af6-113">Parameter</span></span> | <span data-ttu-id="60af6-114">Description</span><span class="sxs-lookup"><span data-stu-id="60af6-114">Description</span></span>        |
|-----------|--------------------|
| <span data-ttu-id="60af6-115">width</span><span class="sxs-lookup"><span data-stu-id="60af6-115">width</span></span>     | <span data-ttu-id="60af6-116">大小的寬度。</span><span class="sxs-lookup"><span data-stu-id="60af6-116">The size's width.</span></span>  |
| <span data-ttu-id="60af6-117">身高</span><span class="sxs-lookup"><span data-stu-id="60af6-117">height</span></span>    | <span data-ttu-id="60af6-118">大小的高度。</span><span class="sxs-lookup"><span data-stu-id="60af6-118">The size's height.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="60af6-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="60af6-119">Return Value</span></span>

<span data-ttu-id="60af6-120">包含指定之寬度和高度的大小。</span><span class="sxs-lookup"><span data-stu-id="60af6-120">A size that contains the specified width and height.</span></span>

## <a name="requirements"></a><span data-ttu-id="60af6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="60af6-121">Requirements</span></span>



| <span data-ttu-id="60af6-122">需求</span><span class="sxs-lookup"><span data-stu-id="60af6-122">Requirement</span></span> | <span data-ttu-id="60af6-123">值</span><span class="sxs-lookup"><span data-stu-id="60af6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60af6-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60af6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="60af6-125">Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="60af6-125">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="60af6-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60af6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="60af6-127">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60af6-127">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="60af6-128">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="60af6-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="60af6-129">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60af6-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="60af6-130">標頭</span><span class="sxs-lookup"><span data-stu-id="60af6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="60af6-131"><dt>D2d1helper。h</dt></span><span class="sxs-lookup"><span data-stu-id="60af6-131"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="60af6-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="60af6-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="60af6-133"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="60af6-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="60af6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="60af6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60af6-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60af6-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





