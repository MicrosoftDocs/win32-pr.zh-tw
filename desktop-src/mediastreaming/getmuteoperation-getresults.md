---
title: GetMuteOperation. GetResults 方法
description: 傳回 GetMuteAsync 啟動的非同步作業結果。
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- GetResults 方法媒體串流 API
- GetResults 方法媒體串流 API，GetMuteOperation 介面
- GetMuteOperation 介面媒體串流 API，GetResults 方法
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33c43dc7fee228b1808ff4f607ee6a72faf1e770
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092668"
---
# <a name="getmuteoperationgetresults-method"></a><span data-ttu-id="918cf-106">GetMuteOperation. GetResults 方法</span><span class="sxs-lookup"><span data-stu-id="918cf-106">GetMuteOperation.GetResults method</span></span>

<span data-ttu-id="918cf-107">傳回 [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync)啟動的非同步作業結果。</span><span class="sxs-lookup"><span data-stu-id="918cf-107">Returns the results of the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="918cf-108">語法</span><span class="sxs-lookup"><span data-stu-id="918cf-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="918cf-109">參數</span><span class="sxs-lookup"><span data-stu-id="918cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="918cf-110">*值* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="918cf-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="918cf-111">靜音值。</span><span class="sxs-lookup"><span data-stu-id="918cf-111">The mute value.</span></span> <span data-ttu-id="918cf-112">值為 true 表示音訊目前為靜音。</span><span class="sxs-lookup"><span data-stu-id="918cf-112">A value of true indicates that audio is currently muted.</span></span> <span data-ttu-id="918cf-113">值為 false 表示音訊未靜音。</span><span class="sxs-lookup"><span data-stu-id="918cf-113">A value of false indicates that audio is not muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="918cf-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="918cf-114">Return value</span></span>

<span data-ttu-id="918cf-115">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="918cf-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="918cf-116">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="918cf-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="918cf-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="918cf-117">Return code</span></span>                                                                          | <span data-ttu-id="918cf-118">Description</span><span class="sxs-lookup"><span data-stu-id="918cf-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="918cf-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="918cf-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="918cf-120">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="918cf-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="918cf-121">備註</span><span class="sxs-lookup"><span data-stu-id="918cf-121">Remarks</span></span>

<span data-ttu-id="918cf-122">**GetResults** 方法通常是由設定 [**Completed**](getmuteoperation-completed.md)屬性所註冊的事件處理常式所呼叫。</span><span class="sxs-lookup"><span data-stu-id="918cf-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getmuteoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="918cf-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="918cf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="918cf-124">**GetMuteOperation**</span><span class="sxs-lookup"><span data-stu-id="918cf-124">**GetMuteOperation**</span></span>](getmuteoperation.md)
</dt> </dl>

 

