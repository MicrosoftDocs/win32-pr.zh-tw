---
description: 已取代。 PenInputPanel 已由文字輸入面板取代 (提示) 。在 PenInputPanel 物件于配置之間變更時發生。
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: 'PenInputPanel. PanelChanged 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6ff0f415e12131221a8dad1c0775a347ef96cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320124"
---
# <a name="peninputpanelpanelchanged-event"></a><span data-ttu-id="77c7a-104">PenInputPanel. PanelChanged 事件</span><span class="sxs-lookup"><span data-stu-id="77c7a-104">PenInputPanel.PanelChanged event</span></span>

<span data-ttu-id="77c7a-105">已取代。</span><span class="sxs-lookup"><span data-stu-id="77c7a-105">Deprecated.</span></span> <span data-ttu-id="77c7a-106">[**PenInputPanel**](peninputpanel-class.md)已由 [文字輸入面板取代 (提示)](text-input-panel-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="77c7a-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="77c7a-107">在 [**PenInputPanel**](peninputpanel-class.md) 物件于配置之間變更時發生。</span><span class="sxs-lookup"><span data-stu-id="77c7a-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object changes between layouts.</span></span>

## <a name="syntax"></a><span data-ttu-id="77c7a-108">語法</span><span class="sxs-lookup"><span data-stu-id="77c7a-108">Syntax</span></span>


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a><span data-ttu-id="77c7a-109">參數</span><span class="sxs-lookup"><span data-stu-id="77c7a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77c7a-110">*NewPanelType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77c7a-110">*NewPanelType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77c7a-111">在 **PanelChanged** 事件引發之後，用於 [**PenInputPanel**](peninputpanel-class.md)物件內輸入的新面板型別。</span><span class="sxs-lookup"><span data-stu-id="77c7a-111">The new panel type used for input within the [**PenInputPanel**](peninputpanel-class.md) object, after the **PanelChanged** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77c7a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="77c7a-112">Return value</span></span>

<span data-ttu-id="77c7a-113">如果此事件成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="77c7a-113">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="77c7a-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="77c7a-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="77c7a-115">備註</span><span class="sxs-lookup"><span data-stu-id="77c7a-115">Remarks</span></span>

<span data-ttu-id="77c7a-116">建立 [**PenInputPanel**](peninputpanel-class.md) 物件時， [**手寫**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) 是預設的 **PanelType**。</span><span class="sxs-lookup"><span data-stu-id="77c7a-116">When creating a [**PenInputPanel**](peninputpanel-class.md) object, [**Handwriting**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) is the default **PanelType**.</span></span> <span data-ttu-id="77c7a-117">如果您在 [畫筆輸入面板] 第一次變成作用中之前設定 [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) 屬性來變更面板，則會發生 **PanelChanged** 事件。</span><span class="sxs-lookup"><span data-stu-id="77c7a-117">If you change the panel by setting the [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) property before the pen input panel becomes active for the first time, a **PanelChanged** event occurs.</span></span>

<span data-ttu-id="77c7a-118">當使用者線上條和手寫書寫板之間變更時，不會引發 **PanelChanged** 事件。</span><span class="sxs-lookup"><span data-stu-id="77c7a-118">The **PanelChanged** event is not raised when the user changes between Lined and Boxed writing pads.</span></span>

## <a name="requirements"></a><span data-ttu-id="77c7a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="77c7a-119">Requirements</span></span>



| <span data-ttu-id="77c7a-120">需求</span><span class="sxs-lookup"><span data-stu-id="77c7a-120">Requirement</span></span> | <span data-ttu-id="77c7a-121">值</span><span class="sxs-lookup"><span data-stu-id="77c7a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77c7a-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77c7a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="77c7a-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77c7a-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="77c7a-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77c7a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="77c7a-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="77c7a-125">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="77c7a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="77c7a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="77c7a-127"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="77c7a-127"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="77c7a-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="77c7a-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="77c7a-129"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77c7a-129"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="77c7a-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77c7a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77c7a-131">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="77c7a-131">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 
