---
description: 當使用者在 InkEdit 控制項具有焦點時按下並放開按鍵時發生。
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: 'InkEdit： KeyPress 事件 (筆跡 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e49264f82b2cfe3c6998666339f08340a540791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990305"
---
# <a name="inkeditkeypress-event"></a><span data-ttu-id="a6c47-103">InkEdit 的按鍵事件</span><span class="sxs-lookup"><span data-stu-id="a6c47-103">InkEdit.KeyPress event</span></span>

<span data-ttu-id="a6c47-104">當使用者在 [InkEdit](inkedit-control-reference.md) 控制項具有焦點時按下並放開按鍵時發生。</span><span class="sxs-lookup"><span data-stu-id="a6c47-104">Occurs when the user presses and releases a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6c47-105">語法</span><span class="sxs-lookup"><span data-stu-id="a6c47-105">Syntax</span></span>


```C++
HRESULT KeyPress(
   Long *Char
);
```



## <a name="parameters"></a><span data-ttu-id="a6c47-106">參數</span><span class="sxs-lookup"><span data-stu-id="a6c47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6c47-107">*Char*</span><span class="sxs-lookup"><span data-stu-id="a6c47-107">*Char*</span></span> 
</dt> <dd>

<span data-ttu-id="a6c47-108">傳回標準數值 ANSI keycode 的整數。</span><span class="sxs-lookup"><span data-stu-id="a6c47-108">An integer that returns a standard numeric ANSI keycode.</span></span> <span data-ttu-id="a6c47-109">*Char* 參數是以傳址方式傳遞;變更它會將不同的字元傳送給控制項。</span><span class="sxs-lookup"><span data-stu-id="a6c47-109">The *Char* parameter is passed by reference; changing it sends a different character to the control.</span></span> <span data-ttu-id="a6c47-110">將 *Char* 參數變更為0會取消事件。</span><span class="sxs-lookup"><span data-stu-id="a6c47-110">Changing the *Char* parameter to 0 cancels the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6c47-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6c47-111">Return value</span></span>

<span data-ttu-id="a6c47-112">如果此事件成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a6c47-112">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a6c47-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a6c47-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6c47-114">備註</span><span class="sxs-lookup"><span data-stu-id="a6c47-114">Remarks</span></span>

<span data-ttu-id="a6c47-115">此事件方法是在 **\_ IInkEditEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="a6c47-115">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="a6c47-116">**\_ IInkEditEvents** 介面會以 DISPID IeeKeyPress 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a6c47-116">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyPress.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6c47-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6c47-117">Requirements</span></span>



| <span data-ttu-id="a6c47-118">需求</span><span class="sxs-lookup"><span data-stu-id="a6c47-118">Requirement</span></span> | <span data-ttu-id="a6c47-119">值</span><span class="sxs-lookup"><span data-stu-id="a6c47-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6c47-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6c47-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a6c47-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6c47-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a6c47-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6c47-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a6c47-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="a6c47-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a6c47-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a6c47-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6c47-125"><dt>筆跡 (也需要筆跡 \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="a6c47-125"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a6c47-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="a6c47-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a6c47-127"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6c47-127"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a6c47-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6c47-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6c47-129">InkEdit</span><span class="sxs-lookup"><span data-stu-id="a6c47-129">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

<span data-ttu-id="a6c47-130">[**KeyDown 事件 \[ InkEdit 控制項\]**](inkedit-keydown.md)</span><span class="sxs-lookup"><span data-stu-id="a6c47-130">[**KeyDown Event \[InkEdit Control\]**](inkedit-keydown.md)</span></span>
</dt> <dt>

<span data-ttu-id="a6c47-131">[**KeyUp 事件 \[ InkEdit 控制項\]**](inkedit-keyup.md)</span><span class="sxs-lookup"><span data-stu-id="a6c47-131">[**KeyUp Event \[InkEdit Control\]**](inkedit-keyup.md)</span></span>
</dt> </dl>

 

