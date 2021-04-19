---
description: 回呼，會通知主機相關要求所傳回的錯誤。
MS-HAID: vspixengine.IPixErrorCallback\_ErrorListCallback\_DWORD\_Issue\_arr\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixErrorCallback：： ErrorListCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B345846D-4853-4F6B-AB79-42265720451D
api_name:
- IPixErrorCallback.ErrorListCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 91754cd7db13165efcb66e9bc87b8e4661842fce
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106986240"
---
# <a name="span-idvspixengineipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arrspanipixerrorcallbackerrorlistcallback-method"></a><span data-ttu-id="154e1-103"><span id="vspixengine.ipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arr"></span>IPixErrorCallback：： ErrorListCallback 方法</span><span class="sxs-lookup"><span data-stu-id="154e1-103"><span id="vspixengine.ipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arr"></span>IPixErrorCallback::ErrorListCallback method</span></span>

<span data-ttu-id="154e1-104">回呼，會通知主機相關要求所傳回的錯誤。</span><span class="sxs-lookup"><span data-stu-id="154e1-104">A callback that notifies the host of errors returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="154e1-105">語法</span><span class="sxs-lookup"><span data-stu-id="154e1-105">Syntax</span></span>


```C++
HRESULT ErrorListCallback(
   DWORD    count,
   Issue [] count0_errorList,
   DWORD    count,
   Issue [] count0_warningList
);
```

## <a name="parameters"></a><span data-ttu-id="154e1-106">參數</span><span class="sxs-lookup"><span data-stu-id="154e1-106">Parameters</span></span>

<span data-ttu-id="154e1-107">*計數* </span><span class="sxs-lookup"><span data-stu-id="154e1-107">*count* </span></span>  
<span data-ttu-id="154e1-108">錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="154e1-108">The number of errors.</span></span>

<span data-ttu-id="154e1-109">*count0 \_ errorList* </span><span class="sxs-lookup"><span data-stu-id="154e1-109">*count0\_errorList* </span></span>  
<span data-ttu-id="154e1-110">錯誤。</span><span class="sxs-lookup"><span data-stu-id="154e1-110">The errors.</span></span>

<span data-ttu-id="154e1-111">*計數* </span><span class="sxs-lookup"><span data-stu-id="154e1-111">*count* </span></span>  
<span data-ttu-id="154e1-112">警告的數目。</span><span class="sxs-lookup"><span data-stu-id="154e1-112">The number of warningns.</span></span>

<span data-ttu-id="154e1-113">*count0 \_ 警告清單* </span><span class="sxs-lookup"><span data-stu-id="154e1-113">*count0\_warningList* </span></span>  
<span data-ttu-id="154e1-114">警告。</span><span class="sxs-lookup"><span data-stu-id="154e1-114">The warnings.</span></span>

## <a name="return-value"></a><span data-ttu-id="154e1-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="154e1-115">Return value</span></span>

<span data-ttu-id="154e1-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="154e1-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="154e1-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="154e1-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="154e1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="154e1-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="154e1-119">標頭</span><span class="sxs-lookup"><span data-stu-id="154e1-119">Header</span></span></p></td><td><span data-ttu-id="154e1-120">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="154e1-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="154e1-121"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="154e1-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="154e1-122">**IPixErrorCallback**</span><span class="sxs-lookup"><span data-stu-id="154e1-122">**IPixErrorCallback**</span></span>](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
