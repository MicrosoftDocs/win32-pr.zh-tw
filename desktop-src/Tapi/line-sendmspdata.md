---
description: '\_當電話語音服務提供者 (TSP) 想要將資訊傳遞給媒體服務提供者 (MSP) 時，會傳送 TSPI LINE SENDMSPDATA 訊息。'
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: 'LINE_SENDMSPDATA 訊息 (Tspi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce46664be0bc7f312af8b45cc5e06e13a7d91488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993293"
---
# <a name="line_sendmspdata-message"></a><span data-ttu-id="575c9-103">行 \_ SENDMSPDATA 訊息</span><span class="sxs-lookup"><span data-stu-id="575c9-103">LINE\_SENDMSPDATA message</span></span>

<span data-ttu-id="575c9-104">當電話語音服務提供者 (TSP) 想要將資訊傳遞給媒體服務提供者 (MSP) 時，會傳送 TSPI **LINE \_ SENDMSPDATA** 訊息。</span><span class="sxs-lookup"><span data-stu-id="575c9-104">The TSPI **LINE\_SENDMSPDATA** message is sent when the telephony service provider (TSP) wants to pass information to the media service provider (MSP).</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="575c9-105">參數</span><span class="sxs-lookup"><span data-stu-id="575c9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="575c9-106">*htLine*</span><span class="sxs-lookup"><span data-stu-id="575c9-106">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="575c9-107">線路的 TAPI 控制碼。</span><span class="sxs-lookup"><span data-stu-id="575c9-107">The TAPI handle for the line.</span></span>

</dd> <dt>

<span data-ttu-id="575c9-108">*htCall*</span><span class="sxs-lookup"><span data-stu-id="575c9-108">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="575c9-109">呼叫的 TAPI 控制碼。</span><span class="sxs-lookup"><span data-stu-id="575c9-109">The TAPI handle for the call.</span></span>

</dd> <dt>

<span data-ttu-id="575c9-110">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="575c9-110">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="575c9-111">值行 \_ SENDMSPDATA。</span><span class="sxs-lookup"><span data-stu-id="575c9-111">The value LINE\_SENDMSPDATA.</span></span>

</dd> <dt>

<span data-ttu-id="575c9-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="575c9-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="575c9-113">識別應該接收訊息的 MSP。</span><span class="sxs-lookup"><span data-stu-id="575c9-113">Identifies the MSP that should receive the message.</span></span> <span data-ttu-id="575c9-114">如果是0，則會將訊息傳送至所有 Msp。</span><span class="sxs-lookup"><span data-stu-id="575c9-114">If 0, the message will be sent to all MSPs.</span></span> <span data-ttu-id="575c9-115">這是傳遞給 [**TSPI \_ LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) 函數的控制碼。</span><span class="sxs-lookup"><span data-stu-id="575c9-115">This is the handle that is passed to the [**TSPI\_LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) function.</span></span>

</dd> <dt>

<span data-ttu-id="575c9-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="575c9-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="575c9-117">要傳遞至 MSP 的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="575c9-117">The buffer to pass to the MSP.</span></span> <span data-ttu-id="575c9-118">TAPI 不會解讀緩衝區。</span><span class="sxs-lookup"><span data-stu-id="575c9-118">The buffer is not interpreted by TAPI.</span></span>

</dd> <dt>

<span data-ttu-id="575c9-119">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="575c9-119">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="575c9-120">*DwParam2* 中緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="575c9-120">The size, in bytes, of the buffer in *dwParam2*.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="575c9-121">備註</span><span class="sxs-lookup"><span data-stu-id="575c9-121">Remarks</span></span>

<span data-ttu-id="575c9-122">服務提供者必須協調 TAPI 3.0 版或更新版本，此訊息才能運作。</span><span class="sxs-lookup"><span data-stu-id="575c9-122">The service provider must negotiate a TAPI version 3.0 or later for this message to operate.</span></span>

## <a name="requirements"></a><span data-ttu-id="575c9-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="575c9-123">Requirements</span></span>



| <span data-ttu-id="575c9-124">需求</span><span class="sxs-lookup"><span data-stu-id="575c9-124">Requirement</span></span> | <span data-ttu-id="575c9-125">值</span><span class="sxs-lookup"><span data-stu-id="575c9-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="575c9-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="575c9-126">TAPI version</span></span><br/> | <span data-ttu-id="575c9-127">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="575c9-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="575c9-128">標頭</span><span class="sxs-lookup"><span data-stu-id="575c9-128">Header</span></span><br/>       | <dl> <span data-ttu-id="575c9-129"><dt>Tspi。h</dt></span><span class="sxs-lookup"><span data-stu-id="575c9-129"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="575c9-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="575c9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="575c9-131">關於媒體服務提供者 (MSP) </span><span class="sxs-lookup"><span data-stu-id="575c9-131">About The Media Service Provider (MSP)</span></span>](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[<span data-ttu-id="575c9-132">**TSPI \_ lineMSPIdentify**</span><span class="sxs-lookup"><span data-stu-id="575c9-132">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[<span data-ttu-id="575c9-133">**TSPI \_ LineCreateMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="575c9-133">**TSPI\_LineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[<span data-ttu-id="575c9-134">**TSPI \_ lineCloseMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="575c9-134">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[<span data-ttu-id="575c9-135">**TSPI \_ lineRecieveMSPData**</span><span class="sxs-lookup"><span data-stu-id="575c9-135">**TSPI\_lineRecieveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[<span data-ttu-id="575c9-136">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="575c9-136">**LINEDEVCAPS**</span></span>](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

