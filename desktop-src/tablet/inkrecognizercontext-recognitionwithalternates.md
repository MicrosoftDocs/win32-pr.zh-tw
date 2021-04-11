---
description: InkRecognizerCoNtext 類別在呼叫 BackgroundRecognizeWithAlternates 方法方法之後產生結果時發生。
ms.assetid: 5e86a4d5-c0a7-4283-81cc-ec3a26f74880
title: 'InkRecognizerCoNtext. RecognitionWithAlternates 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a7d35d8281305b0cb5f84114bb2f2fa0e718c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193723"
---
# <a name="inkrecognizercontextrecognitionwithalternates-event"></a><span data-ttu-id="f8cf9-103">InkRecognizerCoNtext. RecognitionWithAlternates 事件</span><span class="sxs-lookup"><span data-stu-id="f8cf9-103">InkRecognizerContext.RecognitionWithAlternates event</span></span>

<span data-ttu-id="f8cf9-104">[**InkRecognizerCoNtext 類別**](inkrecognizercontext-class.md)在呼叫 [**BackgroundRecognizeWithAlternates 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)方法之後產生結果時發生。</span><span class="sxs-lookup"><span data-stu-id="f8cf9-104">Occurs when the [**InkRecognizerContext Class**](inkrecognizercontext-class.md) has generated results after calling the [**BackgroundRecognizeWithAlternates Method**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8cf9-105">語法</span><span class="sxs-lookup"><span data-stu-id="f8cf9-105">Syntax</span></span>


```C++
void RecognitionWithAlternates(
  [in] IInkRecognitionResult *RecognitionResult,
  [in] VARIANT               CustomData,
  [in] InkRecognitionStatus  RecognitionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="f8cf9-106">參數</span><span class="sxs-lookup"><span data-stu-id="f8cf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8cf9-107">*RecognitionResult* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8cf9-107">*RecognitionResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8cf9-108">事件的辨識結果。</span><span class="sxs-lookup"><span data-stu-id="f8cf9-108">The recognition result from the event.</span></span>

</dd> <dt>

<span data-ttu-id="f8cf9-109">*CustomData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8cf9-109">*CustomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8cf9-110">辨識結果的自訂資料。</span><span class="sxs-lookup"><span data-stu-id="f8cf9-110">The custom data for the recognition result.</span></span>

<span data-ttu-id="f8cf9-111">如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="f8cf9-111">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8cf9-112">*RecognitionStatus* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8cf9-112">*RecognitionStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8cf9-113">從最新的辨識結果到的認可狀態。</span><span class="sxs-lookup"><span data-stu-id="f8cf9-113">The recognition status as of the most recent recognition result.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8cf9-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8cf9-114">Return value</span></span>

<span data-ttu-id="f8cf9-115">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f8cf9-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8cf9-116">備註</span><span class="sxs-lookup"><span data-stu-id="f8cf9-116">Remarks</span></span>

<span data-ttu-id="f8cf9-117">如果您嘗試從辨識事件處理常式取得原始 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 物件的存取權，則應用程式開發介面 (API) 的行為無法預期。</span><span class="sxs-lookup"><span data-stu-id="f8cf9-117">The behavior of the application programming interface (API) is unpredictable if you try to gain access to the original [**InkRecognizerContext**](inkrecognizercontext-class.md) object from the recognition event handler.</span></span> <span data-ttu-id="f8cf9-118">請勿嘗試這麼做。</span><span class="sxs-lookup"><span data-stu-id="f8cf9-118">Do not attempt to do this.</span></span> <span data-ttu-id="f8cf9-119">相反地，如果您需要這樣做，請建立旗標， [**並在辨識事件處理**](inkrecognizercontext-recognition.md) 程式中加以設定。</span><span class="sxs-lookup"><span data-stu-id="f8cf9-119">Instead, if you need to do this, create a flag and set it in the [**Recognition**](inkrecognizercontext-recognition.md) event handler.</span></span> <span data-ttu-id="f8cf9-120">然後您可以輪詢該旗標，判斷何時要變更事件處理常式以外的 **InkRecognizerCoNtext** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f8cf9-120">Then you can poll that flag to determine when to change the **InkRecognizerContext** properties outside of the event handler.</span></span>

<span data-ttu-id="f8cf9-121">此事件方法是在 \_ IInkEvents 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="f8cf9-121">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="f8cf9-122">\_IInkEvents 介面會以 DISPID IRERecognitionWithAlternates 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f8cf9-122">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IRERecognitionWithAlternates.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8cf9-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8cf9-123">Requirements</span></span>



| <span data-ttu-id="f8cf9-124">需求</span><span class="sxs-lookup"><span data-stu-id="f8cf9-124">Requirement</span></span> | <span data-ttu-id="f8cf9-125">值</span><span class="sxs-lookup"><span data-stu-id="f8cf9-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8cf9-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8cf9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f8cf9-127">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8cf9-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f8cf9-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8cf9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f8cf9-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="f8cf9-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f8cf9-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f8cf9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8cf9-131"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="f8cf9-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f8cf9-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="f8cf9-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8cf9-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8cf9-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f8cf9-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8cf9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8cf9-135">**InkRecognizerCoNtext 類別**</span><span class="sxs-lookup"><span data-stu-id="f8cf9-135">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

[<span data-ttu-id="f8cf9-136">**BackgroundRecognizeWithAlternates 方法**</span><span class="sxs-lookup"><span data-stu-id="f8cf9-136">**BackgroundRecognizeWithAlternates Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)
</dt> <dt>

[<span data-ttu-id="f8cf9-137">**辨識方法**</span><span class="sxs-lookup"><span data-stu-id="f8cf9-137">**Recognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[<span data-ttu-id="f8cf9-138">**IInkRecognitionResult 介面**</span><span class="sxs-lookup"><span data-stu-id="f8cf9-138">**IInkRecognitionResult Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

