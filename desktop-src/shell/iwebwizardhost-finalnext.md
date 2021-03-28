---
description: 流覽至裝載伺服器端 HTML 頁面的頁面下的用戶端 wizard 頁面，或者，如果沒有進一步的用戶端頁面，則完成 wizard。
title: 'WebWizardHost. FinalNext 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalNext
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 0699eb16-d6ef-46e3-bd02-d35512536275
ms.openlocfilehash: 5693de342b03a9ee4b7ed04cf24d8cfa9ee8b784
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193733"
---
# <a name="webwizardhostfinalnext-method"></a><span data-ttu-id="e0fb6-103">WebWizardHost. FinalNext 方法</span><span class="sxs-lookup"><span data-stu-id="e0fb6-103">WebWizardHost.FinalNext method</span></span>

<span data-ttu-id="e0fb6-104">流覽至裝載伺服器端 HTML 頁面的頁面下的用戶端 wizard 頁面，或者，如果沒有進一步的用戶端頁面，則完成 wizard。</span><span class="sxs-lookup"><span data-stu-id="e0fb6-104">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0fb6-105">語法</span><span class="sxs-lookup"><span data-stu-id="e0fb6-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a><span data-ttu-id="e0fb6-106">參數</span><span class="sxs-lookup"><span data-stu-id="e0fb6-106">Parameters</span></span>

<span data-ttu-id="e0fb6-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e0fb6-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0fb6-108">備註</span><span class="sxs-lookup"><span data-stu-id="e0fb6-108">Remarks</span></span>

<span data-ttu-id="e0fb6-109">當 wizard 顯示最後一個伺服器端 HTML 網頁，而且使用者按 **下 [下一步** **] 或 [完成]** 按鈕時，伺服器會在該按鈕的事件處理常式中叫用 **FinalNext** 。</span><span class="sxs-lookup"><span data-stu-id="e0fb6-109">When the wizard is displaying the last server-side HTML page and the user clicks the **Next** or **Finish** button, the server invokes **FinalNext** in that button's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0fb6-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0fb6-110">Requirements</span></span>



| <span data-ttu-id="e0fb6-111">需求</span><span class="sxs-lookup"><span data-stu-id="e0fb6-111">Requirement</span></span> | <span data-ttu-id="e0fb6-112">值</span><span class="sxs-lookup"><span data-stu-id="e0fb6-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0fb6-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0fb6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e0fb6-114">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0fb6-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e0fb6-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0fb6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e0fb6-116">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0fb6-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e0fb6-117">標頭</span><span class="sxs-lookup"><span data-stu-id="e0fb6-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0fb6-118"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e0fb6-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0fb6-119">Idl</span><span class="sxs-lookup"><span data-stu-id="e0fb6-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e0fb6-120"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e0fb6-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




