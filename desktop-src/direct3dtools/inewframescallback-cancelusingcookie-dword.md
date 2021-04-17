---
description: 回呼，使用可唯一識別要求的 cookie 來通知主機已取消的要求。
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCookie\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: INewFramesCallback：： CancelUsingCookie 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36176554-BB4F-40CB-AB7B-4957DA84BAA8
api_name:
- INewFramesCallback.CancelUsingCookie
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dfbbbda1a11244088dccad640be348da1e4d8313
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467582"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcookie_dwordspaninewframescallbackcancelusingcookie-method"></a><span data-ttu-id="92b25-103"><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>INewFramesCallback：： CancelUsingCookie 方法</span><span class="sxs-lookup"><span data-stu-id="92b25-103"><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>INewFramesCallback::CancelUsingCookie method</span></span>

<span data-ttu-id="92b25-104">回呼，使用可唯一識別要求的 cookie 來通知主機已取消的要求。</span><span class="sxs-lookup"><span data-stu-id="92b25-104">A callback that notifies the host of a canceled request by using a cookie that uniquely identifies the request.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b25-105">語法</span><span class="sxs-lookup"><span data-stu-id="92b25-105">Syntax</span></span>


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="92b25-106">參數</span><span class="sxs-lookup"><span data-stu-id="92b25-106">Parameters</span></span>

<span data-ttu-id="92b25-107">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="92b25-107">*requestCookie* </span></span>  
<span data-ttu-id="92b25-108">可唯一 idenfies 已取消之要求的 cookie。</span><span class="sxs-lookup"><span data-stu-id="92b25-108">The cookie which uniquely idenfies the cancelled request.</span></span>

## <a name="return-value"></a><span data-ttu-id="92b25-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="92b25-109">Return value</span></span>

<span data-ttu-id="92b25-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="92b25-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="92b25-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="92b25-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="92b25-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="92b25-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="92b25-113">標頭</span><span class="sxs-lookup"><span data-stu-id="92b25-113">Header</span></span></p></td><td><span data-ttu-id="92b25-114">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="92b25-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="92b25-115"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="92b25-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="92b25-116">**INewFramesCallback**</span><span class="sxs-lookup"><span data-stu-id="92b25-116">**INewFramesCallback**</span></span>](/windows/desktop/direct3dtools/inewframescallback)

 

 
