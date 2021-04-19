---
description: '\_當呼叫中樞關閉時，就會傳送 TAPI 線路 CALLHUBCLOSE 訊息。'
ms.assetid: 738dcb20-99b5-44fe-8ad9-b14b8d977f53
title: 'LINE_CALLHUBCLOSE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b538d6f154f3dacb2d779b6233722df16cc635d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989816"
---
# <a name="line_callhubclose-message"></a><span data-ttu-id="25269-103">行 \_ CALLHUBCLOSE 訊息</span><span class="sxs-lookup"><span data-stu-id="25269-103">LINE\_CALLHUBCLOSE message</span></span>

<span data-ttu-id="25269-104">當呼叫中樞關閉時，就會傳送 TAPI **線路 \_ CALLHUBCLOSE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="25269-104">The TAPI **LINE\_CALLHUBCLOSE** message is sent when a call hub has been closed.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="25269-105">參數</span><span class="sxs-lookup"><span data-stu-id="25269-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25269-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="25269-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="25269-107">呼叫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="25269-107">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="25269-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="25269-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="25269-109">開啟呼叫的行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="25269-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="25269-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="25269-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="25269-111">保留的。</span><span class="sxs-lookup"><span data-stu-id="25269-111">Reserved.</span></span> <span data-ttu-id="25269-112">設定為0。</span><span class="sxs-lookup"><span data-stu-id="25269-112">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="25269-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="25269-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="25269-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="25269-114">Reserved.</span></span> <span data-ttu-id="25269-115">設定為0。</span><span class="sxs-lookup"><span data-stu-id="25269-115">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="25269-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="25269-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="25269-117">保留的。</span><span class="sxs-lookup"><span data-stu-id="25269-117">Reserved.</span></span> <span data-ttu-id="25269-118">設定為0。</span><span class="sxs-lookup"><span data-stu-id="25269-118">Set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25269-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="25269-119">Return value</span></span>

<span data-ttu-id="25269-120">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="25269-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25269-121">備註</span><span class="sxs-lookup"><span data-stu-id="25269-121">Remarks</span></span>

<span data-ttu-id="25269-122">此訊息源自 TAPI 而不是服務提供者，因此沒有對應的 TSPI 訊息。</span><span class="sxs-lookup"><span data-stu-id="25269-122">This message originates with TAPI rather than with a service provider, so there is no corresponding TSPI message.</span></span>

## <a name="requirements"></a><span data-ttu-id="25269-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="25269-123">Requirements</span></span>



| <span data-ttu-id="25269-124">需求</span><span class="sxs-lookup"><span data-stu-id="25269-124">Requirement</span></span> | <span data-ttu-id="25269-125">值</span><span class="sxs-lookup"><span data-stu-id="25269-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="25269-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="25269-126">TAPI version</span></span><br/> | <span data-ttu-id="25269-127">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="25269-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="25269-128">標頭</span><span class="sxs-lookup"><span data-stu-id="25269-128">Header</span></span><br/>       | <dl> <span data-ttu-id="25269-129"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="25269-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




