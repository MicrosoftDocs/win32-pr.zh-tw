---
title: IDWriteTextLayout3 GetLineMetrics 方法
description: 抓取每一行的屬性。
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
keywords:
- GetLineMetrics 方法直接寫入
- GetLineMetrics 方法 Direct Write，IDWriteTextLayout3 介面
- IDWriteTextLayout3 介面 Direct Write，GetLineMetrics 方法
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d10a06cbf123b71e1308b45c747ac8a840a5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465841"
---
# <a name="idwritetextlayout3getlinemetrics-method"></a><span data-ttu-id="ebf82-106">IDWriteTextLayout3：： GetLineMetrics 方法</span><span class="sxs-lookup"><span data-stu-id="ebf82-106">IDWriteTextLayout3::GetLineMetrics method</span></span>

<span data-ttu-id="ebf82-107">抓取每一行的屬性。</span><span class="sxs-lookup"><span data-stu-id="ebf82-107">Retrieves properties of each line.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf82-108">語法</span><span class="sxs-lookup"><span data-stu-id="ebf82-108">Syntax</span></span>


```C++
HRESULT GetLineMetrics(
  [out] DWRITE_LINE_METRICS1 *lineMetrics,
        UINT32               maxLineCount,
  [out] UINT32               *actualLineCount
);
```



## <a name="parameters"></a><span data-ttu-id="ebf82-109">參數</span><span class="sxs-lookup"><span data-stu-id="ebf82-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebf82-110">*lineMetrics* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ebf82-110">*lineMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebf82-111">要填入行資訊的陣列。</span><span class="sxs-lookup"><span data-stu-id="ebf82-111">The array to fill with line information.</span></span>

</dd> <dt>

<span data-ttu-id="ebf82-112">*maxLineCount*</span><span class="sxs-lookup"><span data-stu-id="ebf82-112">*maxLineCount*</span></span> 
</dt> <dd>

<span data-ttu-id="ebf82-113">LineMetrics 陣列的大小上限。</span><span class="sxs-lookup"><span data-stu-id="ebf82-113">The maximum size of the lineMetrics array.</span></span>

</dd> <dt>

<span data-ttu-id="ebf82-114">*actualLineCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ebf82-114">*actualLineCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebf82-115">所需 lineMetrics 陣列的實際大小。</span><span class="sxs-lookup"><span data-stu-id="ebf82-115">The actual size of the lineMetrics array that is needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebf82-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="ebf82-116">Return value</span></span>

<span data-ttu-id="ebf82-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ebf82-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ebf82-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ebf82-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebf82-119">備註</span><span class="sxs-lookup"><span data-stu-id="ebf82-119">Remarks</span></span>

<span data-ttu-id="ebf82-120">如果 maxLineCount 不夠大 \_ \_ ，就 \_ 相當於 WIN32 中的 HRESULT （相當於 \_ \_ WIN32 (錯誤的 \_ \_ 緩衝區) ），會傳回，而且 actualLineCount 會設定為所需的行數。</span><span class="sxs-lookup"><span data-stu-id="ebf82-120">If maxLineCount is not large enough E\_NOT\_SUFFICIENT\_BUFFER, which is equivalent to HRESULT\_FROM\_WIN32(ERROR\_INSUFFICIENT\_BUFFER), is returned and actualLineCount is set to the number of lines needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf82-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebf82-121">Requirements</span></span>



| <span data-ttu-id="ebf82-122">需求</span><span class="sxs-lookup"><span data-stu-id="ebf82-122">Requirement</span></span> | <span data-ttu-id="ebf82-123">值</span><span class="sxs-lookup"><span data-stu-id="ebf82-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf82-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ebf82-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ebf82-125">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebf82-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ebf82-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ebf82-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ebf82-127">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebf82-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ebf82-128">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="ebf82-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="ebf82-129">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebf82-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="ebf82-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="ebf82-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ebf82-131"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebf82-131"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ebf82-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ebf82-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebf82-133"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebf82-133"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ebf82-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebf82-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf82-135">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="ebf82-135">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





