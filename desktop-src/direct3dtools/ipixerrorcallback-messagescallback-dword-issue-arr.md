---
description: 回呼，會通知主機相關要求所傳回的訊息。
MS-HAID: vspixengine.IPixErrorCallback\_MessagesCallback\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixErrorCallback：： MessagesCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 55343F63-BB58-4F57-884D-CEFE8AB57A27
api_name:
- IPixErrorCallback.MessagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b95a95a6ef472f2603bfa6b21c85659634074a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970078"
---
# <a name="span-idvspixengineipixerrorcallback_messagescallback_dword_issue_arrspanipixerrorcallbackmessagescallback-method"></a><span data-ttu-id="364f5-103"><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>IPixErrorCallback：： MessagesCallback 方法</span><span class="sxs-lookup"><span data-stu-id="364f5-103"><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>IPixErrorCallback::MessagesCallback method</span></span>

<span data-ttu-id="364f5-104">回呼，會通知主機相關要求所傳回的訊息。</span><span class="sxs-lookup"><span data-stu-id="364f5-104">A callback that notifies the host of messages returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="364f5-105">語法</span><span class="sxs-lookup"><span data-stu-id="364f5-105">Syntax</span></span>


```C++
HRESULT MessagesCallback(
   DWORD    count,
   Issue [] count0_messages
);
```

## <a name="parameters"></a><span data-ttu-id="364f5-106">參數</span><span class="sxs-lookup"><span data-stu-id="364f5-106">Parameters</span></span>

<span data-ttu-id="364f5-107">*計數* </span><span class="sxs-lookup"><span data-stu-id="364f5-107">*count* </span></span>  
<span data-ttu-id="364f5-108">訊息數目。</span><span class="sxs-lookup"><span data-stu-id="364f5-108">The number of messages.</span></span>

<span data-ttu-id="364f5-109">*count0 \_ 訊息* </span><span class="sxs-lookup"><span data-stu-id="364f5-109">*count0\_messages* </span></span>  
<span data-ttu-id="364f5-110">訊息。</span><span class="sxs-lookup"><span data-stu-id="364f5-110">The messages.</span></span>

## <a name="return-value"></a><span data-ttu-id="364f5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="364f5-111">Return value</span></span>

<span data-ttu-id="364f5-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="364f5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="364f5-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="364f5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="364f5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="364f5-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="364f5-115">標頭</span><span class="sxs-lookup"><span data-stu-id="364f5-115">Header</span></span></p></td><td><span data-ttu-id="364f5-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="364f5-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="364f5-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="364f5-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="364f5-118">**IPixErrorCallback**</span><span class="sxs-lookup"><span data-stu-id="364f5-118">**IPixErrorCallback**</span></span>](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
