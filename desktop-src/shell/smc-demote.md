---
description: 降級伴隨的 SMDATA 結構所指定的專案。
title: 'SMC_DEMOTE 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4809fbd1-da66-4453-b4f2-e75cb5b3457c
api_name:
- SMC_DEMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 46e5505571402feec24d81a9184b713e1c61ae0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991651"
---
# <a name="smc_demote-message"></a><span data-ttu-id="5dc20-103">SMC \_ 降級訊息</span><span class="sxs-lookup"><span data-stu-id="5dc20-103">SMC\_DEMOTE message</span></span>

<span data-ttu-id="5dc20-104">降級伴隨的 [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) 結構所指定的專案。</span><span class="sxs-lookup"><span data-stu-id="5dc20-104">Demote the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DEMOTE
            
```



## <a name="parameters"></a><span data-ttu-id="5dc20-105">參數</span><span class="sxs-lookup"><span data-stu-id="5dc20-105">Parameters</span></span>

<span data-ttu-id="5dc20-106">此訊息沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5dc20-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5dc20-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="5dc20-107">Return value</span></span>

<span data-ttu-id="5dc20-108">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="5dc20-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dc20-109">備註</span><span class="sxs-lookup"><span data-stu-id="5dc20-109">Remarks</span></span>

<span data-ttu-id="5dc20-110">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="5dc20-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dc20-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="5dc20-111">Requirements</span></span>



| <span data-ttu-id="5dc20-112">需求</span><span class="sxs-lookup"><span data-stu-id="5dc20-112">Requirement</span></span> | <span data-ttu-id="5dc20-113">值</span><span class="sxs-lookup"><span data-stu-id="5dc20-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dc20-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5dc20-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5dc20-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5dc20-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5dc20-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5dc20-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5dc20-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5dc20-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5dc20-118">標頭</span><span class="sxs-lookup"><span data-stu-id="5dc20-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dc20-119"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="5dc20-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="5dc20-120">Idl</span><span class="sxs-lookup"><span data-stu-id="5dc20-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5dc20-121"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5dc20-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




