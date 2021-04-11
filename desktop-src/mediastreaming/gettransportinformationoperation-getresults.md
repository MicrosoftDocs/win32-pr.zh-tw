---
title: GetTransportInformationOperation GetResults 方法
description: 傳回 GetTransportInformationAsync 啟動的非同步作業結果。
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- GetResults 方法媒體串流 API
- GetResults 方法媒體串流 API，GetTransportInformationOperation 介面
- GetTransportInformationOperation 介面媒體串流 API，GetResults 方法
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17f846a5824ed07bcaf849a540429eaabe46f3d2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375201"
---
# <a name="gettransportinformationoperationgetresults-method"></a><span data-ttu-id="c5086-106">GetTransportInformationOperation：： GetResults 方法</span><span class="sxs-lookup"><span data-stu-id="c5086-106">GetTransportInformationOperation::GetResults method</span></span>

<span data-ttu-id="c5086-107">傳回 [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync)啟動的非同步作業結果。</span><span class="sxs-lookup"><span data-stu-id="c5086-107">Returns the results of the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5086-108">語法</span><span class="sxs-lookup"><span data-stu-id="c5086-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a><span data-ttu-id="c5086-109">參數</span><span class="sxs-lookup"><span data-stu-id="c5086-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5086-110">*值* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="c5086-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c5086-111">[**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation)結構的參考，其中包含作業的結果。</span><span class="sxs-lookup"><span data-stu-id="c5086-111">A reference to a [**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) structure that contains the results of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5086-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5086-112">Return value</span></span>

<span data-ttu-id="c5086-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="c5086-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c5086-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="c5086-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c5086-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c5086-115">Return code</span></span>                                                                          | <span data-ttu-id="c5086-116">Description</span><span class="sxs-lookup"><span data-stu-id="c5086-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c5086-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c5086-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c5086-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="c5086-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c5086-119">備註</span><span class="sxs-lookup"><span data-stu-id="c5086-119">Remarks</span></span>

<span data-ttu-id="c5086-120">**GetResults** 方法通常是由設定 [**Completed**](gettransportinformationoperation-completed.md)屬性所註冊的事件處理常式所呼叫。</span><span class="sxs-lookup"><span data-stu-id="c5086-120">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](gettransportinformationoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5086-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5086-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5086-122">**GetTransportInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="c5086-122">**GetTransportInformationOperation**</span></span>](gettransportinformationoperation.md)
</dt> </dl>

 

