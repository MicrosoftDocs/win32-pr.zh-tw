---
description: 使用者已按下箭號展開伴隨的 SMDATA 結構所指定的專案。
title: 'SMC_CHEVRONEXPAND 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cb0b3cf1-1a12-4236-96e9-cc04360d269f
api_name:
- SMC_CHEVRONEXPAND
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6ecf8f86e111326b3f37f3111c382d2d04ef2fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193574"
---
# <a name="smc_chevronexpand-message"></a><span data-ttu-id="203f4-103">SMC \_ CHEVRONEXPAND 訊息</span><span class="sxs-lookup"><span data-stu-id="203f4-103">SMC\_CHEVRONEXPAND message</span></span>

<span data-ttu-id="203f4-104">使用者已按下箭號展開伴隨的 [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) 結構所指定的專案。</span><span class="sxs-lookup"><span data-stu-id="203f4-104">The user has clicked a chevron to expand the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_CHEVRONEXPAND
            
```



## <a name="parameters"></a><span data-ttu-id="203f4-105">參數</span><span class="sxs-lookup"><span data-stu-id="203f4-105">Parameters</span></span>

<span data-ttu-id="203f4-106">此訊息沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="203f4-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="203f4-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="203f4-107">Return value</span></span>

<span data-ttu-id="203f4-108">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="203f4-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="203f4-109">備註</span><span class="sxs-lookup"><span data-stu-id="203f4-109">Remarks</span></span>

<span data-ttu-id="203f4-110">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="203f4-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="203f4-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="203f4-111">Requirements</span></span>



| <span data-ttu-id="203f4-112">需求</span><span class="sxs-lookup"><span data-stu-id="203f4-112">Requirement</span></span> | <span data-ttu-id="203f4-113">值</span><span class="sxs-lookup"><span data-stu-id="203f4-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="203f4-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="203f4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="203f4-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="203f4-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="203f4-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="203f4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="203f4-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="203f4-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="203f4-118">標頭</span><span class="sxs-lookup"><span data-stu-id="203f4-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="203f4-119"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="203f4-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="203f4-120">Idl</span><span class="sxs-lookup"><span data-stu-id="203f4-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="203f4-121"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="203f4-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




