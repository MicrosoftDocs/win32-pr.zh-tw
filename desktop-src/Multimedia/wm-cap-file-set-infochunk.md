---
title: 'WM_CAP_FILE_SET_INFOCHUNK 訊息 (Vfw .h) '
description: WM \_ CAP 檔案 \_ \_ 集 INFOCHUNK 訊息會設定 \_ 並清除資訊區塊。
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- WM_CAP_FILE_SET_INFOCHUNK message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_INFOCHUNK
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 067ba00563a5ca511f13b23615fc4542090ba397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024622"
---
# <a name="wm_cap_file_set_infochunk-message"></a><span data-ttu-id="9c975-104">WM \_ CAP \_ FILE \_ SET \_ INFOCHUNK message</span><span class="sxs-lookup"><span data-stu-id="9c975-104">WM\_CAP\_FILE\_SET\_INFOCHUNK message</span></span>

<span data-ttu-id="9c975-105">**WM \_ CAP 檔案 \_ \_ 集 \_ INFOCHUNK** 訊息會設定並清除資訊區塊。</span><span class="sxs-lookup"><span data-stu-id="9c975-105">The **WM\_CAP\_FILE\_SET\_INFOCHUNK** message sets and clears information chunks.</span></span> <span data-ttu-id="9c975-106">資訊區塊可以在 capture 期間插入 AVI 檔案中，以內嵌文字字串或自訂資料。</span><span class="sxs-lookup"><span data-stu-id="9c975-106">Information chunks can be inserted in an AVI file during capture to embed text strings or custom data.</span></span> <span data-ttu-id="9c975-107">您可以使用 [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="9c975-107">You can send this message explicitly or by using the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro.</span></span>


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a><span data-ttu-id="9c975-108">參數</span><span class="sxs-lookup"><span data-stu-id="9c975-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c975-109"><span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*</span><span class="sxs-lookup"><span data-stu-id="9c975-109"><span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*</span></span>
</dt> <dd>

<span data-ttu-id="9c975-110">[**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk)結構的指標，定義要建立或刪除的資訊區塊。</span><span class="sxs-lookup"><span data-stu-id="9c975-110">Pointer to a [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) structure defining the information chunk to be created or deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c975-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c975-111">Return Value</span></span>

<span data-ttu-id="9c975-112">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="9c975-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="9c975-113">如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。</span><span class="sxs-lookup"><span data-stu-id="9c975-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c975-114">備註</span><span class="sxs-lookup"><span data-stu-id="9c975-114">Remarks</span></span>

<span data-ttu-id="9c975-115">您可以將多個已註冊的資訊區塊加入至 AVI 檔案。</span><span class="sxs-lookup"><span data-stu-id="9c975-115">Multiple registered information chunks can be added to an AVI file.</span></span> <span data-ttu-id="9c975-116">設定資訊區塊之後，它會繼續新增至後續的捕獲檔案，直到清除專案或清除所有資訊區塊專案為止。</span><span class="sxs-lookup"><span data-stu-id="9c975-116">After an information chunk is set, it continues to be added to subsequent capture files until either the entry is cleared or all information chunk entries are cleared.</span></span> <span data-ttu-id="9c975-117">若要清除單一專案，請在 **fccInfoID** 成員中指定資訊區塊，並在 [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk)結構的 **lpData** 成員中指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="9c975-117">To clear a single entry, specify the information chunk in the **fccInfoID** member and **NULL** in the **lpData** member of the [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) structure.</span></span> <span data-ttu-id="9c975-118">若要清除所有專案，請在 **fccInfoID** 中指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="9c975-118">To clear all entries, specify **NULL** in **fccInfoID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c975-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c975-119">Requirements</span></span>



| <span data-ttu-id="9c975-120">需求</span><span class="sxs-lookup"><span data-stu-id="9c975-120">Requirement</span></span> | <span data-ttu-id="9c975-121">值</span><span class="sxs-lookup"><span data-stu-id="9c975-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9c975-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c975-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9c975-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c975-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9c975-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c975-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9c975-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c975-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9c975-126">標頭</span><span class="sxs-lookup"><span data-stu-id="9c975-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c975-127"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="9c975-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c975-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c975-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c975-129">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="9c975-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="9c975-130">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="9c975-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





