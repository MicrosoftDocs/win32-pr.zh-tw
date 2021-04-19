---
description: 已取代。 PenInputPanel 已由文字輸入面板取代 (提示) 。在 PenInputPanel 物件能夠將使用者輸入插入附加控制項之前變更輸入焦點時發生。
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: 'PenInputPanel. InputFailed 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 198c2b466dc03357d9851d7c8a6b7f44c6bf6884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998173"
---
# <a name="peninputpanelinputfailed-event"></a><span data-ttu-id="c2c0c-104">PenInputPanel. InputFailed 事件</span><span class="sxs-lookup"><span data-stu-id="c2c0c-104">PenInputPanel.InputFailed event</span></span>

<span data-ttu-id="c2c0c-105">已取代。</span><span class="sxs-lookup"><span data-stu-id="c2c0c-105">Deprecated.</span></span> <span data-ttu-id="c2c0c-106">[**PenInputPanel**](peninputpanel-class.md)已由 [文字輸入面板取代 (提示)](text-input-panel-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="c2c0c-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="c2c0c-107">在 [**PenInputPanel**](peninputpanel-class.md) 物件能夠將使用者輸入插入附加控制項之前變更輸入焦點時發生。</span><span class="sxs-lookup"><span data-stu-id="c2c0c-107">Occurs when input focus changes before the [**PenInputPanel**](peninputpanel-class.md) object was able to insert user input into the attached control.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2c0c-108">語法</span><span class="sxs-lookup"><span data-stu-id="c2c0c-108">Syntax</span></span>


```C++
HRESULT InputFailed(
  [in] long  hWnd,
  [in] long  Key,
  [in] BSTR  Text,
  [in] short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="c2c0c-109">參數</span><span class="sxs-lookup"><span data-stu-id="c2c0c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2c0c-110">*hWnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2c0c-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2c0c-111">叫用 [**PenInputPanel**](peninputpanel-class.md) 物件之控制項的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="c2c0c-111">The window handle of the control that invoked the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="c2c0c-112">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2c0c-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2c0c-113">對應到所按下之索引鍵的虛擬機器碼。</span><span class="sxs-lookup"><span data-stu-id="c2c0c-113">The virtual key corresponding to the key pressed.</span></span>

</dd> <dt>

<span data-ttu-id="c2c0c-114">*文字* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2c0c-114">*Text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2c0c-115">當引發 **InputFailed** 事件時，要插入 *hWnd* 參數所代表之控制項中的字串。</span><span class="sxs-lookup"><span data-stu-id="c2c0c-115">The string that was to be inserted into the control represented by the *hWnd* parameter when the **InputFailed** event was raised.</span></span>

<span data-ttu-id="c2c0c-116">如需 BSTR 資料類型的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="c2c0c-116">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2c0c-117">*ShiftKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2c0c-117">*ShiftKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2c0c-118">鍵盤修飾詞的狀態，包括 SHIFT、CAPS、CTRL 和 ALT。</span><span class="sxs-lookup"><span data-stu-id="c2c0c-118">The state of the keyboard modifiers, including SHIFT, CAPS, CTRL, and ALT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2c0c-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2c0c-119">Return value</span></span>

<span data-ttu-id="c2c0c-120">如果此事件成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c2c0c-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c2c0c-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c2c0c-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2c0c-122">備註</span><span class="sxs-lookup"><span data-stu-id="c2c0c-122">Remarks</span></span>

<span data-ttu-id="c2c0c-123">當輸入焦點在使用者輸入插入附加控制項之前變更時，就會發生 **InputFailed** 事件。</span><span class="sxs-lookup"><span data-stu-id="c2c0c-123">The **InputFailed** event occurs when input focus changes before user input was inserted into the attached control.</span></span> <span data-ttu-id="c2c0c-124">例如，如果使用者在書寫板中輸入筆墨，然後在辨識器有機會完成之前先點擊另一個編輯控制項，就會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="c2c0c-124">For example, if the user enters ink into the writing pad, then taps on another edit control before the recognizer has had a chance to finish, this event fires.</span></span>

<span data-ttu-id="c2c0c-125">使用傳遞至這個事件的視窗控制碼，您可以選擇在發生這個事件時，自行插入文字。</span><span class="sxs-lookup"><span data-stu-id="c2c0c-125">Using the window handle passed into this event, you can choose to insert the text yourself when this event occurs.</span></span>

> [!Note]  
> <span data-ttu-id="c2c0c-126">從 Microsoft Windows XP Tablet PC Edition 2005 開始， **InputFailed** 活動不再適用。</span><span class="sxs-lookup"><span data-stu-id="c2c0c-126">Starting with Microsoft Windows XP Tablet PC Edition 2005, the **InputFailed** event no longer applies.</span></span> <span data-ttu-id="c2c0c-127">文字一律會在焦點變更之前插入。</span><span class="sxs-lookup"><span data-stu-id="c2c0c-127">Text is always inserted before focus changes.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c2c0c-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2c0c-128">Requirements</span></span>



| <span data-ttu-id="c2c0c-129">需求</span><span class="sxs-lookup"><span data-stu-id="c2c0c-129">Requirement</span></span> | <span data-ttu-id="c2c0c-130">值</span><span class="sxs-lookup"><span data-stu-id="c2c0c-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c0c-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2c0c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c2c0c-132">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2c0c-132">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c2c0c-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2c0c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c2c0c-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="c2c0c-134">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c2c0c-135">標頭</span><span class="sxs-lookup"><span data-stu-id="c2c0c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2c0c-136"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="c2c0c-136"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c2c0c-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="c2c0c-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2c0c-138"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2c0c-138"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c2c0c-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2c0c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2c0c-140">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="c2c0c-140">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




