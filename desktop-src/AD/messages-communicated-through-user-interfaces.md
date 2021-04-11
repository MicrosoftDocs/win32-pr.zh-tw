---
title: 透過使用者介面傳達的訊息
description: 本主題列出目錄服務可從使用者介面傳送的訊息。
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- 透過使用者介面傳達的訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab0d01717129db284f05b2361b2a067d611a33e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020842"
---
# <a name="messages-communicated-through-user-interfaces"></a><span data-ttu-id="6c445-104">透過使用者介面傳達的訊息</span><span class="sxs-lookup"><span data-stu-id="6c445-104">Messages Communicated through User Interfaces</span></span>

<span data-ttu-id="6c445-105">本主題列出目錄服務可從使用者介面傳送的訊息。</span><span class="sxs-lookup"><span data-stu-id="6c445-105">This topic lists messages that a directory service can send from a user interface.</span></span>

## <a name="common-query-page-messages"></a><span data-ttu-id="6c445-106">一般查詢頁面訊息</span><span class="sxs-lookup"><span data-stu-id="6c445-106">Common Query Page Messages</span></span>

<span data-ttu-id="6c445-107">下列訊息會傳送至 [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) 回呼函數中的目錄服務查詢表單延伸頁面：</span><span class="sxs-lookup"><span data-stu-id="6c445-107">The following messages are sent to a directory service query form extension page in the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function:</span></span>

-   [<span data-ttu-id="6c445-108">**CQPM \_ CLEARFORM**</span><span class="sxs-lookup"><span data-stu-id="6c445-108">**CQPM\_CLEARFORM**</span></span>](cqpm-clearform.md)
-   [<span data-ttu-id="6c445-109">**CQPM \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="6c445-109">**CQPM\_ENABLE**</span></span>](cqpm-enable.md)
-   [<span data-ttu-id="6c445-110">**CQPM \_ GETPARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="6c445-110">**CQPM\_GETPARAMETERS**</span></span>](cqpm-getparameters.md)
-   [<span data-ttu-id="6c445-111">**CQPM \_ HANDLERSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="6c445-111">**CQPM\_HANDLERSPECIFIC**</span></span>](cqpm-handlerspecific.md)
-   [<span data-ttu-id="6c445-112">**CQPM \_ 說明**</span><span class="sxs-lookup"><span data-stu-id="6c445-112">**CQPM\_HELP**</span></span>](cqpm-help.md)
-   [<span data-ttu-id="6c445-113">**CQPM \_ INITIALIZE**</span><span class="sxs-lookup"><span data-stu-id="6c445-113">**CQPM\_INITIALIZE**</span></span>](cqpm-initialize.md)
-   [<span data-ttu-id="6c445-114">**CQPM \_ 保存**</span><span class="sxs-lookup"><span data-stu-id="6c445-114">**CQPM\_PERSIST**</span></span>](cqpm-persist.md)
-   [<span data-ttu-id="6c445-115">**CQPM \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="6c445-115">**CQPM\_RELEASE**</span></span>](cqpm-release.md)
-   [<span data-ttu-id="6c445-116">**CQPM \_ SETDEFAULTPARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="6c445-116">**CQPM\_SETDEFAULTPARAMETERS**</span></span>](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a><span data-ttu-id="6c445-117">其他訊息</span><span class="sxs-lookup"><span data-stu-id="6c445-117">Miscellaneous Messages</span></span>

<span data-ttu-id="6c445-118">下表列出目錄服務可傳送的訊息。</span><span class="sxs-lookup"><span data-stu-id="6c445-118">The following table lists messages that a directory service can send.</span></span>



| <span data-ttu-id="6c445-119">訊息</span><span class="sxs-lookup"><span data-stu-id="6c445-119">Message</span></span>                  | <span data-ttu-id="6c445-120">值</span><span class="sxs-lookup"><span data-stu-id="6c445-120">Value</span></span>                     | <span data-ttu-id="6c445-121">描述</span><span class="sxs-lookup"><span data-stu-id="6c445-121">Description</span></span>                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c445-122">DSPROP \_ ATTRCHANGED \_ MSG</span><span class="sxs-lookup"><span data-stu-id="6c445-122">DSPROP\_ATTRCHANGED\_MSG</span></span> | <span data-ttu-id="6c445-123">"DsPropAttrChanged"</span><span class="sxs-lookup"><span data-stu-id="6c445-123">"DsPropAttrChanged"</span></span>       | <span data-ttu-id="6c445-124">針對同步處理屬性頁和目錄服務管理工具所傳送的訊息，在 Dsclient 中宣告。</span><span class="sxs-lookup"><span data-stu-id="6c445-124">A message sent for synchronizing property pages and the directory service administration tools, declared in Dsclient.h.</span></span>                                                                                                                       |
| <span data-ttu-id="6c445-125">DSQPM \_ GETCLASSLIST</span><span class="sxs-lookup"><span data-stu-id="6c445-125">DSQPM\_GETCLASSLIST</span></span>      | <span data-ttu-id="6c445-126">CQPM \_ HANDLERSPECIFIC + 0</span><span class="sxs-lookup"><span data-stu-id="6c445-126">CQPM\_HANDLERSPECIFIC+0</span></span>   | <span data-ttu-id="6c445-127">傳送至表單頁面的頁面訊息，可供您用來取得查詢類別清單，供欄位選取器和屬性妥善建立，以建立其顯示類別清單。</span><span class="sxs-lookup"><span data-stu-id="6c445-127">A page message sent to the form pages for retrieving a list of classes for query, used by the field selector and property well to build its list of display classes.</span></span> <span data-ttu-id="6c445-128">wParam = flags 和 lParam = LPLPDSQUERYCLASSLIST，在 Dsquery. h 中宣告。</span><span class="sxs-lookup"><span data-stu-id="6c445-128">wParam = flags and lParam = LPLPDSQUERYCLASSLIST, declared in Dsquery.h.</span></span> |
| <span data-ttu-id="6c445-129">DSQPM \_ HELPTOPICS</span><span class="sxs-lookup"><span data-stu-id="6c445-129">DSQPM\_HELPTOPICS</span></span>        | <span data-ttu-id="6c445-130"> (CQPM \_ HANDLERSPECIFIC + 1) </span><span class="sxs-lookup"><span data-stu-id="6c445-130">(CQPM\_HANDLERSPECIFIC+1)</span></span> | <span data-ttu-id="6c445-131">傳送至表單頁面的頁面訊息，用來處理「說明主題」要求。</span><span class="sxs-lookup"><span data-stu-id="6c445-131">A page message sent to the form pages for handling the "Help Topics" request.</span></span> <span data-ttu-id="6c445-132">wParam = 0，lParam = hWndParent，在 Dsquery. h 中宣告。</span><span class="sxs-lookup"><span data-stu-id="6c445-132">wParam = 0, lParam = hWndParent, declared in Dsquery.h.</span></span>                                                                                                         |



 

 

 




