---
description: SMC_GETSFOBJECT 訊息-要求指定物件的指標。
title: 'SMC_GETSFOBJECT 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a8478f10-77ce-4e71-a5dc-89d8a90cf513
api_name:
- SMC_GETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 612b43c193cd1919db4a5cf9dba3a8fdba1c81c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086606"
---
# <a name="smc_getsfobject-message"></a><span data-ttu-id="98ab8-103">SMC \_ GETSFOBJECT 訊息</span><span class="sxs-lookup"><span data-stu-id="98ab8-103">SMC\_GETSFOBJECT message</span></span>

<span data-ttu-id="98ab8-104">要求指定物件的指標。</span><span class="sxs-lookup"><span data-stu-id="98ab8-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETSFOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="98ab8-105">參數</span><span class="sxs-lookup"><span data-stu-id="98ab8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98ab8-106">*Iid*</span><span class="sxs-lookup"><span data-stu-id="98ab8-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="98ab8-107">與要求的物件相關聯的 IID。</span><span class="sxs-lookup"><span data-stu-id="98ab8-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="98ab8-108">*光伏*</span><span class="sxs-lookup"><span data-stu-id="98ab8-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="98ab8-109">將指標接收至所要求介面的 void 指標。</span><span class="sxs-lookup"><span data-stu-id="98ab8-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98ab8-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="98ab8-110">Return value</span></span>

<span data-ttu-id="98ab8-111">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="98ab8-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="98ab8-112">備註</span><span class="sxs-lookup"><span data-stu-id="98ab8-112">Remarks</span></span>

<span data-ttu-id="98ab8-113">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="98ab8-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="98ab8-114">它類似于 [**SMC \_ GETOBJECT**](smc-getobject.md) ，但用於 Shell 資料夾專案。</span><span class="sxs-lookup"><span data-stu-id="98ab8-114">It is similar to [**SMC\_GETOBJECT**](smc-getobject.md) but used for Shell folder items.</span></span> <span data-ttu-id="98ab8-115">建立要求的物件，並將指標指派給所要求的介面，以做為 *pv*。</span><span class="sxs-lookup"><span data-stu-id="98ab8-115">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="98ab8-116">可能會要求下列介面。</span><span class="sxs-lookup"><span data-stu-id="98ab8-116">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="98ab8-117">**IStream**</span><span class="sxs-lookup"><span data-stu-id="98ab8-117">**IStream**</span></span>](/windows/win32/api/objidl/nn-objidl-istream)
-   [<span data-ttu-id="98ab8-118">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="98ab8-118">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="98ab8-119">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="98ab8-119">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a><span data-ttu-id="98ab8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="98ab8-120">Requirements</span></span>



| <span data-ttu-id="98ab8-121">需求</span><span class="sxs-lookup"><span data-stu-id="98ab8-121">Requirement</span></span> | <span data-ttu-id="98ab8-122">值</span><span class="sxs-lookup"><span data-stu-id="98ab8-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98ab8-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98ab8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="98ab8-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98ab8-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="98ab8-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98ab8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="98ab8-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98ab8-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="98ab8-127">標頭</span><span class="sxs-lookup"><span data-stu-id="98ab8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="98ab8-128"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="98ab8-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="98ab8-129">Idl</span><span class="sxs-lookup"><span data-stu-id="98ab8-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="98ab8-130"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="98ab8-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
