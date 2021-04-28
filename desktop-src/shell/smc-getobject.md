---
description: SMC_GETOBJECT 訊息-要求指定物件的指標。
title: 'SMC_GETOBJECT 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36e8f304-a92a-485f-8413-b9c416087ec9
api_name:
- SMC_GETOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58741290d741cc18fd788282d0f302ef87bb15dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100436"
---
# <a name="smc_getobject-message"></a><span data-ttu-id="f114f-103">SMC \_ GETOBJECT 訊息</span><span class="sxs-lookup"><span data-stu-id="f114f-103">SMC\_GETOBJECT message</span></span>

<span data-ttu-id="f114f-104">要求指定物件的指標。</span><span class="sxs-lookup"><span data-stu-id="f114f-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="f114f-105">參數</span><span class="sxs-lookup"><span data-stu-id="f114f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f114f-106">*Iid*</span><span class="sxs-lookup"><span data-stu-id="f114f-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="f114f-107">與要求的物件相關聯的 IID。</span><span class="sxs-lookup"><span data-stu-id="f114f-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="f114f-108">*光伏*</span><span class="sxs-lookup"><span data-stu-id="f114f-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="f114f-109">將指標接收至所要求介面的 void 指標。</span><span class="sxs-lookup"><span data-stu-id="f114f-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f114f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f114f-110">Return value</span></span>

<span data-ttu-id="f114f-111">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="f114f-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f114f-112">備註</span><span class="sxs-lookup"><span data-stu-id="f114f-112">Remarks</span></span>

<span data-ttu-id="f114f-113">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="f114f-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="f114f-114">建立要求的物件，並將指標指派給所要求的介面，以做為 *pv*。</span><span class="sxs-lookup"><span data-stu-id="f114f-114">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="f114f-115">可能會要求下列介面。</span><span class="sxs-lookup"><span data-stu-id="f114f-115">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="f114f-116">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="f114f-116">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="f114f-117">**ICoNtextMenu**</span><span class="sxs-lookup"><span data-stu-id="f114f-117">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
-   [<span data-ttu-id="f114f-118">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="f114f-118">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)
-   [<span data-ttu-id="f114f-119">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="f114f-119">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

## <a name="requirements"></a><span data-ttu-id="f114f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f114f-120">Requirements</span></span>



| <span data-ttu-id="f114f-121">需求</span><span class="sxs-lookup"><span data-stu-id="f114f-121">Requirement</span></span> | <span data-ttu-id="f114f-122">值</span><span class="sxs-lookup"><span data-stu-id="f114f-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f114f-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f114f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f114f-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f114f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f114f-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f114f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f114f-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f114f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f114f-127">標頭</span><span class="sxs-lookup"><span data-stu-id="f114f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f114f-128"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="f114f-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="f114f-129">Idl</span><span class="sxs-lookup"><span data-stu-id="f114f-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f114f-130"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f114f-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
