---
description: 使用者選取了伴隨的 SMDATA 結構所指定的專案。
title: 'SMC_SFSELECTITEM 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 82c3dfca-98a8-43ca-bebc-85bfdf640d38
api_name:
- SMC_SFSELECTITEM
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cfb3384fcfff73d264d21c53a91ede554cc7da5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973276"
---
# <a name="smc_sfselectitem-message"></a><span data-ttu-id="2b737-103">SMC \_ SFSELECTITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="2b737-103">SMC\_SFSELECTITEM message</span></span>

<span data-ttu-id="2b737-104">使用者選取了伴隨的 [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) 結構所指定的專案。</span><span class="sxs-lookup"><span data-stu-id="2b737-104">The user has selected the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFSELECTITEM
            
```



## <a name="parameters"></a><span data-ttu-id="2b737-105">參數</span><span class="sxs-lookup"><span data-stu-id="2b737-105">Parameters</span></span>

<span data-ttu-id="2b737-106">此訊息沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2b737-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b737-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b737-107">Return value</span></span>

<span data-ttu-id="2b737-108">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="2b737-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b737-109">備註</span><span class="sxs-lookup"><span data-stu-id="2b737-109">Remarks</span></span>

<span data-ttu-id="2b737-110">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="2b737-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b737-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b737-111">Requirements</span></span>



| <span data-ttu-id="2b737-112">需求</span><span class="sxs-lookup"><span data-stu-id="2b737-112">Requirement</span></span> | <span data-ttu-id="2b737-113">值</span><span class="sxs-lookup"><span data-stu-id="2b737-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b737-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b737-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2b737-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b737-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2b737-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b737-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2b737-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b737-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b737-118">標頭</span><span class="sxs-lookup"><span data-stu-id="2b737-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b737-119"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b737-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b737-120">Idl</span><span class="sxs-lookup"><span data-stu-id="2b737-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2b737-121"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2b737-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




