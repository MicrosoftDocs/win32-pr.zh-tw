---
description: '\_當新的呼叫中樞建立時，會傳送 TAPI 線路 APPNEWCALLHUB 訊息來通知應用程式。'
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: 'LINE_APPNEWCALLHUB 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634dd82aadd5e3c8a7664572136b54f8bbdf8a52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998660"
---
# <a name="line_appnewcallhub-message"></a><span data-ttu-id="b56b7-103">行 \_ APPNEWCALLHUB 訊息</span><span class="sxs-lookup"><span data-stu-id="b56b7-103">LINE\_APPNEWCALLHUB message</span></span>

<span data-ttu-id="b56b7-104">當新的呼叫中樞建立時，會傳送 TAPI **線路 \_ APPNEWCALLHUB** 訊息來通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="b56b7-104">The TAPI **LINE\_APPNEWCALLHUB** message is sent to inform an application when a new call hub has been created.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="b56b7-105">參數</span><span class="sxs-lookup"><span data-stu-id="b56b7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b56b7-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="b56b7-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="b56b7-107">呼叫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b56b7-107">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="b56b7-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="b56b7-109">開啟呼叫的行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="b56b7-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b56b7-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="b56b7-111">新中樞上的追蹤層級，如其中一個 [**LINECALLHUBTRACKING \_ 常數**](linecallhubtracking--constants.md)所定義。</span><span class="sxs-lookup"><span data-stu-id="b56b7-111">The tracking level on the new hub, as defined by one of the [**LINECALLHUBTRACKING\_ Constants**](linecallhubtracking--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b56b7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b56b7-112">Return value</span></span>

<span data-ttu-id="b56b7-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="b56b7-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b56b7-114">備註</span><span class="sxs-lookup"><span data-stu-id="b56b7-114">Remarks</span></span>

<span data-ttu-id="b56b7-115">此訊息源自 TAPI 而不是服務提供者，因此沒有對應的 TSPI 訊息。</span><span class="sxs-lookup"><span data-stu-id="b56b7-115">This message originates with TAPI rather than with a service provider, so there is no corresponding TSPI message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b56b7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b56b7-116">Requirements</span></span>



| <span data-ttu-id="b56b7-117">需求</span><span class="sxs-lookup"><span data-stu-id="b56b7-117">Requirement</span></span> | <span data-ttu-id="b56b7-118">值</span><span class="sxs-lookup"><span data-stu-id="b56b7-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b56b7-119">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="b56b7-119">TAPI version</span></span><br/> | <span data-ttu-id="b56b7-120">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="b56b7-120">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="b56b7-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b56b7-121">Header</span></span><br/>       | <dl> <span data-ttu-id="b56b7-122"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="b56b7-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




