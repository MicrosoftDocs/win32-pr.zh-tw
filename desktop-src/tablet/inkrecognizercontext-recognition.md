---
description: 當 InkRecognizerCoNtext 從 BackgroundRecognize 方法產生結果時發生。
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: 'InkRecognizerCoNtext 識別事件 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86da1a7470169f9f978e92a87f3e32f7e63acb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987751"
---
# <a name="inkrecognizercontextrecognition-event"></a><span data-ttu-id="016a5-103">InkRecognizerCoNtext 辨識事件</span><span class="sxs-lookup"><span data-stu-id="016a5-103">InkRecognizerContext.Recognition event</span></span>

<span data-ttu-id="016a5-104">當 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 從 [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) 方法產生結果時發生。</span><span class="sxs-lookup"><span data-stu-id="016a5-104">Occurs when the [**InkRecognizerContext**](inkrecognizercontext-class.md) has generated results from the [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="016a5-105">語法</span><span class="sxs-lookup"><span data-stu-id="016a5-105">Syntax</span></span>


```C++
void Recognition(
  [in] BSTR                 RecognizedString,
  [in] VARIANT              CustomData,
  [in] InkRecognitionStatus RecognitionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="016a5-106">參數</span><span class="sxs-lookup"><span data-stu-id="016a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="016a5-107">*RecognizedString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="016a5-107">*RecognizedString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="016a5-108">具有最高信賴度的辨識結果文字。</span><span class="sxs-lookup"><span data-stu-id="016a5-108">The recognition result text with the highest confidence.</span></span>

<span data-ttu-id="016a5-109">如需 BSTR 資料類型的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="016a5-109">For more information about the BSTR data type, see the [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="016a5-110">*CustomData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="016a5-110">*CustomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="016a5-111">物件，包含辨識結果的自訂資料。</span><span class="sxs-lookup"><span data-stu-id="016a5-111">The object that contains the custom data for the recognition result.</span></span>

<span data-ttu-id="016a5-112">如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="016a5-112">For more information about the VARIANT structure, see the [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="016a5-113">*RecognitionStatus* \[在\]</span><span class="sxs-lookup"><span data-stu-id="016a5-113">*RecognitionStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="016a5-114">從最新的辨識結果到的認可狀態。</span><span class="sxs-lookup"><span data-stu-id="016a5-114">The recognition status as of the most recent recognition result.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="016a5-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="016a5-115">Return value</span></span>

<span data-ttu-id="016a5-116">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="016a5-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="016a5-117">備註</span><span class="sxs-lookup"><span data-stu-id="016a5-117">Remarks</span></span>

<span data-ttu-id="016a5-118">如果您嘗試從辨識事件處理常式取得原始 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 物件的存取權，則應用程式開發介面 (API) 的行為無法預期。</span><span class="sxs-lookup"><span data-stu-id="016a5-118">The behavior of the application programming interface (API) is unpredictable if you try to gain access to the original [**InkRecognizerContext**](inkrecognizercontext-class.md) object from the recognition event handler.</span></span> <span data-ttu-id="016a5-119">請勿嘗試這麼做。</span><span class="sxs-lookup"><span data-stu-id="016a5-119">Do not attempt to do this.</span></span> <span data-ttu-id="016a5-120">相反地，如果您需要這樣做，請建立旗標， [並在辨識事件處理](ink-recognition.md) 程式中加以設定。</span><span class="sxs-lookup"><span data-stu-id="016a5-120">Instead, if you need to do this, create a flag and set it in the [Recognition](ink-recognition.md) event handler.</span></span> <span data-ttu-id="016a5-121">然後您可以輪詢該旗標，判斷何時要變更事件處理常式以外的 **InkRecognizerCoNtext** 屬性。</span><span class="sxs-lookup"><span data-stu-id="016a5-121">Then you can poll that flag to determine when to change the **InkRecognizerContext** properties outside of the event handler.</span></span>

<span data-ttu-id="016a5-122">此事件方法是在 \_ IInkEvents 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="016a5-122">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="016a5-123">\_IInkEvents 介面會以 DISPID IRERecognition 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="016a5-123">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IRERecognition.</span></span>

## <a name="requirements"></a><span data-ttu-id="016a5-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="016a5-124">Requirements</span></span>



| <span data-ttu-id="016a5-125">需求</span><span class="sxs-lookup"><span data-stu-id="016a5-125">Requirement</span></span> | <span data-ttu-id="016a5-126">值</span><span class="sxs-lookup"><span data-stu-id="016a5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="016a5-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="016a5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="016a5-128">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="016a5-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="016a5-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="016a5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="016a5-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="016a5-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="016a5-131">標頭</span><span class="sxs-lookup"><span data-stu-id="016a5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="016a5-132"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="016a5-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="016a5-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="016a5-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="016a5-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="016a5-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="016a5-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="016a5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="016a5-136">**InkRecognizerCoNtext 類別**</span><span class="sxs-lookup"><span data-stu-id="016a5-136">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

[<span data-ttu-id="016a5-137">**BackgroundRecognize 方法**</span><span class="sxs-lookup"><span data-stu-id="016a5-137">**BackgroundRecognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[<span data-ttu-id="016a5-138">**InkRecognitionStatus 列舉**</span><span class="sxs-lookup"><span data-stu-id="016a5-138">**InkRecognitionStatus Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[<span data-ttu-id="016a5-139">**辨識方法**</span><span class="sxs-lookup"><span data-stu-id="016a5-139">**Recognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[<span data-ttu-id="016a5-140">**IInkRecognitionResult 介面**</span><span class="sxs-lookup"><span data-stu-id="016a5-140">**IInkRecognitionResult Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

