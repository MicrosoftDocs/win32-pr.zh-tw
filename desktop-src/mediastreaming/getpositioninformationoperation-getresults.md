---
title: GetPositionInformationOperation. GetResults 方法
description: 傳回 GetPositionInformationAsync 啟動的非同步作業結果。
ms.assetid: 1DC7CD65-1F0F-44A5-9836-C77A5C23F91E
keywords:
- GetResults 方法媒體串流 API
- GetResults 方法媒體串流 API，GetPositionInformationOperation 介面
- GetPositionInformationOperation 介面媒體串流 API，GetResults 方法
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a0b4311c3be814a73ddb1e2a9b18d8e19aea9ee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682222"
---
# <a name="getpositioninformationoperationgetresults-method"></a><span data-ttu-id="21224-106">GetPositionInformationOperation. GetResults 方法</span><span class="sxs-lookup"><span data-stu-id="21224-106">GetPositionInformationOperation.GetResults method</span></span>

<span data-ttu-id="21224-107">傳回 [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync)啟動的非同步作業結果。</span><span class="sxs-lookup"><span data-stu-id="21224-107">Returns the results of the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="21224-108">語法</span><span class="sxs-lookup"><span data-stu-id="21224-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] PositionInformation *value
);
```



## <a name="parameters"></a><span data-ttu-id="21224-109">參數</span><span class="sxs-lookup"><span data-stu-id="21224-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21224-110">*值* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="21224-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="21224-111">[**PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation)結構的參考，其中包含作業的結果。</span><span class="sxs-lookup"><span data-stu-id="21224-111">A reference to a [**PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) structure that contains the results of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21224-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="21224-112">Return value</span></span>

<span data-ttu-id="21224-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="21224-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="21224-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="21224-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="21224-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="21224-115">Return code</span></span>                                                                          | <span data-ttu-id="21224-116">Description</span><span class="sxs-lookup"><span data-stu-id="21224-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="21224-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="21224-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="21224-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="21224-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="21224-119">備註</span><span class="sxs-lookup"><span data-stu-id="21224-119">Remarks</span></span>

<span data-ttu-id="21224-120">**GetResults** 方法通常是由設定 [**Completed**](getpositioninformationoperation-completed.md)屬性所註冊的事件處理常式所呼叫。</span><span class="sxs-lookup"><span data-stu-id="21224-120">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getpositioninformationoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="21224-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21224-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21224-122">**GetPositionInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="21224-122">**GetPositionInformationOperation**</span></span>](getpositioninformationoperation.md)
</dt> </dl>

 

