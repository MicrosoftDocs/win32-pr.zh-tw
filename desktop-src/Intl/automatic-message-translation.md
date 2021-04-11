---
description: 使用 Unicode 和字元集 API 函數的應用程式通常會使用相同的視窗類別。 作業系統會以透明的方式轉譯不同類別的視窗之間的訊息。
ms.assetid: 68e9839b-39f8-411a-8ae4-4a627c667cae
title: 自動訊息轉譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b02a5c5a4951189333608aa448f09ba9c6866d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690260"
---
# <a name="automatic-message-translation"></a><span data-ttu-id="2dc8d-104">自動訊息轉譯</span><span class="sxs-lookup"><span data-stu-id="2dc8d-104">Automatic Message Translation</span></span>

<span data-ttu-id="2dc8d-105">使用 Unicode 和字元集 API 函數的應用程式通常會使用相同的視窗類別。</span><span class="sxs-lookup"><span data-stu-id="2dc8d-105">Applications using the Unicode and character set API functions generally use the same window class.</span></span> <span data-ttu-id="2dc8d-106">作業系統會以透明的方式轉譯不同類別的視窗之間的訊息。</span><span class="sxs-lookup"><span data-stu-id="2dc8d-106">The operating system transparently translates messages between windows of different classes.</span></span>

<span data-ttu-id="2dc8d-107">執行的視窗函式會以 Unicode 或 Windows 字碼頁格式接收訊息。</span><span class="sxs-lookup"><span data-stu-id="2dc8d-107">A window function is implemented to receive messages in Unicode or Windows code page format.</span></span> <span data-ttu-id="2dc8d-108">視窗函數可以傳送訊息或呼叫任一個類型的函式。</span><span class="sxs-lookup"><span data-stu-id="2dc8d-108">The window function can send messages or call functions of either type.</span></span>

<span data-ttu-id="2dc8d-109">下列訊息有文字引數，且受限於自動文字翻譯。</span><span class="sxs-lookup"><span data-stu-id="2dc8d-109">The following messages have text arguments and are subject to automatic text translation.</span></span> <span data-ttu-id="2dc8d-110">如需自動轉譯的詳細資訊，請參閱子類別化 [和自動訊息轉譯](subclassing-and-automatic-message-translation.md)。</span><span class="sxs-lookup"><span data-stu-id="2dc8d-110">For information about automatic translation, see [Subclassing and Automatic Message Translation](subclassing-and-automatic-message-translation.md).</span></span>

<dl>

[<span data-ttu-id="2dc8d-111">CB \_ ADDSTRING</span><span class="sxs-lookup"><span data-stu-id="2dc8d-111">CB\_ADDSTRING</span></span>](../controls/cb-addstring.md)  
[<span data-ttu-id="2dc8d-112">CB \_ 目錄</span><span class="sxs-lookup"><span data-stu-id="2dc8d-112">CB\_DIR</span></span>](../controls/cb-dir.md)  
[<span data-ttu-id="2dc8d-113">CB \_ FINDSTRING</span><span class="sxs-lookup"><span data-stu-id="2dc8d-113">CB\_FINDSTRING</span></span>](../controls/cb-findstring.md)  
[<span data-ttu-id="2dc8d-114">CB \_ GETLBTEXT</span><span class="sxs-lookup"><span data-stu-id="2dc8d-114">CB\_GETLBTEXT</span></span>](../controls/cb-getlbtext.md)  
[<span data-ttu-id="2dc8d-115">CB \_ INSERTSTRING</span><span class="sxs-lookup"><span data-stu-id="2dc8d-115">CB\_INSERTSTRING</span></span>](../controls/cb-insertstring.md)  
[<span data-ttu-id="2dc8d-116">CB \_ SELECTSTRING</span><span class="sxs-lookup"><span data-stu-id="2dc8d-116">CB\_SELECTSTRING</span></span>](../controls/cb-selectstring.md)  
[<span data-ttu-id="2dc8d-117">EM \_ GETLINE</span><span class="sxs-lookup"><span data-stu-id="2dc8d-117">EM\_GETLINE</span></span>](../controls/em-getline.md)  
[<span data-ttu-id="2dc8d-118">EM \_ REPLACESEL</span><span class="sxs-lookup"><span data-stu-id="2dc8d-118">EM\_REPLACESEL</span></span>](../controls/em-replacesel.md)  
[<span data-ttu-id="2dc8d-119">EM \_ SETPASSWORDCHAR</span><span class="sxs-lookup"><span data-stu-id="2dc8d-119">EM\_SETPASSWORDCHAR</span></span>](../controls/em-setpasswordchar.md)  
[<span data-ttu-id="2dc8d-120">LB \_ ADDFILE</span><span class="sxs-lookup"><span data-stu-id="2dc8d-120">LB\_ADDFILE</span></span>](../controls/lb-addfile.md)  
[<span data-ttu-id="2dc8d-121">LB \_ ADDSTRING</span><span class="sxs-lookup"><span data-stu-id="2dc8d-121">LB\_ADDSTRING</span></span>](../controls/lb-addstring.md)  
[<span data-ttu-id="2dc8d-122">LB \_ 目錄</span><span class="sxs-lookup"><span data-stu-id="2dc8d-122">LB\_DIR</span></span>](../controls/lb-dir.md)  
[<span data-ttu-id="2dc8d-123">LB \_ FINDSTRING</span><span class="sxs-lookup"><span data-stu-id="2dc8d-123">LB\_FINDSTRING</span></span>](../controls/lb-findstring.md)  
[<span data-ttu-id="2dc8d-124">LB \_ GETTEXT</span><span class="sxs-lookup"><span data-stu-id="2dc8d-124">LB\_GETTEXT</span></span>](../controls/lb-gettext.md)  
[<span data-ttu-id="2dc8d-125">LB \_ INSERTSTRING</span><span class="sxs-lookup"><span data-stu-id="2dc8d-125">LB\_INSERTSTRING</span></span>](../controls/lb-insertstring.md)  
[<span data-ttu-id="2dc8d-126">LB \_ SELECTSTRING</span><span class="sxs-lookup"><span data-stu-id="2dc8d-126">LB\_SELECTSTRING</span></span>](../controls/lb-selectstring.md)  
[<span data-ttu-id="2dc8d-127">WM \_ ASKCBFORMATNAME</span><span class="sxs-lookup"><span data-stu-id="2dc8d-127">WM\_ASKCBFORMATNAME</span></span>](../dataxchg/wm-askcbformatname.md)  
[<span data-ttu-id="2dc8d-128">WM \_ 字元</span><span class="sxs-lookup"><span data-stu-id="2dc8d-128">WM\_CHAR</span></span>](../inputdev/wm-char.md)  
[<span data-ttu-id="2dc8d-129">WM \_ CHARTOITEM</span><span class="sxs-lookup"><span data-stu-id="2dc8d-129">WM\_CHARTOITEM</span></span>](../controls/wm-chartoitem.md)  
[<span data-ttu-id="2dc8d-130">WM \_ 建立</span><span class="sxs-lookup"><span data-stu-id="2dc8d-130">WM\_CREATE</span></span>](../winmsg/wm-create.md)  
[<span data-ttu-id="2dc8d-131">WM \_ DEADCHAR</span><span class="sxs-lookup"><span data-stu-id="2dc8d-131">WM\_DEADCHAR</span></span>](../inputdev/wm-deadchar.md)  
[<span data-ttu-id="2dc8d-132">WM \_ DEVMODECHANGE</span><span class="sxs-lookup"><span data-stu-id="2dc8d-132">WM\_DEVMODECHANGE</span></span>](../gdi/wm-devmodechange.md)  
[<span data-ttu-id="2dc8d-133">WM \_ GETTEXT</span><span class="sxs-lookup"><span data-stu-id="2dc8d-133">WM\_GETTEXT</span></span>](../winmsg/wm-gettext.md)  
[<span data-ttu-id="2dc8d-134">WM \_ MDICREATE</span><span class="sxs-lookup"><span data-stu-id="2dc8d-134">WM\_MDICREATE</span></span>](../winmsg/wm-mdicreate.md)  
[<span data-ttu-id="2dc8d-135">WM \_ MENUCHAR</span><span class="sxs-lookup"><span data-stu-id="2dc8d-135">WM\_MENUCHAR</span></span>](../menurc/wm-menuchar.md)  
[<span data-ttu-id="2dc8d-136">WM \_ NCCREATE</span><span class="sxs-lookup"><span data-stu-id="2dc8d-136">WM\_NCCREATE</span></span>](../winmsg/wm-nccreate.md)  
[<span data-ttu-id="2dc8d-137">WM \_ SETTEXT</span><span class="sxs-lookup"><span data-stu-id="2dc8d-137">WM\_SETTEXT</span></span>](../winmsg/wm-settext.md)  
[<span data-ttu-id="2dc8d-138">WM \_ SYSCHAR</span><span class="sxs-lookup"><span data-stu-id="2dc8d-138">WM\_SYSCHAR</span></span>](../menurc/wm-syschar.md)  
[<span data-ttu-id="2dc8d-139">WM \_ SYSDEADCHAR</span><span class="sxs-lookup"><span data-stu-id="2dc8d-139">WM\_SYSDEADCHAR</span></span>](../inputdev/wm-sysdeadchar.md)  
[<span data-ttu-id="2dc8d-140">WM \_ WININICHANGE</span><span class="sxs-lookup"><span data-stu-id="2dc8d-140">WM\_WININICHANGE</span></span>](../winmsg/wm-wininichange.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="2dc8d-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="2dc8d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dc8d-142">Windows API 中的 Unicode</span><span class="sxs-lookup"><span data-stu-id="2dc8d-142">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
