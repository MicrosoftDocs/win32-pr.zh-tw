---
description: 發生于按兩下 InkPicture 控制項時。
ms.assetid: 5b2a6413-d415-4bf1-a291-35f4c3c5a0dc
title: InkPicture (Msinkaut) 的 DblClick 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c3d9bb9125c8142186da969acf6ce03f5f76b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320131"
---
# <a name="inkpicturedblclick-event"></a><span data-ttu-id="1fcec-103">InkPicture： DblClick 事件</span><span class="sxs-lookup"><span data-stu-id="1fcec-103">InkPicture.DblClick event</span></span>

<span data-ttu-id="1fcec-104">發生于按兩下 [InkPicture](inkpicture-control-reference.md) 控制項時。</span><span class="sxs-lookup"><span data-stu-id="1fcec-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fcec-105">語法</span><span class="sxs-lookup"><span data-stu-id="1fcec-105">Syntax</span></span>


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="1fcec-106">參數</span><span class="sxs-lookup"><span data-stu-id="1fcec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fcec-107">*取消* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1fcec-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fcec-108">是否應該取消父控制項的事件。</span><span class="sxs-lookup"><span data-stu-id="1fcec-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fcec-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="1fcec-109">Return value</span></span>

<span data-ttu-id="1fcec-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1fcec-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fcec-111">備註</span><span class="sxs-lookup"><span data-stu-id="1fcec-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1fcec-112">若要區分左、右和中間的按鍵，請使用 [**MouseDown**](inkpicture-mousedown.md) 和 [**MouseUp**](inkpicture-mouseup.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="1fcec-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events.</span></span> <span data-ttu-id="1fcec-113">如果 [**Click**](inkpicture-click.md) 事件中有程式碼，則不會觸發 **DblClick** 事件。</span><span class="sxs-lookup"><span data-stu-id="1fcec-113">If there is code in the [**Click**](inkpicture-click.md) event, the **DblClick** event will never trigger.</span></span>

 

<span data-ttu-id="1fcec-114">此事件方法是在 **\_ IInkPictureEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="1fcec-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="1fcec-115">**\_ IInkPictureEvents** 介面會以 **DISPID \_ IPEDblClick** 的識別碼來實作為 IDispatch 介面。</span><span class="sxs-lookup"><span data-stu-id="1fcec-115">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEDblClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fcec-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fcec-116">Requirements</span></span>



| <span data-ttu-id="1fcec-117">需求</span><span class="sxs-lookup"><span data-stu-id="1fcec-117">Requirement</span></span> | <span data-ttu-id="1fcec-118">值</span><span class="sxs-lookup"><span data-stu-id="1fcec-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fcec-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1fcec-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1fcec-120">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1fcec-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1fcec-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1fcec-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1fcec-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="1fcec-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1fcec-123">標頭</span><span class="sxs-lookup"><span data-stu-id="1fcec-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fcec-124"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="1fcec-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1fcec-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="1fcec-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="1fcec-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fcec-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1fcec-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fcec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fcec-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="1fcec-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




