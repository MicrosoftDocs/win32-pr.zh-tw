---
title: IDWriteTextLayout3 SetLineSpacing 方法
description: 設定行間距。 |IDWriteTextLayout3 SetLineSpacing 方法
ms.assetid: 1bfca257-189c-4d18-628c-aff8217d2775
keywords:
- SetLineSpacing 方法直接寫入
- SetLineSpacing 方法 Direct Write，IDWriteTextLayout3 介面
- IDWriteTextLayout3 介面 Direct Write，SetLineSpacing 方法
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794df5b0dc993688c8bab15c927ae2c03bc18d69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106974789"
---
# <a name="idwritetextlayout3setlinespacing-method"></a><span data-ttu-id="520c3-107">IDWriteTextLayout3：： SetLineSpacing 方法</span><span class="sxs-lookup"><span data-stu-id="520c3-107">IDWriteTextLayout3::SetLineSpacing method</span></span>

<span data-ttu-id="520c3-108">設定行間距。</span><span class="sxs-lookup"><span data-stu-id="520c3-108">Set line spacing.</span></span>

## <a name="syntax"></a><span data-ttu-id="520c3-109">語法</span><span class="sxs-lookup"><span data-stu-id="520c3-109">Syntax</span></span>


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="520c3-110">參數</span><span class="sxs-lookup"><span data-stu-id="520c3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="520c3-111">*lineSpacingOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="520c3-111">*lineSpacingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520c3-112">如何管理各行之間的空間。</span><span class="sxs-lookup"><span data-stu-id="520c3-112">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="520c3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="520c3-113">Return value</span></span>

<span data-ttu-id="520c3-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="520c3-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="520c3-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="520c3-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="520c3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="520c3-116">Requirements</span></span>



| <span data-ttu-id="520c3-117">需求</span><span class="sxs-lookup"><span data-stu-id="520c3-117">Requirement</span></span> | <span data-ttu-id="520c3-118">值</span><span class="sxs-lookup"><span data-stu-id="520c3-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="520c3-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="520c3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="520c3-120">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="520c3-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="520c3-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="520c3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="520c3-122">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="520c3-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="520c3-123">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="520c3-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="520c3-124">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="520c3-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="520c3-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="520c3-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="520c3-126"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="520c3-126"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="520c3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="520c3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="520c3-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="520c3-128"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="520c3-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="520c3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="520c3-130">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="520c3-130">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





