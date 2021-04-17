---
description: 當使用者在 InkEdit 控制項具有焦點時放開按鍵時發生。
ms.assetid: 973d99f2-df09-4315-aaab-72877272100b
title: InkEdit (筆跡) 的 KeyUp 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590f5f6b2e81e1996bca973f4994c0eade7ead18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514024"
---
# <a name="inkeditkeyup-event"></a><span data-ttu-id="0baeb-103">InkEdit KeyUp 事件</span><span class="sxs-lookup"><span data-stu-id="0baeb-103">InkEdit.KeyUp event</span></span>

<span data-ttu-id="0baeb-104">當使用者在 [InkEdit](inkedit-control-reference.md) 控制項具有焦點時放開按鍵時發生。</span><span class="sxs-lookup"><span data-stu-id="0baeb-104">Occurs when the user releases a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="0baeb-105">語法</span><span class="sxs-lookup"><span data-stu-id="0baeb-105">Syntax</span></span>


```C++
HRESULT KeyUp(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="0baeb-106">參數</span><span class="sxs-lookup"><span data-stu-id="0baeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0baeb-107">*pKey*</span><span class="sxs-lookup"><span data-stu-id="0baeb-107">*pKey*</span></span> 
</dt> <dd>

<span data-ttu-id="0baeb-108">使用者按下按鍵的虛擬金鑰碼。</span><span class="sxs-lookup"><span data-stu-id="0baeb-108">The virtual-key code of the key pressed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="0baeb-109">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="0baeb-109">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="0baeb-110">[**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)列舉的成員，指出事件時要按下的輔助按鍵。</span><span class="sxs-lookup"><span data-stu-id="0baeb-110">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="0baeb-111">值</span><span class="sxs-lookup"><span data-stu-id="0baeb-111">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="0baeb-112">意義</span><span class="sxs-lookup"><span data-stu-id="0baeb-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="0baeb-113"><dt>**IKM \_ Shift**</dt></span><span class="sxs-lookup"><span data-stu-id="0baeb-113"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="0baeb-114">指定 SHIFT 鍵已做為修飾詞使用。</span><span class="sxs-lookup"><span data-stu-id="0baeb-114">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="0baeb-115"><dt>**IKM \_控制項**</dt></span><span class="sxs-lookup"><span data-stu-id="0baeb-115"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="0baeb-116">指定使用 CTRL 鍵做為修飾詞。</span><span class="sxs-lookup"><span data-stu-id="0baeb-116">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="0baeb-117"><dt>**IKM \_Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="0baeb-117"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="0baeb-118">指定使用 ALT 鍵做為修飾詞。</span><span class="sxs-lookup"><span data-stu-id="0baeb-118">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0baeb-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="0baeb-119">Return value</span></span>

<span data-ttu-id="0baeb-120">如果此事件成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0baeb-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0baeb-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0baeb-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0baeb-122">備註</span><span class="sxs-lookup"><span data-stu-id="0baeb-122">Remarks</span></span>

<span data-ttu-id="0baeb-123">此事件方法是在 **\_ IInkEditEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="0baeb-123">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="0baeb-124">**\_ IInkEditEvents** 介面會以 DISPID IeeKeyUp 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0baeb-124">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="0baeb-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="0baeb-125">Requirements</span></span>



| <span data-ttu-id="0baeb-126">需求</span><span class="sxs-lookup"><span data-stu-id="0baeb-126">Requirement</span></span> | <span data-ttu-id="0baeb-127">值</span><span class="sxs-lookup"><span data-stu-id="0baeb-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0baeb-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0baeb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0baeb-129">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0baeb-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0baeb-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0baeb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0baeb-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="0baeb-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0baeb-132">標頭</span><span class="sxs-lookup"><span data-stu-id="0baeb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0baeb-133"><dt>筆跡 (也需要筆跡 \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="0baeb-133"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0baeb-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="0baeb-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="0baeb-135"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0baeb-135"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0baeb-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0baeb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0baeb-137">InkEdit</span><span class="sxs-lookup"><span data-stu-id="0baeb-137">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="0baeb-138">**InkShiftKeyModifierFlags 列舉**</span><span class="sxs-lookup"><span data-stu-id="0baeb-138">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="0baeb-139">[**KeyDown 事件 \[ InkEdit 控制項\]**](inkedit-keydown.md)</span><span class="sxs-lookup"><span data-stu-id="0baeb-139">[**KeyDown Event \[InkEdit Control\]**](inkedit-keydown.md)</span></span>
</dt> <dt>

<span data-ttu-id="0baeb-140">[**KeyPress 事件 \[ InkEdit 控制項\]**](inkedit-keypress.md)</span><span class="sxs-lookup"><span data-stu-id="0baeb-140">[**KeyPress Event \[InkEdit Control\]**](inkedit-keypress.md)</span></span>
</dt> </dl>

 

