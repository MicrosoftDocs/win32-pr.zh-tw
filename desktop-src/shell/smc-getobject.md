---
description: 要求指定物件的指標。
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
ms.openlocfilehash: 5d0c0592356bff13e60c122b3c88cad05733e4f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991646"
---
# <a name="smc_getobject-message"></a><span data-ttu-id="733b9-103">SMC \_ GETOBJECT 訊息</span><span class="sxs-lookup"><span data-stu-id="733b9-103">SMC\_GETOBJECT message</span></span>

<span data-ttu-id="733b9-104">要求指定物件的指標。</span><span class="sxs-lookup"><span data-stu-id="733b9-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="733b9-105">參數</span><span class="sxs-lookup"><span data-stu-id="733b9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="733b9-106">*Iid*</span><span class="sxs-lookup"><span data-stu-id="733b9-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="733b9-107">與要求的物件相關聯的 IID。</span><span class="sxs-lookup"><span data-stu-id="733b9-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="733b9-108">*光伏*</span><span class="sxs-lookup"><span data-stu-id="733b9-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="733b9-109">將指標接收至所要求介面的 void 指標。</span><span class="sxs-lookup"><span data-stu-id="733b9-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="733b9-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="733b9-110">Return value</span></span>

<span data-ttu-id="733b9-111">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="733b9-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="733b9-112">備註</span><span class="sxs-lookup"><span data-stu-id="733b9-112">Remarks</span></span>

<span data-ttu-id="733b9-113">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="733b9-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="733b9-114">建立要求的物件，並將指標指派給所要求的介面，以做為 *pv*。</span><span class="sxs-lookup"><span data-stu-id="733b9-114">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="733b9-115">可能會要求下列介面。</span><span class="sxs-lookup"><span data-stu-id="733b9-115">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="733b9-116">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="733b9-116">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="733b9-117">**ICoNtextMenu**</span><span class="sxs-lookup"><span data-stu-id="733b9-117">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
-   [<span data-ttu-id="733b9-118">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="733b9-118">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)
-   [<span data-ttu-id="733b9-119">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="733b9-119">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

## <a name="requirements"></a><span data-ttu-id="733b9-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="733b9-120">Requirements</span></span>



| <span data-ttu-id="733b9-121">需求</span><span class="sxs-lookup"><span data-stu-id="733b9-121">Requirement</span></span> | <span data-ttu-id="733b9-122">值</span><span class="sxs-lookup"><span data-stu-id="733b9-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="733b9-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="733b9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="733b9-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="733b9-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="733b9-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="733b9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="733b9-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="733b9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="733b9-127">標頭</span><span class="sxs-lookup"><span data-stu-id="733b9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="733b9-128"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="733b9-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="733b9-129">Idl</span><span class="sxs-lookup"><span data-stu-id="733b9-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="733b9-130"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="733b9-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
