---
title: IDWriteColorGlyphRunEnumerator MoveNext 方法
description: 移至列舉值中的下一個圖像執行。
ms.assetid: E6336C0E-F880-485C-9111-A102298257C1
keywords:
- MoveNext 方法直接寫入
- MoveNext 方法 Direct Write，IDWriteColorGlyphRunEnumerator 介面
- IDWriteColorGlyphRunEnumerator 介面直接寫入，MoveNext 方法
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator.MoveNext
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c9963916c07f1df8cf3cfedb49b9e3fd66d0df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508799"
---
# <a name="idwritecolorglyphrunenumeratormovenext-method"></a><span data-ttu-id="43c2e-106">IDWriteColorGlyphRunEnumerator：： MoveNext 方法</span><span class="sxs-lookup"><span data-stu-id="43c2e-106">IDWriteColorGlyphRunEnumerator::MoveNext method</span></span>

<span data-ttu-id="43c2e-107">移至列舉值中的下一個圖像執行。</span><span class="sxs-lookup"><span data-stu-id="43c2e-107">Move to the next glyph run in the enumerator.</span></span>

## <a name="syntax"></a><span data-ttu-id="43c2e-108">語法</span><span class="sxs-lookup"><span data-stu-id="43c2e-108">Syntax</span></span>


```C++
HRESULT MoveNext(
  [out] BOOL *haveRun
);
```



## <a name="parameters"></a><span data-ttu-id="43c2e-109">參數</span><span class="sxs-lookup"><span data-stu-id="43c2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43c2e-110">*haveRun* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="43c2e-110">*haveRun* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43c2e-111">類型： \**BOOL \** _</span><span class="sxs-lookup"><span data-stu-id="43c2e-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="43c2e-112">如果有下一個圖像執行，則傳回 _ \*TRUE\*\*。</span><span class="sxs-lookup"><span data-stu-id="43c2e-112">Returns _ *TRUE*\* if there is a next glyph run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43c2e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="43c2e-113">Return value</span></span>

<span data-ttu-id="43c2e-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="43c2e-114">Type: **HRESULT**</span></span>

<span data-ttu-id="43c2e-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="43c2e-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="43c2e-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="43c2e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="43c2e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="43c2e-117">Requirements</span></span>



| <span data-ttu-id="43c2e-118">需求</span><span class="sxs-lookup"><span data-stu-id="43c2e-118">Requirement</span></span> | <span data-ttu-id="43c2e-119">值</span><span class="sxs-lookup"><span data-stu-id="43c2e-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43c2e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43c2e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="43c2e-121">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43c2e-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="43c2e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43c2e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="43c2e-123">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43c2e-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="43c2e-124">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="43c2e-124">Minimum supported phone</span></span><br/>  | <span data-ttu-id="43c2e-125">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43c2e-125">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="43c2e-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="43c2e-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="43c2e-127"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="43c2e-127"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="43c2e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="43c2e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43c2e-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43c2e-129"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="43c2e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43c2e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43c2e-131">**IDWriteColorGlyphRunEnumerator**</span><span class="sxs-lookup"><span data-stu-id="43c2e-131">**IDWriteColorGlyphRunEnumerator**</span></span>](idwritecolorglyphrunenumerator.md)
</dt> </dl>

 

 





