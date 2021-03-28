---
description: 升級隨附的 SMDATA 結構所指定的專案。
title: 'SMC_PROMOTE 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b1208673-06b4-42b2-b4ac-872fd22927df
api_name:
- SMC_PROMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 22718e51d6ef1bf7e3c5652741b95cadb4db9937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973448"
---
# <a name="smc_promote-message"></a><span data-ttu-id="c8121-103">SMC \_ 升階訊息</span><span class="sxs-lookup"><span data-stu-id="c8121-103">SMC\_PROMOTE message</span></span>

<span data-ttu-id="c8121-104">升級隨附的 [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) 結構所指定的專案。</span><span class="sxs-lookup"><span data-stu-id="c8121-104">Promote the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_PROMOTE
```



## <a name="parameters"></a><span data-ttu-id="c8121-105">參數</span><span class="sxs-lookup"><span data-stu-id="c8121-105">Parameters</span></span>

<span data-ttu-id="c8121-106">此訊息沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c8121-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8121-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8121-107">Return value</span></span>

<span data-ttu-id="c8121-108">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c8121-108">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8121-109">備註</span><span class="sxs-lookup"><span data-stu-id="c8121-109">Remarks</span></span>

<span data-ttu-id="c8121-110">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="c8121-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8121-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8121-111">Requirements</span></span>



| <span data-ttu-id="c8121-112">需求</span><span class="sxs-lookup"><span data-stu-id="c8121-112">Requirement</span></span> | <span data-ttu-id="c8121-113">值</span><span class="sxs-lookup"><span data-stu-id="c8121-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8121-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8121-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c8121-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8121-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c8121-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8121-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c8121-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8121-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c8121-118">標頭</span><span class="sxs-lookup"><span data-stu-id="c8121-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8121-119"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8121-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="c8121-120">Idl</span><span class="sxs-lookup"><span data-stu-id="c8121-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c8121-121"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c8121-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




