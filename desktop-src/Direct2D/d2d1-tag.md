---
title: 'D2D1_TAG (D2d1) '
description: 應用程式定義的64位值，用於 \ 160; 標記一組轉譯作業。
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacd11aa016e64ed463f1809595c865ae7e1f124
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317207"
---
# <a name="d2d1_tag"></a><span data-ttu-id="a855b-104">D2D1 \_ 標記</span><span class="sxs-lookup"><span data-stu-id="a855b-104">D2D1\_TAG</span></span>

<span data-ttu-id="a855b-105">用來標記一組轉譯作業的應用程式定義64位值。</span><span class="sxs-lookup"><span data-stu-id="a855b-105">An application-defined 64-bit value used to mark a set of rendering operations.</span></span>


```C++
typedef UINT64 D2D1_TAG;
```



## <a name="remarks"></a><span data-ttu-id="a855b-106">備註</span><span class="sxs-lookup"><span data-stu-id="a855b-106">Remarks</span></span>

<span data-ttu-id="a855b-107">若要在一連串轉譯作業之前設定標記，請使用 [**ID2D1RenderTarget：： SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) 方法。</span><span class="sxs-lookup"><span data-stu-id="a855b-107">To set a tag before a series of rendering operations, use the [**ID2D1RenderTarget::SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) method.</span></span> <span data-ttu-id="a855b-108">若要取出目前的標記，請使用 [**ID2D1RenderTarget：： GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) 方法。</span><span class="sxs-lookup"><span data-stu-id="a855b-108">To retrieve the current tag, use the [**ID2D1RenderTarget::GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a855b-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="a855b-109">Requirements</span></span>



| <span data-ttu-id="a855b-110">需求</span><span class="sxs-lookup"><span data-stu-id="a855b-110">Requirement</span></span> | <span data-ttu-id="a855b-111">值</span><span class="sxs-lookup"><span data-stu-id="a855b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a855b-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a855b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a855b-113">Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="a855b-113">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="a855b-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a855b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a855b-115">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a855b-115">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a855b-116">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="a855b-116">Minimum supported phone</span></span><br/>  | <span data-ttu-id="a855b-117">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a855b-117">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="a855b-118">標頭</span><span class="sxs-lookup"><span data-stu-id="a855b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a855b-119"><dt>D2d1。h</dt></span><span class="sxs-lookup"><span data-stu-id="a855b-119"><dt>D2d1.h</dt></span></span> </dl>                                                        |



## <a name="see-also"></a><span data-ttu-id="a855b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a855b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a855b-121">**GetTags**</span><span class="sxs-lookup"><span data-stu-id="a855b-121">**GetTags**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[<span data-ttu-id="a855b-122">**SetTags**</span><span class="sxs-lookup"><span data-stu-id="a855b-122">**SetTags**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 

