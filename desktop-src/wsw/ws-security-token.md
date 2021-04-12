---
title: 'WS_SECURITY_TOKEN (WebServices) '
description: 代表安全性權杖的不透明控制碼。
ms.assetid: 050a2ce5-279e-48fb-85da-1d0b11cd8229
keywords:
- WS_SECURITY_TOKEN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52e69a46f206f1def7cc2e7e2d03c2e5f1369f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465729"
---
# <a name="ws_security_token"></a><span data-ttu-id="91f87-104">WS \_ 安全性 \_ 權杖</span><span class="sxs-lookup"><span data-stu-id="91f87-104">WS\_SECURITY\_TOKEN</span></span>

<span data-ttu-id="91f87-105">代表 [安全性權杖](security-processing-results.md)的不透明控制碼。</span><span class="sxs-lookup"><span data-stu-id="91f87-105">The opaque handle representing a [security token](security-processing-results.md).</span></span>


```C++
typedef struct _WS_SECURITY_TOKEN WS_SECURITY_TOKEN;
```



## <a name="remarks"></a><span data-ttu-id="91f87-106">備註</span><span class="sxs-lookup"><span data-stu-id="91f87-106">Remarks</span></span>

<span data-ttu-id="91f87-107">此物件不是安全線程。</span><span class="sxs-lookup"><span data-stu-id="91f87-107">This object is not thread safe.</span></span> <span data-ttu-id="91f87-108">如需詳細資訊，請參閱 [執行緒安全性](thread-safety.md)。</span><span class="sxs-lookup"><span data-stu-id="91f87-108">For more information, see [thread safety](thread-safety.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91f87-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="91f87-109">Requirements</span></span>



| <span data-ttu-id="91f87-110">需求</span><span class="sxs-lookup"><span data-stu-id="91f87-110">Requirement</span></span> | <span data-ttu-id="91f87-111">值</span><span class="sxs-lookup"><span data-stu-id="91f87-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="91f87-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91f87-112">Minimum supported client</span></span><br/> | <span data-ttu-id="91f87-113">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91f87-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="91f87-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91f87-114">Minimum supported server</span></span><br/> | <span data-ttu-id="91f87-115">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91f87-115">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="91f87-116">標頭</span><span class="sxs-lookup"><span data-stu-id="91f87-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="91f87-117"><dt>WebServices。h</dt></span><span class="sxs-lookup"><span data-stu-id="91f87-117"><dt>WebServices.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91f87-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91f87-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91f87-119">安全性處理結果</span><span class="sxs-lookup"><span data-stu-id="91f87-119">Security Processing Results</span></span>](security-processing-results.md)
</dt> <dt>

[<span data-ttu-id="91f87-120">執行緒安全性</span><span class="sxs-lookup"><span data-stu-id="91f87-120">Thread Safety</span></span>](thread-safety.md)
</dt> </dl>

 

 





