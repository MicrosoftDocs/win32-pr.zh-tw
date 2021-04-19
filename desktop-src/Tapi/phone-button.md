---
description: 傳送 TAPI 電話 \_ 按鈕訊息以通知應用程式，如果偵測到按鈕按下本機電話，則會啟用按鈕的按下監視。
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: 'PHONE_BUTTON 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da810630a937f8415e070373f359dca06a694e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997708"
---
# <a name="phone_button-message"></a><span data-ttu-id="3dd40-103">電話 \_ 按鈕訊息</span><span class="sxs-lookup"><span data-stu-id="3dd40-103">PHONE\_BUTTON message</span></span>

<span data-ttu-id="3dd40-104">傳送 TAPI **電話 \_ 按鈕** 訊息以通知應用程式，如果偵測到按鈕按下本機電話，則會啟用按鈕的按下監視。</span><span class="sxs-lookup"><span data-stu-id="3dd40-104">The TAPI **PHONE\_BUTTON** message is sent to notify the application that button press monitoring is enabled if it has detected a button press on the local phone.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="3dd40-105">參數</span><span class="sxs-lookup"><span data-stu-id="3dd40-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dd40-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="3dd40-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="3dd40-107">手機裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3dd40-107">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="3dd40-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="3dd40-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="3dd40-109">開啟手機裝置時提供的應用程式回呼實例。</span><span class="sxs-lookup"><span data-stu-id="3dd40-109">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="3dd40-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="3dd40-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="3dd40-111">已按下按鈕的按鈕/燈泡識別碼。</span><span class="sxs-lookup"><span data-stu-id="3dd40-111">The button/lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="3dd40-112">請注意，按鈕識別碼0到11一律是鍵台按鈕，' 0 ' 是按鈕識別碼零，' 1 ' 是按鈕識別碼 1 (依此類推，透過按鈕識別碼 9) ，以及 ' ' 是按鈕識別碼 \* 10，而 ' \# ' 是按鈕識別碼11。</span><span class="sxs-lookup"><span data-stu-id="3dd40-112">Note that button identifiers zero through 11 are always the KEYPAD buttons, with '0' being button identifier zero, '1' being button identifier 1 (and so on through button identifier 9), and with '\*' being button identifier 10, and '\#' being button identifier 11.</span></span> <span data-ttu-id="3dd40-113">使用 [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) 和 [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)時，可以取得有關按鈕識別碼的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="3dd40-113">Additional information about a button identifier is available with [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) and [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).</span></span>

</dd> <dt>

<span data-ttu-id="3dd40-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="3dd40-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="3dd40-115">按鈕的按鈕模式。</span><span class="sxs-lookup"><span data-stu-id="3dd40-115">The button mode of the button.</span></span> <span data-ttu-id="3dd40-116">此參數會使用其中一個 [**PHONEBUTTONMODE \_ 常數**](phonebuttonmode--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="3dd40-116">This parameter uses one of the [**PHONEBUTTONMODE\_ constants**](phonebuttonmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd40-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="3dd40-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="3dd40-118">指定這是按鈕關閉事件或按鈕的事件。</span><span class="sxs-lookup"><span data-stu-id="3dd40-118">Specifies whether this is a button-down event or a button-up event.</span></span> <span data-ttu-id="3dd40-119">此參數會使用其中一個 [**PHONEBUTTONSTATE \_ 常數**](phonebuttonstate--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="3dd40-119">This parameter uses one of the [**PHONEBUTTONSTATE\_ constants**](phonebuttonstate--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dd40-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="3dd40-120">Return value</span></span>

<span data-ttu-id="3dd40-121">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="3dd40-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dd40-122">備註</span><span class="sxs-lookup"><span data-stu-id="3dd40-122">Remarks</span></span>

<span data-ttu-id="3dd40-123">每當按鈕變更狀態時，就會傳送 **電話 \_ 按鈕** 訊息。</span><span class="sxs-lookup"><span data-stu-id="3dd40-123">A **PHONE\_BUTTON** message is sent whenever a button changes state.</span></span> <span data-ttu-id="3dd40-124">應用程式可保證每個按鈕關閉事件最後都會傳送對應的按鈕 up 事件。</span><span class="sxs-lookup"><span data-stu-id="3dd40-124">An application is guaranteed that for each button down event, it is eventually sent a corresponding button up event.</span></span> <span data-ttu-id="3dd40-125">無法偵測實際按鈕的服務提供者，必須在每個按鈕按下按鈕之後，立即產生按鈕的訊息。</span><span class="sxs-lookup"><span data-stu-id="3dd40-125">A service provider that is incapable of detecting the actual button up is required to generate the button up message shortly after the button down message for each button press.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dd40-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="3dd40-126">Requirements</span></span>



| <span data-ttu-id="3dd40-127">需求</span><span class="sxs-lookup"><span data-stu-id="3dd40-127">Requirement</span></span> | <span data-ttu-id="3dd40-128">值</span><span class="sxs-lookup"><span data-stu-id="3dd40-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3dd40-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="3dd40-129">TAPI version</span></span><br/> | <span data-ttu-id="3dd40-130">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="3dd40-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="3dd40-131">標頭</span><span class="sxs-lookup"><span data-stu-id="3dd40-131">Header</span></span><br/>       | <dl> <span data-ttu-id="3dd40-132"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="3dd40-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dd40-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3dd40-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd40-134">**phoneGetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="3dd40-134">**phoneGetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[<span data-ttu-id="3dd40-135">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="3dd40-135">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




