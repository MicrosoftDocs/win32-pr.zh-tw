---
description: 針對伴隨的 SMDATA 結構所指定的專案，要求有燕號提示的標題和文字。
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: 'SMC_CHEVRONGETTIP 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118056627d19990648e81b69aa355f3df99ec286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973460"
---
# <a name="smc_chevrongettip-message"></a><span data-ttu-id="ac2d3-103">SMC \_ CHEVRONGETTIP 訊息</span><span class="sxs-lookup"><span data-stu-id="ac2d3-103">SMC\_CHEVRONGETTIP message</span></span>

<span data-ttu-id="ac2d3-104">針對伴隨的 [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) 結構所指定的專案，要求有燕號提示的標題和文字。</span><span class="sxs-lookup"><span data-stu-id="ac2d3-104">Requests the title and text for a chevron infotip for the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a><span data-ttu-id="ac2d3-105">參數</span><span class="sxs-lookup"><span data-stu-id="ac2d3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac2d3-106">*pwszTipTitle*</span><span class="sxs-lookup"><span data-stu-id="ac2d3-106">*pwszTipTitle*</span></span> 
</dt> <dd>

<span data-ttu-id="ac2d3-107">緩衝區的指標，此緩衝區會接收以 **Null** 終止的 Unicode 字串，其中包含提示的標題。</span><span class="sxs-lookup"><span data-stu-id="ac2d3-107">A pointer to a buffer that receives a **NULL**-terminated Unicode string that contains the infotip's title.</span></span> <span data-ttu-id="ac2d3-108">這個字串的長度不能超過最大 \_ 路徑字元，包括結束的 **Null** 字元。</span><span class="sxs-lookup"><span data-stu-id="ac2d3-108">This string must be no longer than MAX\_PATH characters long, including the terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="ac2d3-109">*pwszTipText*</span><span class="sxs-lookup"><span data-stu-id="ac2d3-109">*pwszTipText*</span></span> 
</dt> <dd>

<span data-ttu-id="ac2d3-110">緩衝區的指標，此緩衝區會接收以 **Null** 終止的 Unicode 字串，其中包含內容提示的文字。</span><span class="sxs-lookup"><span data-stu-id="ac2d3-110">A pointer to a buffer that receives a **NULL**-terminated Unicode string that contains the infotip's text.</span></span> <span data-ttu-id="ac2d3-111">這個字串的長度不能超過最大 \_ 路徑字元，包括結束的 **Null** 字元。</span><span class="sxs-lookup"><span data-stu-id="ac2d3-111">This string must be no longer than MAX\_PATH characters long, including the terminating **NULL** character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac2d3-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac2d3-112">Return value</span></span>

<span data-ttu-id="ac2d3-113">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="ac2d3-113">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac2d3-114">備註</span><span class="sxs-lookup"><span data-stu-id="ac2d3-114">Remarks</span></span>

<span data-ttu-id="ac2d3-115">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="ac2d3-115">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac2d3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac2d3-116">Requirements</span></span>



| <span data-ttu-id="ac2d3-117">需求</span><span class="sxs-lookup"><span data-stu-id="ac2d3-117">Requirement</span></span> | <span data-ttu-id="ac2d3-118">值</span><span class="sxs-lookup"><span data-stu-id="ac2d3-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac2d3-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac2d3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ac2d3-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac2d3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ac2d3-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac2d3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ac2d3-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac2d3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ac2d3-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ac2d3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac2d3-124"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="ac2d3-124"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac2d3-125">Idl</span><span class="sxs-lookup"><span data-stu-id="ac2d3-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ac2d3-126"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ac2d3-126"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




