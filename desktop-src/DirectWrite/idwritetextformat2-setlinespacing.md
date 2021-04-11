---
title: IDWriteTextFormat2 SetLineSpacing 方法
description: 設定行間距。 |IDWriteTextFormat2 SetLineSpacing 方法
ms.assetid: 71d8c6c4-920f-a1b5-5a13-9985a7aca41e
keywords:
- SetLineSpacing 方法直接寫入
- SetLineSpacing 方法 Direct Write，IDWriteTextFormat2 介面
- IDWriteTextFormat2 介面 Direct Write，SetLineSpacing 方法
topic_type:
- apiref
api_name:
- IDWriteTextFormat2.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d3514c52c9b8a51666d36eec7ce893735635f3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196110"
---
# <a name="idwritetextformat2setlinespacing-method"></a><span data-ttu-id="84073-107">IDWriteTextFormat2：： SetLineSpacing 方法</span><span class="sxs-lookup"><span data-stu-id="84073-107">IDWriteTextFormat2::SetLineSpacing method</span></span>

<span data-ttu-id="84073-108">設定行間距。</span><span class="sxs-lookup"><span data-stu-id="84073-108">Set line spacing.</span></span>

## <a name="syntax"></a><span data-ttu-id="84073-109">語法</span><span class="sxs-lookup"><span data-stu-id="84073-109">Syntax</span></span>


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="84073-110">參數</span><span class="sxs-lookup"><span data-stu-id="84073-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84073-111">*lineSpacingOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="84073-111">*lineSpacingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84073-112">Type： **Const [**DWRITE \_ \_**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing) \*** 行距</span><span class="sxs-lookup"><span data-stu-id="84073-112">Type: **const [**DWRITE\_LINE\_SPACING**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing)\***</span></span>

<span data-ttu-id="84073-113">如何管理各行之間的空間。</span><span class="sxs-lookup"><span data-stu-id="84073-113">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84073-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="84073-114">Return value</span></span>

<span data-ttu-id="84073-115">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="84073-115">Type: **HRESULT**</span></span>

<span data-ttu-id="84073-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="84073-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="84073-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="84073-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="84073-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="84073-118">Requirements</span></span>



| <span data-ttu-id="84073-119">需求</span><span class="sxs-lookup"><span data-stu-id="84073-119">Requirement</span></span> | <span data-ttu-id="84073-120">值</span><span class="sxs-lookup"><span data-stu-id="84073-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84073-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84073-121">Minimum supported client</span></span><br/> | <span data-ttu-id="84073-122">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84073-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="84073-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84073-123">Minimum supported server</span></span><br/> | <span data-ttu-id="84073-124">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84073-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="84073-125">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="84073-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="84073-126">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84073-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="84073-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="84073-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="84073-128"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="84073-128"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="84073-129">DLL</span><span class="sxs-lookup"><span data-stu-id="84073-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84073-130"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84073-130"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="84073-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84073-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84073-132">**IDWriteTextFormat2**</span><span class="sxs-lookup"><span data-stu-id="84073-132">**IDWriteTextFormat2**</span></span>](idwritetextformat2.md)
</dt> </dl>

 

 





