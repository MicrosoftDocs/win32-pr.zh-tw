---
description: 當使用者在任何 IInkTablet 物件上繪製新的 IInkStrokeDisp 物件時發生。
ms.assetid: fac5104d-d0da-40b1-a4a6-00a34718d09f
title: 'InkEdit： Stroke 事件 (筆跡) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d21abde9deb565f207a44ddd44b51681f1bfa6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695000"
---
# <a name="inkeditstroke-event"></a><span data-ttu-id="460c1-103">InkEdit。筆觸事件</span><span class="sxs-lookup"><span data-stu-id="460c1-103">InkEdit.Stroke event</span></span>

<span data-ttu-id="460c1-104">當使用者在任何 [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)物件上繪製新的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件時發生。</span><span class="sxs-lookup"><span data-stu-id="460c1-104">Occurs when the user draws a new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object on any [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="460c1-105">語法</span><span class="sxs-lookup"><span data-stu-id="460c1-105">Syntax</span></span>


```C++
HRESULT Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="460c1-106">參數</span><span class="sxs-lookup"><span data-stu-id="460c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="460c1-107">資料 *指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="460c1-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="460c1-108">[**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。</span><span class="sxs-lookup"><span data-stu-id="460c1-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="460c1-109">*筆觸* \[在\]</span><span class="sxs-lookup"><span data-stu-id="460c1-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="460c1-110">收集的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件。</span><span class="sxs-lookup"><span data-stu-id="460c1-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="460c1-111">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="460c1-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="460c1-112">**變異 \_TRUE** 表示取消 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件的集合; **變異 \_FALSE** 表示收集 **IInkStrokeDisp** 物件，並繼續進行 **筆劃** 。</span><span class="sxs-lookup"><span data-stu-id="460c1-112">**VARIANT\_TRUE** to cancel the collection of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object; **VARIANT\_FALSE** to collect the **IInkStrokeDisp** object and continue with the **Stroke** even.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="460c1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="460c1-113">Return value</span></span>

<span data-ttu-id="460c1-114">如果此事件成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="460c1-114">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="460c1-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="460c1-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="460c1-116">備註</span><span class="sxs-lookup"><span data-stu-id="460c1-116">Remarks</span></span>

<span data-ttu-id="460c1-117">此事件方法是在 **\_ IInkEditEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="460c1-117">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="460c1-118">**\_ IInkEditEvents** 介面會以 DISPID IeeStroke 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="460c1-118">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeStroke.</span></span>

## <a name="requirements"></a><span data-ttu-id="460c1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="460c1-119">Requirements</span></span>



| <span data-ttu-id="460c1-120">需求</span><span class="sxs-lookup"><span data-stu-id="460c1-120">Requirement</span></span> | <span data-ttu-id="460c1-121">值</span><span class="sxs-lookup"><span data-stu-id="460c1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="460c1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="460c1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="460c1-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="460c1-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="460c1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="460c1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="460c1-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="460c1-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="460c1-126">標頭</span><span class="sxs-lookup"><span data-stu-id="460c1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="460c1-127"><dt>筆跡 (也需要筆跡 \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="460c1-127"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="460c1-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="460c1-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="460c1-129"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="460c1-129"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="460c1-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="460c1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="460c1-131">InkEdit</span><span class="sxs-lookup"><span data-stu-id="460c1-131">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="460c1-132">**IInkCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="460c1-132">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="460c1-133">**IInkStrokeDisp 介面**</span><span class="sxs-lookup"><span data-stu-id="460c1-133">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

