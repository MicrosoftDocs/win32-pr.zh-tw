---
title: 'EM_GETAUTOURLDETECT 訊息 (Richedit .h) '
description: 指出是否已在 rich edit 控制項中開啟自動 URL 偵測。
ms.assetid: f723f15c-bf8f-41ab-aef0-bd8f2c0b9e5d
keywords:
- EM_GETAUTOURLDETECT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETAUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e68e4f2991c5f8780cb587594289674e07ec992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025181"
---
# <a name="em_getautourldetect-message"></a><span data-ttu-id="11bf9-104">EM \_ GETAUTOURLDETECT 訊息</span><span class="sxs-lookup"><span data-stu-id="11bf9-104">EM\_GETAUTOURLDETECT message</span></span>

<span data-ttu-id="11bf9-105">指出是否已在 rich edit 控制項中開啟自動 URL 偵測。</span><span class="sxs-lookup"><span data-stu-id="11bf9-105">Indicates whether the auto URL detection is turned on in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="11bf9-106">參數</span><span class="sxs-lookup"><span data-stu-id="11bf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11bf9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="11bf9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11bf9-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="11bf9-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="11bf9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11bf9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11bf9-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="11bf9-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11bf9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="11bf9-111">Return value</span></span>

<span data-ttu-id="11bf9-112">如果自動 URL 偵測為使用中，則傳回值為1。</span><span class="sxs-lookup"><span data-stu-id="11bf9-112">If auto-URL detection is active, the return value is 1.</span></span>

<span data-ttu-id="11bf9-113">如果自動 URL 偵測為非使用中，則傳回值為0。</span><span class="sxs-lookup"><span data-stu-id="11bf9-113">If auto-URL detection is inactive, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="11bf9-114">備註</span><span class="sxs-lookup"><span data-stu-id="11bf9-114">Remarks</span></span>

<span data-ttu-id="11bf9-115">開啟自動 URL 偵測時，Microsoft Rich Edit 會持續檢查輸入的文字是否有有效的 URL。</span><span class="sxs-lookup"><span data-stu-id="11bf9-115">When auto URL detection is on, Microsoft Rich Edit is constantly checking typed text for a valid URL.</span></span> <span data-ttu-id="11bf9-116">Rich Edit 可辨識以這些首碼開頭的 Url：</span><span class="sxs-lookup"><span data-stu-id="11bf9-116">Rich Edit recognizes URLs that start with these prefixes:</span></span>

-   <span data-ttu-id="11bf9-117">http:</span><span class="sxs-lookup"><span data-stu-id="11bf9-117">http:</span></span>
-   <span data-ttu-id="11bf9-118">file：</span><span class="sxs-lookup"><span data-stu-id="11bf9-118">file:</span></span>
-   <span data-ttu-id="11bf9-119">mailto:</span><span class="sxs-lookup"><span data-stu-id="11bf9-119">mailto:</span></span>
-   <span data-ttu-id="11bf9-120">Ftp：</span><span class="sxs-lookup"><span data-stu-id="11bf9-120">ftp:</span></span>
-   <span data-ttu-id="11bf9-121">ip-HTTPs</span><span class="sxs-lookup"><span data-stu-id="11bf9-121">https:</span></span>
-   <span data-ttu-id="11bf9-122">開頭</span><span class="sxs-lookup"><span data-stu-id="11bf9-122">gopher:</span></span>
-   <span data-ttu-id="11bf9-123">nntp</span><span class="sxs-lookup"><span data-stu-id="11bf9-123">nntp:</span></span>
-   <span data-ttu-id="11bf9-124">普洛斯彼羅：</span><span class="sxs-lookup"><span data-stu-id="11bf9-124">prospero:</span></span>
-   <span data-ttu-id="11bf9-125">Telnet：</span><span class="sxs-lookup"><span data-stu-id="11bf9-125">telnet:</span></span>
-   <span data-ttu-id="11bf9-126">新聞：</span><span class="sxs-lookup"><span data-stu-id="11bf9-126">news:</span></span>
-   <span data-ttu-id="11bf9-127">wais</span><span class="sxs-lookup"><span data-stu-id="11bf9-127">wais:</span></span>
-   <span data-ttu-id="11bf9-128">前景：</span><span class="sxs-lookup"><span data-stu-id="11bf9-128">outlook:</span></span>

<span data-ttu-id="11bf9-129">Rich Edit 也可辨識開頭為的標準路徑名稱 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="11bf9-129">Rich Edit also recognizes standard path names that start with \\\\.</span></span> <span data-ttu-id="11bf9-130">當 Rich Edit 找出 URL 時，它會變更 URL 文字色彩、將文字加上底線，並使用 [En-us \_ 連結](en-link.md)通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="11bf9-130">When Rich Edit locates a URL, it changes the URL text color, underlines the text, and notifies the client using [EN\_LINK](en-link.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11bf9-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="11bf9-131">Requirements</span></span>



| <span data-ttu-id="11bf9-132">需求</span><span class="sxs-lookup"><span data-stu-id="11bf9-132">Requirement</span></span> | <span data-ttu-id="11bf9-133">值</span><span class="sxs-lookup"><span data-stu-id="11bf9-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11bf9-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11bf9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="11bf9-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11bf9-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="11bf9-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11bf9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="11bf9-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11bf9-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11bf9-138">標頭</span><span class="sxs-lookup"><span data-stu-id="11bf9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="11bf9-139"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="11bf9-139"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11bf9-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11bf9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11bf9-141">EN \_ 連結</span><span class="sxs-lookup"><span data-stu-id="11bf9-141">EN\_LINK</span></span>](en-link.md)
</dt> </dl>

 

 





