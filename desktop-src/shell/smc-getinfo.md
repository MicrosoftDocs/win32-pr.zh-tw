---
description: 要求一般功能表項目的相關資訊。
title: 'SMC_GETINFO 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07f35a64-eff0-48e8-a2fc-719ccf1eca18
api_name:
- SMC_GETINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f60c1581ae7c4585de48eea943cc23b4d87fa4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991643"
---
# <a name="smc_getinfo-message"></a><span data-ttu-id="f710a-103">SMC \_ GETINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="f710a-103">SMC\_GETINFO message</span></span>

<span data-ttu-id="f710a-104">要求一般功能表項目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f710a-104">Requests information about a regular menu item.</span></span>


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a><span data-ttu-id="f710a-105">參數</span><span class="sxs-lookup"><span data-stu-id="f710a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f710a-106">*psminfo*</span><span class="sxs-lookup"><span data-stu-id="f710a-106">*psminfo*</span></span> 
</dt> <dd>

<span data-ttu-id="f710a-107">[**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f710a-107">A pointer to a [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) structure.</span></span> <span data-ttu-id="f710a-108">使用適當的資訊填入結構，並傳回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="f710a-108">Fill the structure with the appropriate information and return S\_OK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f710a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f710a-109">Return value</span></span>

<span data-ttu-id="f710a-110">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="f710a-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f710a-111">備註</span><span class="sxs-lookup"><span data-stu-id="f710a-111">Remarks</span></span>

<span data-ttu-id="f710a-112">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="f710a-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f710a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f710a-113">Requirements</span></span>



| <span data-ttu-id="f710a-114">需求</span><span class="sxs-lookup"><span data-stu-id="f710a-114">Requirement</span></span> | <span data-ttu-id="f710a-115">值</span><span class="sxs-lookup"><span data-stu-id="f710a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f710a-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f710a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f710a-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f710a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f710a-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f710a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f710a-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f710a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f710a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="f710a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f710a-121"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="f710a-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="f710a-122">Idl</span><span class="sxs-lookup"><span data-stu-id="f710a-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f710a-123"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f710a-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




