---
title: 'WS_SECURITY_CONTEXT (WebServices) '
description: 用來參考安全性內容物件的不透明類型。
ms.assetid: 8d23357b-bff8-45fe-80ef-df3f3b0edde1
keywords:
- WS_SECURITY_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c041307eadd1ebcea379f9de0880fc011bd137ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104238"
---
# <a name="ws_security_context"></a><span data-ttu-id="5a9ab-104">WS \_ 安全性 \_ 內容</span><span class="sxs-lookup"><span data-stu-id="5a9ab-104">WS\_SECURITY\_CONTEXT</span></span>

<span data-ttu-id="5a9ab-105">用來參考 [安全性內容物件](security-context.md)的不透明類型。</span><span class="sxs-lookup"><span data-stu-id="5a9ab-105">An opaque type used to reference a [security context object](security-context.md).</span></span>


```C++
typedef struct _WS_SECURITY_CONTEXT WS_SECURITY_CONTEXT;
```



## <a name="remarks"></a><span data-ttu-id="5a9ab-106">備註</span><span class="sxs-lookup"><span data-stu-id="5a9ab-106">Remarks</span></span>

<span data-ttu-id="5a9ab-107">此物件不是安全線程。</span><span class="sxs-lookup"><span data-stu-id="5a9ab-107">This object is not thread safe.</span></span> <span data-ttu-id="5a9ab-108">如需詳細資訊，請參閱 [執行緒安全性](thread-safety.md)。</span><span class="sxs-lookup"><span data-stu-id="5a9ab-108">For more information, see [thread safety](thread-safety.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a9ab-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a9ab-109">Requirements</span></span>



| <span data-ttu-id="5a9ab-110">需求</span><span class="sxs-lookup"><span data-stu-id="5a9ab-110">Requirement</span></span> | <span data-ttu-id="5a9ab-111">值</span><span class="sxs-lookup"><span data-stu-id="5a9ab-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a9ab-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a9ab-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5a9ab-113">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a9ab-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="5a9ab-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a9ab-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5a9ab-115">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a9ab-115">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5a9ab-116">標頭</span><span class="sxs-lookup"><span data-stu-id="5a9ab-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a9ab-117"><dt>WebServices。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a9ab-117"><dt>WebServices.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a9ab-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a9ab-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a9ab-119">安全性內容</span><span class="sxs-lookup"><span data-stu-id="5a9ab-119">Security Context</span></span>](security-context.md)
</dt> <dt>

[<span data-ttu-id="5a9ab-120">執行緒安全性</span><span class="sxs-lookup"><span data-stu-id="5a9ab-120">Thread Safety</span></span>](thread-safety.md)
</dt> </dl>

 

 





