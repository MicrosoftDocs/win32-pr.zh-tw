---
description: 當選取的輸入法需要應用程式的轉換字串時，通知應用程式。 應用程式會透過 WM \_ IME 要求訊息接收此命令 \_ ，並使用如下所示的參數設定。
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: 'IMR_DOCUMENTFEED 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4fe46f95b7ad17ba7bb7850ec3fb9ca980519f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192666"
---
# <a name="imr_documentfeed-notification-code"></a><span data-ttu-id="f3a69-104">IMR \_ DOCUMENTFEED 通知碼</span><span class="sxs-lookup"><span data-stu-id="f3a69-104">IMR\_DOCUMENTFEED notification code</span></span>

<span data-ttu-id="f3a69-105">當選取的輸入法需要應用程式的轉換字串時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="f3a69-105">Notifies an application when the selected IME needs the converted string from the application.</span></span> <span data-ttu-id="f3a69-106">應用程式會透過 [**WM \_ IME \_ 要求**](wm-ime-request.md) 訊息接收此命令，並使用如下所示的參數設定。</span><span class="sxs-lookup"><span data-stu-id="f3a69-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters set as shown below.</span></span>


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a><span data-ttu-id="f3a69-107">參數</span><span class="sxs-lookup"><span data-stu-id="f3a69-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3a69-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3a69-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="f3a69-109">設定為 IMR \_ DOCUMENTFEED。</span><span class="sxs-lookup"><span data-stu-id="f3a69-109">Set to IMR\_DOCUMENTFEED.</span></span>

</dd> <dt>

<span data-ttu-id="f3a69-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3a69-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f3a69-111">包含 [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) 結構之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="f3a69-111">Pointer to a buffer to contain the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3a69-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3a69-112">Return Value</span></span>

<span data-ttu-id="f3a69-113">傳回目前的漢字重組字串結構。</span><span class="sxs-lookup"><span data-stu-id="f3a69-113">Returns the current reconversion string structure.</span></span> <span data-ttu-id="f3a69-114">如果 *lParam* 設定為 **Null**，則應用程式會傳回緩衝區所需的大小以保存結構。</span><span class="sxs-lookup"><span data-stu-id="f3a69-114">If *lParam* is set to **NULL**, the application returns the required size for the buffer to hold the structure.</span></span> <span data-ttu-id="f3a69-115">如果不成功，此命令會傳回0。</span><span class="sxs-lookup"><span data-stu-id="f3a69-115">The command returns 0 if it does not succeed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3a69-116">備註</span><span class="sxs-lookup"><span data-stu-id="f3a69-116">Remarks</span></span>

<span data-ttu-id="f3a69-117">IME 會快取已轉換的字串，以提升轉換的精確度。</span><span class="sxs-lookup"><span data-stu-id="f3a69-117">The IME caches converted strings for higher conversion accuracy.</span></span> <span data-ttu-id="f3a69-118">輸入法的一個快取限制是在下列情況下，它會遺失轉換的字串：</span><span class="sxs-lookup"><span data-stu-id="f3a69-118">One caching limitation of the IME is that it loses the converted string under the following circumstances:</span></span>

-   <span data-ttu-id="f3a69-119">應用程式的插入號位置是由按鍵（例如，資料指標索引鍵）移動。</span><span class="sxs-lookup"><span data-stu-id="f3a69-119">The caret position for the application is moved by a key, for example, a cursor key.</span></span>
-   <span data-ttu-id="f3a69-120">滑鼠會移動應用程式的插入號位置。</span><span class="sxs-lookup"><span data-stu-id="f3a69-120">The caret position for the application is moved by the mouse.</span></span>
-   <span data-ttu-id="f3a69-121">新檔會開啟。</span><span class="sxs-lookup"><span data-stu-id="f3a69-121">A new document is opened.</span></span>

<span data-ttu-id="f3a69-122">使用 **IMR \_ DOCUMENTFEED** 命令，IME 隨時都可以重新整理其快取字串。</span><span class="sxs-lookup"><span data-stu-id="f3a69-122">With the **IMR\_DOCUMENTFEED** command, the IME can refresh its cached strings any time.</span></span> <span data-ttu-id="f3a69-123">使用這個命令可改善轉換的精確度。</span><span class="sxs-lookup"><span data-stu-id="f3a69-123">Use of this command improves conversion accuracy.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a69-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3a69-124">Requirements</span></span>



| <span data-ttu-id="f3a69-125">需求</span><span class="sxs-lookup"><span data-stu-id="f3a69-125">Requirement</span></span> | <span data-ttu-id="f3a69-126">值</span><span class="sxs-lookup"><span data-stu-id="f3a69-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a69-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3a69-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f3a69-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3a69-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f3a69-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3a69-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f3a69-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3a69-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f3a69-131">標頭</span><span class="sxs-lookup"><span data-stu-id="f3a69-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3a69-132"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f3a69-132"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3a69-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3a69-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a69-134">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="f3a69-134">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="f3a69-135">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="f3a69-135">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="f3a69-136">**RECONVERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="f3a69-136">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="f3a69-137">**WM \_ IME \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="f3a69-137">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




