---
description: 發生于按兩下 InkEdit 控制項時。
ms.assetid: 380499e4-8697-4823-8153-29f24b2f234c
title: InkEdit (筆跡) 的 DblClick 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fee0ec42171c9abbe0c99691f881b99db512869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975482"
---
# <a name="inkeditdblclick-event"></a><span data-ttu-id="f61ca-103">InkEdit： DblClick 事件</span><span class="sxs-lookup"><span data-stu-id="f61ca-103">InkEdit.DblClick event</span></span>

<span data-ttu-id="f61ca-104">發生于按兩下 [InkEdit](inkedit-control-reference.md) 控制項時。</span><span class="sxs-lookup"><span data-stu-id="f61ca-104">Occurs when the [InkEdit](inkedit-control-reference.md) control is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="f61ca-105">語法</span><span class="sxs-lookup"><span data-stu-id="f61ca-105">Syntax</span></span>


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="f61ca-106">參數</span><span class="sxs-lookup"><span data-stu-id="f61ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f61ca-107">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f61ca-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f61ca-108">**變異 \_TRUE** 表示取消父控制項的事件;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f61ca-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f61ca-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f61ca-109">Return value</span></span>

<span data-ttu-id="f61ca-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f61ca-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f61ca-111">備註</span><span class="sxs-lookup"><span data-stu-id="f61ca-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f61ca-112">若要區分左、右和中間的按鍵，請使用 [**MouseDown**](inkedit-mousedown.md) 和 [**MouseUp**](inkedit-mouseup.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="f61ca-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events.</span></span> <span data-ttu-id="f61ca-113">如果 [**Click**](inkedit-click.md) 事件中有程式碼，則不會觸發 **DblClick** 事件。</span><span class="sxs-lookup"><span data-stu-id="f61ca-113">If there is code in the [**Click**](inkedit-click.md) event, the **DblClick** event will never trigger.</span></span>

 

<span data-ttu-id="f61ca-114">此事件方法是在 **\_ IInkEditEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="f61ca-114">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="f61ca-115">**\_ IInkEditEvents** 介面會以 **DISPID \_ IeeDblClick** 的識別碼來實作為 IDispatch 介面。</span><span class="sxs-lookup"><span data-stu-id="f61ca-115">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeDblClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f61ca-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f61ca-116">Requirements</span></span>



| <span data-ttu-id="f61ca-117">需求</span><span class="sxs-lookup"><span data-stu-id="f61ca-117">Requirement</span></span> | <span data-ttu-id="f61ca-118">值</span><span class="sxs-lookup"><span data-stu-id="f61ca-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f61ca-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f61ca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f61ca-120">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f61ca-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f61ca-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f61ca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f61ca-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="f61ca-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f61ca-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f61ca-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f61ca-124"><dt>筆跡 (也需要筆跡 \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="f61ca-124"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f61ca-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="f61ca-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="f61ca-126"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f61ca-126"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f61ca-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f61ca-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f61ca-128">InkEdit</span><span class="sxs-lookup"><span data-stu-id="f61ca-128">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




