---
description: 當一個或多個 IInkStrokeDisp 物件加入至 InkStrokes 集合時發生。
ms.assetid: 577ad52b-ecd3-4a49-8997-481ebdb47203
title: 'InkPicture. StrokesAdded 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e79d87a4315068cbb0cf9db25b6532bc4c09943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975807"
---
# <a name="inkpicturestrokesadded-event"></a><span data-ttu-id="3112a-103">InkPicture. StrokesAdded 事件</span><span class="sxs-lookup"><span data-stu-id="3112a-103">InkPicture.StrokesAdded event</span></span>

<span data-ttu-id="3112a-104">當一個或多個 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件加入至 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合時發生。</span><span class="sxs-lookup"><span data-stu-id="3112a-104">Occurs when one or more [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects are added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3112a-105">語法</span><span class="sxs-lookup"><span data-stu-id="3112a-105">Syntax</span></span>


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="3112a-106">參數</span><span class="sxs-lookup"><span data-stu-id="3112a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3112a-107">*StrokeIds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3112a-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3112a-108">當此事件發生時，所加入之每個 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件的識別碼的整數陣列。</span><span class="sxs-lookup"><span data-stu-id="3112a-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object added when this event occurs.</span></span>

<span data-ttu-id="3112a-109">如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="3112a-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3112a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3112a-110">Return value</span></span>

<span data-ttu-id="3112a-111">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3112a-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3112a-112">備註</span><span class="sxs-lookup"><span data-stu-id="3112a-112">Remarks</span></span>

<span data-ttu-id="3112a-113">此事件方法是在 **\_ IInkStrokesEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="3112a-113">This event method is defined in the **\_IInkStrokesEvents** interface.</span></span> <span data-ttu-id="3112a-114">**\_ IInkStrokesEvents** 介面會以 DISPID SEStrokesAdded 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3112a-114">The **\_IInkStrokesEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="3112a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3112a-115">Requirements</span></span>



| <span data-ttu-id="3112a-116">需求</span><span class="sxs-lookup"><span data-stu-id="3112a-116">Requirement</span></span> | <span data-ttu-id="3112a-117">值</span><span class="sxs-lookup"><span data-stu-id="3112a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3112a-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3112a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3112a-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3112a-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3112a-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3112a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3112a-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="3112a-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3112a-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3112a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3112a-123"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="3112a-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3112a-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="3112a-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="3112a-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3112a-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3112a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3112a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3112a-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="3112a-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

