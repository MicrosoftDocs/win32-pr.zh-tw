---
description: 當 InkEdit 控制項以手動方式從 InkEdit：：辨識方法的呼叫取得結果，或在辨識超時引發之後自動取得結果時發生。
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: 'InkEdit. RecognitionResult 事件 (筆跡 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d6206293b604e5540b5e6d0271e1ebe984a987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194797"
---
# <a name="inkeditrecognitionresult-event"></a><span data-ttu-id="cf89a-103">InkEdit. RecognitionResult 事件</span><span class="sxs-lookup"><span data-stu-id="cf89a-103">InkEdit.RecognitionResult event</span></span>

<span data-ttu-id="cf89a-104">當 [InkEdit](inkedit-control-reference.md) 控制項以手動方式從 [**InkEdit：：辨識**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) 方法的呼叫取得結果，或在辨識超時引發之後自動取得結果時發生。</span><span class="sxs-lookup"><span data-stu-id="cf89a-104">Occurs when the [InkEdit](inkedit-control-reference.md) control gets results manually from a call to the [**InkEdit::Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) method or automatically after the recognition timeout fires.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf89a-105">語法</span><span class="sxs-lookup"><span data-stu-id="cf89a-105">Syntax</span></span>


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a><span data-ttu-id="cf89a-106">參數</span><span class="sxs-lookup"><span data-stu-id="cf89a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf89a-107">*RecognitionResult* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf89a-107">*RecognitionResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf89a-108">[**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)物件，其中包含辨識的結果。</span><span class="sxs-lookup"><span data-stu-id="cf89a-108">An [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object that contains the result of the recognition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf89a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf89a-109">Return value</span></span>

<span data-ttu-id="cf89a-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cf89a-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf89a-111">備註</span><span class="sxs-lookup"><span data-stu-id="cf89a-111">Remarks</span></span>

<span data-ttu-id="cf89a-112">此事件方法是在 **\_ IInkEditEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="cf89a-112">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="cf89a-113">**\_ IInkEditEvents** 介面會以 DISPID IeeRecognitionResult 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cf89a-113">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeRecognitionResult.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf89a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf89a-114">Requirements</span></span>



| <span data-ttu-id="cf89a-115">需求</span><span class="sxs-lookup"><span data-stu-id="cf89a-115">Requirement</span></span> | <span data-ttu-id="cf89a-116">值</span><span class="sxs-lookup"><span data-stu-id="cf89a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf89a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf89a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cf89a-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf89a-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cf89a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf89a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cf89a-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="cf89a-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cf89a-121">標頭</span><span class="sxs-lookup"><span data-stu-id="cf89a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf89a-122"><dt>筆跡 (也需要筆跡 \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="cf89a-122"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cf89a-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="cf89a-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf89a-124"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf89a-124"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cf89a-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf89a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf89a-126">InkEdit</span><span class="sxs-lookup"><span data-stu-id="cf89a-126">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

<span data-ttu-id="cf89a-127">[**辨識方法 \[ InkEdit 控制項\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)</span><span class="sxs-lookup"><span data-stu-id="cf89a-127">[**Recognize Method \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)</span></span>
</dt> </dl>

 

