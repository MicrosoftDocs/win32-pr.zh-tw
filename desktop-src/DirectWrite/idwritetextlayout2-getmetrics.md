---
title: IDWriteTextLayout2 GetMetrics 方法
description: 抓取格式化字串的整體計量。
ms.assetid: EADCD83A-9FF5-44AB-8AB5-35FCB3A84889
keywords:
- GetMetrics 方法直接寫入
- GetMetrics 方法 Direct Write，IDWriteTextLayout2 介面
- IDWriteTextLayout2 介面 Direct Write，GetMetrics 方法
topic_type:
- apiref
api_name:
- IDWriteTextLayout2.GetMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e393dfabb632641125d915e85f275977b20f0326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965917"
---
# <a name="idwritetextlayout2getmetrics-method"></a><span data-ttu-id="cc3e0-106">IDWriteTextLayout2：： GetMetrics 方法</span><span class="sxs-lookup"><span data-stu-id="cc3e0-106">IDWriteTextLayout2::GetMetrics method</span></span>

<span data-ttu-id="cc3e0-107">抓取格式化字串的整體計量。</span><span class="sxs-lookup"><span data-stu-id="cc3e0-107">Retrieves overall metrics for the formatted string.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc3e0-108">語法</span><span class="sxs-lookup"><span data-stu-id="cc3e0-108">Syntax</span></span>


```C++
virtual HRESULT GetMetrics(
  [out] DWRITE_TEXT_METRICS1 * textMetrics
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="cc3e0-109">參數</span><span class="sxs-lookup"><span data-stu-id="cc3e0-109">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="cc3e0-110">*textMetrics* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cc3e0-110">*textMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3e0-111">類型： \**[**DWRITE \_ 文字 \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) \** _</span><span class="sxs-lookup"><span data-stu-id="cc3e0-111">Type: \**[**DWRITE\_TEXT\_METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1)\** _</span></span>

<span data-ttu-id="cc3e0-112">當此方法傳回時，會在格式化之後包含文字和相關內容的測量距離。</span><span class="sxs-lookup"><span data-stu-id="cc3e0-112">When this method returns, contains the measured distances of text and associated content after being formatted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc3e0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc3e0-113">Return value</span></span>

<span data-ttu-id="cc3e0-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="cc3e0-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="cc3e0-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="cc3e0-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc3e0-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cc3e0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc3e0-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc3e0-117">Requirements</span></span>



| <span data-ttu-id="cc3e0-118">需求</span><span class="sxs-lookup"><span data-stu-id="cc3e0-118">Requirement</span></span> | <span data-ttu-id="cc3e0-119">值</span><span class="sxs-lookup"><span data-stu-id="cc3e0-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc3e0-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc3e0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cc3e0-121">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc3e0-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="cc3e0-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc3e0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cc3e0-123">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc3e0-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="cc3e0-124">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="cc3e0-124">Minimum supported phone</span></span><br/>  | <span data-ttu-id="cc3e0-125">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc3e0-125">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="cc3e0-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="cc3e0-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="cc3e0-127"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc3e0-127"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cc3e0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="cc3e0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc3e0-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc3e0-129"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cc3e0-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc3e0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc3e0-131">**IDWriteTextLayout2**</span><span class="sxs-lookup"><span data-stu-id="cc3e0-131">**IDWriteTextLayout2**</span></span>](idwritetextlayout2.md)
</dt> </dl>

 

 





