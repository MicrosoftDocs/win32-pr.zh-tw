---
title: 'TTN_LINKCLICK (Commctrl 的通知碼) '
description: 按一下氣球工具提示內的文字連結時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- TTN_LINKCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TTN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90be24910c2739b4495b651abf97156342d955b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995579"
---
# <a name="ttn_linkclick-notification-code"></a><span data-ttu-id="29344-105">TTN \_ LINKCLICK 通知碼</span><span class="sxs-lookup"><span data-stu-id="29344-105">TTN\_LINKCLICK notification code</span></span>

<span data-ttu-id="29344-106">按一下氣球工具提示內的文字連結時傳送。</span><span class="sxs-lookup"><span data-stu-id="29344-106">Sent when a text link inside a balloon tooltip is clicked.</span></span> <span data-ttu-id="29344-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="29344-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a><span data-ttu-id="29344-108">參數</span><span class="sxs-lookup"><span data-stu-id="29344-108">Parameters</span></span>

<span data-ttu-id="29344-109">此通知碼沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="29344-109">This notification code has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="29344-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="29344-110">Return value</span></span>

<span data-ttu-id="29344-111">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="29344-111">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="29344-112">備註</span><span class="sxs-lookup"><span data-stu-id="29344-112">Remarks</span></span>

<span data-ttu-id="29344-113">以下是傳送此通知的範例。</span><span class="sxs-lookup"><span data-stu-id="29344-113">Following is an example of when this notification is sent.</span></span> <span data-ttu-id="29344-114">假設您的氣球工具提示包含下列文字：「這是 <A>連結</A>」。</span><span class="sxs-lookup"><span data-stu-id="29344-114">Assume that your balloon tooltip contains the following text, "This is a <A>link</A>".</span></span> <span data-ttu-id="29344-115">按一下 [連結] 時，工具提示控制項會傳送 TTN \_ LINKCLICK 通知碼。</span><span class="sxs-lookup"><span data-stu-id="29344-115">When "link" is clicked, the tooltip control sends a TTN\_LINKCLICK notification code.</span></span>

> [!Note]  
> <span data-ttu-id="29344-116">若要使用此通知碼，您必須提供指定 Comclt32.dll 版本6.0 的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="29344-116">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="29344-117">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="29344-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="29344-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="29344-118">Requirements</span></span>



| <span data-ttu-id="29344-119">需求</span><span class="sxs-lookup"><span data-stu-id="29344-119">Requirement</span></span> | <span data-ttu-id="29344-120">值</span><span class="sxs-lookup"><span data-stu-id="29344-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29344-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29344-121">Minimum supported client</span></span><br/> | <span data-ttu-id="29344-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29344-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="29344-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29344-123">Minimum supported server</span></span><br/> | <span data-ttu-id="29344-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29344-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="29344-125">標頭</span><span class="sxs-lookup"><span data-stu-id="29344-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="29344-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="29344-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





