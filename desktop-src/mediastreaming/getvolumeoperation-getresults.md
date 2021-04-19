---
title: GetVolumeOperation. GetResults 方法
description: 傳回 GetVolumeAsync 啟動的非同步作業結果。
ms.assetid: 71DC4D76-4CC2-4D40-960F-AF56E1F33557
keywords:
- GetResults 方法媒體串流 API
- GetResults 方法媒體串流 API，GetVolumeOperation 介面
- GetVolumeOperation 介面媒體串流 API，GetResults 方法
topic_type:
- apiref
api_name:
- GetVolumeOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 444eaf590e5afc5d4f5185bcd3793698d6fe4535
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969705"
---
# <a name="getvolumeoperationgetresults-method"></a><span data-ttu-id="ea91e-106">GetVolumeOperation. GetResults 方法</span><span class="sxs-lookup"><span data-stu-id="ea91e-106">GetVolumeOperation.GetResults method</span></span>

<span data-ttu-id="ea91e-107">傳回 [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync)啟動的非同步作業結果。</span><span class="sxs-lookup"><span data-stu-id="ea91e-107">Returns the results of the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="ea91e-108">語法</span><span class="sxs-lookup"><span data-stu-id="ea91e-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="ea91e-109">參數</span><span class="sxs-lookup"><span data-stu-id="ea91e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea91e-110">*值* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="ea91e-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ea91e-111">磁片區。</span><span class="sxs-lookup"><span data-stu-id="ea91e-111">The volume.</span></span> <span data-ttu-id="ea91e-112">介於0與100之間的值。</span><span class="sxs-lookup"><span data-stu-id="ea91e-112">A value between 0 and 100.</span></span> <span data-ttu-id="ea91e-113">0表示最小磁片區，100表示最大磁片區。</span><span class="sxs-lookup"><span data-stu-id="ea91e-113">0 indicates minimum volume, and 100 indicates maximum volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea91e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea91e-114">Return value</span></span>

<span data-ttu-id="ea91e-115">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="ea91e-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ea91e-116">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="ea91e-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ea91e-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ea91e-117">Return code</span></span>                                                                          | <span data-ttu-id="ea91e-118">Description</span><span class="sxs-lookup"><span data-stu-id="ea91e-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ea91e-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ea91e-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ea91e-120">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="ea91e-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ea91e-121">備註</span><span class="sxs-lookup"><span data-stu-id="ea91e-121">Remarks</span></span>

<span data-ttu-id="ea91e-122">**GetResults** 方法通常是由設定 [**Completed**](getvolumeoperation-completed.md)屬性所註冊的事件處理常式所呼叫。</span><span class="sxs-lookup"><span data-stu-id="ea91e-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getvolumeoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea91e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea91e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea91e-124">**GetVolumeOperation**</span><span class="sxs-lookup"><span data-stu-id="ea91e-124">**GetVolumeOperation**</span></span>](getvolumeoperation.md)
</dt> </dl>

 

