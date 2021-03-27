---
description: 通知您功能表已折迭。
title: 'SMC_EXITMENU 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 868b4819-1dbf-497a-9c79-5935f503969a
api_name:
- SMC_EXITMENU
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9a8680617a17ce0069a8633e1c70ff6b32a4be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944580"
---
# <a name="smc_exitmenu-message"></a><span data-ttu-id="b3786-103">SMC \_ EXITMENU 訊息</span><span class="sxs-lookup"><span data-stu-id="b3786-103">SMC\_EXITMENU message</span></span>

<span data-ttu-id="b3786-104">通知您功能表已折迭。</span><span class="sxs-lookup"><span data-stu-id="b3786-104">Notifies you that the menu is collapsing.</span></span>


```C++
SMC_EXITMENU
            
```



## <a name="parameters"></a><span data-ttu-id="b3786-105">參數</span><span class="sxs-lookup"><span data-stu-id="b3786-105">Parameters</span></span>

<span data-ttu-id="b3786-106">此訊息沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b3786-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3786-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3786-107">Return value</span></span>

<span data-ttu-id="b3786-108">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="b3786-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3786-109">備註</span><span class="sxs-lookup"><span data-stu-id="b3786-109">Remarks</span></span>

<span data-ttu-id="b3786-110">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="b3786-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3786-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3786-111">Requirements</span></span>



| <span data-ttu-id="b3786-112">需求</span><span class="sxs-lookup"><span data-stu-id="b3786-112">Requirement</span></span> | <span data-ttu-id="b3786-113">值</span><span class="sxs-lookup"><span data-stu-id="b3786-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3786-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3786-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b3786-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3786-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b3786-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3786-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b3786-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3786-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3786-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b3786-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3786-119"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="b3786-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3786-120">Idl</span><span class="sxs-lookup"><span data-stu-id="b3786-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3786-121"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3786-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




