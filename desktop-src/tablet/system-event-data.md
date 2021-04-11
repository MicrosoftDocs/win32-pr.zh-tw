---
description: 包含 tablet 系統事件的相關資訊。
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: SYSTEM_EVENT_DATA 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_EVENT_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5d77c78a78a6cecae0368e8d9192a0dc0efc10e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195317"
---
# <a name="system_event_data-structure"></a><span data-ttu-id="32bcb-103">系統 \_ 事件 \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="32bcb-103">SYSTEM\_EVENT\_DATA structure</span></span>

<span data-ttu-id="32bcb-104">包含 tablet 系統事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="32bcb-104">Contains information about a tablet system event.</span></span>

## <a name="syntax"></a><span data-ttu-id="32bcb-105">語法</span><span class="sxs-lookup"><span data-stu-id="32bcb-105">Syntax</span></span>


```C++
typedef struct tagSYSTEM_EVENT_DATA {
  BYTE  bModifier;
  WCHAR wKey;
  LONG  xPos;
  LONG  yPos;
  BYTE  bCursorMode;
  DWORD dwButtonState;
} SYSTEM_EVENT_DATA;
```



## <a name="members"></a><span data-ttu-id="32bcb-106">成員</span><span class="sxs-lookup"><span data-stu-id="32bcb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="32bcb-107">**bModifier**</span><span class="sxs-lookup"><span data-stu-id="32bcb-107">**bModifier**</span></span>
</dt> <dd>

<span data-ttu-id="32bcb-108">修飾詞的位值。</span><span class="sxs-lookup"><span data-stu-id="32bcb-108">Bit values for the modifiers.</span></span> <span data-ttu-id="32bcb-109">如需詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="32bcb-109">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="32bcb-110">**wKey**</span><span class="sxs-lookup"><span data-stu-id="32bcb-110">**wKey**</span></span>
</dt> <dd>

<span data-ttu-id="32bcb-111">掃描鍵盤字元的程式碼。</span><span class="sxs-lookup"><span data-stu-id="32bcb-111">Scan code for the keyboard character.</span></span>

</dd> <dt>

<span data-ttu-id="32bcb-112">**xPos**</span><span class="sxs-lookup"><span data-stu-id="32bcb-112">**xPos**</span></span>
</dt> <dd>

<span data-ttu-id="32bcb-113">事件的 X 位置。</span><span class="sxs-lookup"><span data-stu-id="32bcb-113">X position of the event.</span></span>

</dd> <dt>

<span data-ttu-id="32bcb-114">**yPos**</span><span class="sxs-lookup"><span data-stu-id="32bcb-114">**yPos**</span></span>
</dt> <dd>

<span data-ttu-id="32bcb-115">事件的 Y 位置。</span><span class="sxs-lookup"><span data-stu-id="32bcb-115">Y position of the event.</span></span>

</dd> <dt>

<span data-ttu-id="32bcb-116">**bCursorMode**</span><span class="sxs-lookup"><span data-stu-id="32bcb-116">**bCursorMode**</span></span>
</dt> <dd>

<span data-ttu-id="32bcb-117">造成事件的資料指標類型。</span><span class="sxs-lookup"><span data-stu-id="32bcb-117">The type of cursor that caused the event.</span></span> <span data-ttu-id="32bcb-118">如需詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="32bcb-118">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="32bcb-119">**dwButtonState**</span><span class="sxs-lookup"><span data-stu-id="32bcb-119">**dwButtonState**</span></span>
</dt> <dd>

<span data-ttu-id="32bcb-120">系統事件時按鈕的狀態。</span><span class="sxs-lookup"><span data-stu-id="32bcb-120">State of the buttons at the time of the system event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32bcb-121">備註</span><span class="sxs-lookup"><span data-stu-id="32bcb-121">Remarks</span></span>

<span data-ttu-id="32bcb-122">下列系統事件已定義為在 **bModifier** 成員中使用。</span><span class="sxs-lookup"><span data-stu-id="32bcb-122">The following system events are defined for use in the **bModifier** member.</span></span>



| <span data-ttu-id="32bcb-123">值</span><span class="sxs-lookup"><span data-stu-id="32bcb-123">Value</span></span>               | <span data-ttu-id="32bcb-124">描述</span><span class="sxs-lookup"><span data-stu-id="32bcb-124">Description</span></span>                  |
|---------------------|------------------------------|
| <span data-ttu-id="32bcb-125">SE \_ 修飾詞 \_ CTRL</span><span class="sxs-lookup"><span data-stu-id="32bcb-125">SE\_MODIFIER\_CTRL</span></span>  | <span data-ttu-id="32bcb-126">已按下控制項鍵。</span><span class="sxs-lookup"><span data-stu-id="32bcb-126">The Control key was pressed.</span></span> |
| <span data-ttu-id="32bcb-127">SE \_ 修飾詞 \_ ALT</span><span class="sxs-lookup"><span data-stu-id="32bcb-127">SE\_MODIFIER\_ALT</span></span>   | <span data-ttu-id="32bcb-128">已按下 ALT 鍵。</span><span class="sxs-lookup"><span data-stu-id="32bcb-128">The Alt key was pressed.</span></span>     |
| <span data-ttu-id="32bcb-129">SE \_ 修飾詞 \_ 移位</span><span class="sxs-lookup"><span data-stu-id="32bcb-129">SE\_MODIFIER\_SHIFT</span></span> | <span data-ttu-id="32bcb-130">已按下 Shift 鍵。</span><span class="sxs-lookup"><span data-stu-id="32bcb-130">The Shift key was pressed.</span></span>   |



 

<span data-ttu-id="32bcb-131">下列系統事件已定義為在 **bCursorMode** 成員中使用。</span><span class="sxs-lookup"><span data-stu-id="32bcb-131">The following system events are defined for use in the **bCursorMode** member.</span></span>



| <span data-ttu-id="32bcb-132">值</span><span class="sxs-lookup"><span data-stu-id="32bcb-132">Value</span></span>              | <span data-ttu-id="32bcb-133">描述</span><span class="sxs-lookup"><span data-stu-id="32bcb-133">Description</span></span>               |
|--------------------|---------------------------|
| <span data-ttu-id="32bcb-134">SE \_ 正常資料 \_ 指標</span><span class="sxs-lookup"><span data-stu-id="32bcb-134">SE\_NORMAL\_CURSOR</span></span> | <span data-ttu-id="32bcb-135">表示畫筆提示。</span><span class="sxs-lookup"><span data-stu-id="32bcb-135">Indicates the pen tip.</span></span>    |
| <span data-ttu-id="32bcb-136">SE \_ 橡皮擦 \_ 游標</span><span class="sxs-lookup"><span data-stu-id="32bcb-136">SE\_ERASER\_CURSOR</span></span> | <span data-ttu-id="32bcb-137">表示畫筆橡皮擦。</span><span class="sxs-lookup"><span data-stu-id="32bcb-137">Indicates the pen eraser.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="32bcb-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="32bcb-138">Requirements</span></span>



| <span data-ttu-id="32bcb-139">需求</span><span class="sxs-lookup"><span data-stu-id="32bcb-139">Requirement</span></span> | <span data-ttu-id="32bcb-140">值</span><span class="sxs-lookup"><span data-stu-id="32bcb-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="32bcb-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32bcb-141">Minimum supported client</span></span><br/> | <span data-ttu-id="32bcb-142">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32bcb-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="32bcb-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32bcb-143">Minimum supported server</span></span><br/> | <span data-ttu-id="32bcb-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="32bcb-144">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="32bcb-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32bcb-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32bcb-146">**IStylusPlugin：： SystemEvent 方法**</span><span class="sxs-lookup"><span data-stu-id="32bcb-146">**IStylusPlugin::SystemEvent Method**</span></span>](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[<span data-ttu-id="32bcb-147">**ITabletEventSink：： SystemEvent 方法**</span><span class="sxs-lookup"><span data-stu-id="32bcb-147">**ITabletEventSink::SystemEvent Method**</span></span>](itableteventsink-systemevent.md)
</dt> </dl>

 

 




