---
description: 傳送已完全重新整理功能表的通知，您可以重設您的狀態。
title: 'SMC_REFRESH 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8c79d9d5-b7dc-4271-9edb-93b40606c9be
api_name:
- SMC_REFRESH
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aab18245c6502d4d3424e6ed6727eceb5a329d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850423"
---
# <a name="smc_refresh-message"></a><span data-ttu-id="e215c-103">SMC \_ REFRESH 訊息</span><span class="sxs-lookup"><span data-stu-id="e215c-103">SMC\_REFRESH message</span></span>

<span data-ttu-id="e215c-104">傳送已完全重新整理功能表的通知，您可以重設您的狀態。</span><span class="sxs-lookup"><span data-stu-id="e215c-104">Sends notification that the menus have completely refreshed and you can reset your state.</span></span>


```C++
SMC_REFRESH
            
```



## <a name="parameters"></a><span data-ttu-id="e215c-105">參數</span><span class="sxs-lookup"><span data-stu-id="e215c-105">Parameters</span></span>

<span data-ttu-id="e215c-106">此訊息沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e215c-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e215c-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="e215c-107">Return value</span></span>

<span data-ttu-id="e215c-108">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="e215c-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e215c-109">備註</span><span class="sxs-lookup"><span data-stu-id="e215c-109">Remarks</span></span>

<span data-ttu-id="e215c-110">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="e215c-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e215c-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e215c-111">Requirements</span></span>



| <span data-ttu-id="e215c-112">需求</span><span class="sxs-lookup"><span data-stu-id="e215c-112">Requirement</span></span> | <span data-ttu-id="e215c-113">值</span><span class="sxs-lookup"><span data-stu-id="e215c-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e215c-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e215c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e215c-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e215c-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e215c-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e215c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e215c-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e215c-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e215c-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e215c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e215c-119"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="e215c-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="e215c-120">Idl</span><span class="sxs-lookup"><span data-stu-id="e215c-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e215c-121"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e215c-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




