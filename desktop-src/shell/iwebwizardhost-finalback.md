---
description: 在主控伺服器端 HTML 頁面的頁面上，直接流覽至用戶端頁面。
title: 'WebWizardHost. FinalBack 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalBack
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: a0616388-cf94-4433-ae52-24f02f1d15ac
ms.openlocfilehash: 704efbd4aae5a98ec01d8bd900e226144d25833d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849724"
---
# <a name="webwizardhostfinalback-method"></a><span data-ttu-id="f185f-103">WebWizardHost. FinalBack 方法</span><span class="sxs-lookup"><span data-stu-id="f185f-103">WebWizardHost.FinalBack method</span></span>

<span data-ttu-id="f185f-104">在主控伺服器端 HTML 頁面的頁面上，直接流覽至用戶端頁面。</span><span class="sxs-lookup"><span data-stu-id="f185f-104">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="f185f-105">語法</span><span class="sxs-lookup"><span data-stu-id="f185f-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a><span data-ttu-id="f185f-106">參數</span><span class="sxs-lookup"><span data-stu-id="f185f-106">Parameters</span></span>

<span data-ttu-id="f185f-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f185f-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f185f-108">備註</span><span class="sxs-lookup"><span data-stu-id="f185f-108">Remarks</span></span>

<span data-ttu-id="f185f-109">當 wizard 顯示第一個伺服器端頁面，而且使用者按下 [ **上一步** ] 按鈕時，伺服器會在用戶端的事件處理常式收到該事件的通知時叫用 **FinalBack** 。</span><span class="sxs-lookup"><span data-stu-id="f185f-109">When the wizard displays the first server-side page and the user clicks the **Back** button, the server invokes **FinalBack** when notified of that event by the client's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="f185f-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="f185f-110">Requirements</span></span>



| <span data-ttu-id="f185f-111">需求</span><span class="sxs-lookup"><span data-stu-id="f185f-111">Requirement</span></span> | <span data-ttu-id="f185f-112">值</span><span class="sxs-lookup"><span data-stu-id="f185f-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f185f-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f185f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f185f-114">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f185f-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f185f-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f185f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f185f-116">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f185f-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f185f-117">標頭</span><span class="sxs-lookup"><span data-stu-id="f185f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f185f-118"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f185f-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f185f-119">Idl</span><span class="sxs-lookup"><span data-stu-id="f185f-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f185f-120"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f185f-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




