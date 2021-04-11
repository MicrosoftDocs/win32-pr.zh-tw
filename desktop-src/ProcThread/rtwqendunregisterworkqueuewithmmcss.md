---
description: 完成非同步要求，以利用多媒體類別排程器服務將工作佇列取消註冊 (MMCSS) 工作。
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: RtwqEndUnregisterWorkQueueWithMMCSS 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtwqEndUnregisterWorkQueueWithMMCSS
api_type:
- DllExport
api_location:
- RTWorkQ.dll
ms.openlocfilehash: b55386b2a018b0e311a1d4dbb2084b136d49c2f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849620"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a><span data-ttu-id="63a2e-103">RtwqEndUnregisterWorkQueueWithMMCSS 函式</span><span class="sxs-lookup"><span data-stu-id="63a2e-103">RtwqEndUnregisterWorkQueueWithMMCSS function</span></span>

<span data-ttu-id="63a2e-104">完成非同步要求，以利用多媒體類別排程器服務將工作佇列取消註冊 (MMCSS) 工作。</span><span class="sxs-lookup"><span data-stu-id="63a2e-104">Completes an asynchronous request to unregister a work queue with a Multimedia Class Scheduler Service (MMCSS) task.</span></span>

## <a name="syntax"></a><span data-ttu-id="63a2e-105">語法</span><span class="sxs-lookup"><span data-stu-id="63a2e-105">Syntax</span></span>


```C++
HRESULT WINAPI RtwqEndUnregisterWorkQueueWithMMCSS(
    IMFAsyncResult  *pResult 
);
```



## <a name="parameters"></a><span data-ttu-id="63a2e-106">參數</span><span class="sxs-lookup"><span data-stu-id="63a2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63a2e-107">*pResult*</span><span class="sxs-lookup"><span data-stu-id="63a2e-107">*pResult*</span></span> 
</dt> <dd>

<span data-ttu-id="63a2e-108">[**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="63a2e-108">Pointer to the [**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="63a2e-109">傳入您的回呼物件在 [**IRtwqAsyncCallback：： Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) 方法中收到的相同指標。</span><span class="sxs-lookup"><span data-stu-id="63a2e-109">Pass in the same pointer that your callback object received in the [**IRtwqAsyncCallback::Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63a2e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="63a2e-110">Return value</span></span>

<span data-ttu-id="63a2e-111">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="63a2e-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="63a2e-112">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="63a2e-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="63a2e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="63a2e-113">Requirements</span></span>



| <span data-ttu-id="63a2e-114">需求</span><span class="sxs-lookup"><span data-stu-id="63a2e-114">Requirement</span></span> | <span data-ttu-id="63a2e-115">值</span><span class="sxs-lookup"><span data-stu-id="63a2e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63a2e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63a2e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="63a2e-117">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63a2e-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="63a2e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63a2e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="63a2e-119">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63a2e-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="63a2e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="63a2e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="63a2e-121"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="63a2e-121"><dt>None</dt></span></span> </dl>        |
| <span data-ttu-id="63a2e-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="63a2e-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="63a2e-123"><dt>Rtworkq .lib</dt></span><span class="sxs-lookup"><span data-stu-id="63a2e-123"><dt>Rtworkq.lib</dt></span></span> </dl> |
| <span data-ttu-id="63a2e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="63a2e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63a2e-125"><dt>RTWorkQ.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63a2e-125"><dt>RTWorkQ.dll</dt></span></span> </dl> |



 

 
