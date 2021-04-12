---
title: IDWriteTextLayout3 InvalidateLayout 方法
description: 使版面配置失效，並在呼叫度量或繪圖函式之前強制重新測量配置。 如果字型的位置變更、配置應重新繪製，或如果用戶端的大小已實 IDWriteInlineObject 變更，這項功能就很有用。
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- InvalidateLayout 方法直接寫入
- InvalidateLayout 方法 Direct Write，IDWriteTextLayout3 介面
- IDWriteTextLayout3 介面 Direct Write，InvalidateLayout 方法
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.InvalidateLayout
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5df97d4590f62f586a570d52428b6560a7d88df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104405"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a><span data-ttu-id="b8842-107">IDWriteTextLayout3：： InvalidateLayout 方法</span><span class="sxs-lookup"><span data-stu-id="b8842-107">IDWriteTextLayout3::InvalidateLayout method</span></span>

<span data-ttu-id="b8842-108">使版面配置失效，並在呼叫度量或繪圖函式之前強制重新測量配置。</span><span class="sxs-lookup"><span data-stu-id="b8842-108">Invalidates the layout, forcing layout to remeasure before calling the metrics or drawing functions.</span></span> <span data-ttu-id="b8842-109">如果字型的位置變更、配置應重新繪製，或如果用戶端的大小已實 IDWriteInlineObject 變更，這項功能就很有用。</span><span class="sxs-lookup"><span data-stu-id="b8842-109">This is useful if the locality of a font changes, and layout should be redrawn, or if the size of a client implemented IDWriteInlineObject changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8842-110">語法</span><span class="sxs-lookup"><span data-stu-id="b8842-110">Syntax</span></span>


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a><span data-ttu-id="b8842-111">參數</span><span class="sxs-lookup"><span data-stu-id="b8842-111">Parameters</span></span>

<span data-ttu-id="b8842-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b8842-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8842-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8842-113">Return value</span></span>

<span data-ttu-id="b8842-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b8842-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b8842-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b8842-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8842-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8842-116">Requirements</span></span>



| <span data-ttu-id="b8842-117">需求</span><span class="sxs-lookup"><span data-stu-id="b8842-117">Requirement</span></span> | <span data-ttu-id="b8842-118">值</span><span class="sxs-lookup"><span data-stu-id="b8842-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8842-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8842-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b8842-120">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8842-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b8842-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8842-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b8842-122">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8842-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b8842-123">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="b8842-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="b8842-124">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8842-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="b8842-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="b8842-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8842-126"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8842-126"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b8842-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b8842-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8842-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8842-128"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b8842-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8842-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8842-130">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="b8842-130">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





