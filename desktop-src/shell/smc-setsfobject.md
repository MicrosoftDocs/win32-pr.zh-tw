---
description: 通知您儲存傳遞的物件。
title: 'SMC_SETSFOBJECT 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f7e2cf12-7f09-45b0-97d3-eed803e57d9f
api_name:
- SMC_SETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 44aeb41ab7dcd271f8c84bff4eb8b5525ac66e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193568"
---
# <a name="smc_setsfobject-message"></a><span data-ttu-id="e71ee-103">SMC \_ SETSFOBJECT 訊息</span><span class="sxs-lookup"><span data-stu-id="e71ee-103">SMC\_SETSFOBJECT message</span></span>

<span data-ttu-id="e71ee-104">通知您儲存傳遞的物件。</span><span class="sxs-lookup"><span data-stu-id="e71ee-104">Notifies you to save the passed object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="e71ee-105">參數</span><span class="sxs-lookup"><span data-stu-id="e71ee-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e71ee-106">*Iid*</span><span class="sxs-lookup"><span data-stu-id="e71ee-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="e71ee-107">與物件相關聯的 IID。</span><span class="sxs-lookup"><span data-stu-id="e71ee-107">The IID associated with the object.</span></span>

</dd> <dt>

<span data-ttu-id="e71ee-108">*光伏*</span><span class="sxs-lookup"><span data-stu-id="e71ee-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="e71ee-109">由 *iid* 指定之物件上的介面指標。</span><span class="sxs-lookup"><span data-stu-id="e71ee-109">A pointer the interface on the object specified by *iid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e71ee-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e71ee-110">Return value</span></span>

<span data-ttu-id="e71ee-111">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="e71ee-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e71ee-112">備註</span><span class="sxs-lookup"><span data-stu-id="e71ee-112">Remarks</span></span>

<span data-ttu-id="e71ee-113">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="e71ee-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

<span data-ttu-id="e71ee-114">**SMC \_ SETSFOBJECT** 通知會搭配 IID 串流使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e71ee-114">The **SMC\_SETSFOBJECT** notification is used with IID\_Stream.</span></span> <span data-ttu-id="e71ee-115">物件會儲存在登錄中保存的表單中，而不會使用傳入之物件上的參考計數來完成任何動作。</span><span class="sxs-lookup"><span data-stu-id="e71ee-115">The object is saved into a persisted form in the registry and nothing is done with the reference count on the object passed in.</span></span>

## <a name="requirements"></a><span data-ttu-id="e71ee-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e71ee-116">Requirements</span></span>



| <span data-ttu-id="e71ee-117">需求</span><span class="sxs-lookup"><span data-stu-id="e71ee-117">Requirement</span></span> | <span data-ttu-id="e71ee-118">值</span><span class="sxs-lookup"><span data-stu-id="e71ee-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e71ee-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e71ee-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e71ee-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e71ee-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e71ee-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e71ee-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e71ee-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e71ee-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e71ee-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e71ee-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e71ee-124"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="e71ee-124"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="e71ee-125">Idl</span><span class="sxs-lookup"><span data-stu-id="e71ee-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e71ee-126"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e71ee-126"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




