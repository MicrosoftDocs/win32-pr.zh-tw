---
title: IDWriteTextLayout3 GetLineSpacing 方法
description: 取得行距資訊。
ms.assetid: 6b93a3ec-c8ea-2e64-45b5-51565d6de173
keywords:
- GetLineSpacing 方法直接寫入
- GetLineSpacing 方法 Direct Write，IDWriteTextLayout3 介面
- IDWriteTextLayout3 介面 Direct Write，GetLineSpacing 方法
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303030a5674f39c160804ae2dad5b91050d82f37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934610"
---
# <a name="idwritetextlayout3getlinespacing-method"></a><span data-ttu-id="5dad6-106">IDWriteTextLayout3：： GetLineSpacing 方法</span><span class="sxs-lookup"><span data-stu-id="5dad6-106">IDWriteTextLayout3::GetLineSpacing method</span></span>

<span data-ttu-id="5dad6-107">取得行距資訊。</span><span class="sxs-lookup"><span data-stu-id="5dad6-107">Gets line spacing information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dad6-108">語法</span><span class="sxs-lookup"><span data-stu-id="5dad6-108">Syntax</span></span>


```C++
HRESULT GetLineSpacing(
  [out] DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="5dad6-109">參數</span><span class="sxs-lookup"><span data-stu-id="5dad6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dad6-110">*lineSpacingOptions* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5dad6-110">*lineSpacingOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5dad6-111">如何管理各行之間的空間。</span><span class="sxs-lookup"><span data-stu-id="5dad6-111">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dad6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5dad6-112">Return value</span></span>

<span data-ttu-id="5dad6-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5dad6-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5dad6-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5dad6-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dad6-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5dad6-115">Requirements</span></span>



| <span data-ttu-id="5dad6-116">需求</span><span class="sxs-lookup"><span data-stu-id="5dad6-116">Requirement</span></span> | <span data-ttu-id="5dad6-117">值</span><span class="sxs-lookup"><span data-stu-id="5dad6-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dad6-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5dad6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5dad6-119">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5dad6-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5dad6-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5dad6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5dad6-121">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5dad6-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5dad6-122">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="5dad6-122">Minimum supported phone</span></span><br/>  | <span data-ttu-id="5dad6-123">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5dad6-123">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="5dad6-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="5dad6-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="5dad6-125"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5dad6-125"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5dad6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5dad6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dad6-127"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dad6-127"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5dad6-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5dad6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dad6-129">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="5dad6-129">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





