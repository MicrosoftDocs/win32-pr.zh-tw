---
description: '\_當地址的狀態變更在應用程式目前開啟的行上時，就會傳送 TAPI 線路 ADDRESSSTATE 訊息。 應用程式可以叫用 lineGetAddressStatus 來判斷位址的目前狀態。'
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: 'LINE_ADDRESSSTATE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d85b42f6957487ff24706485bd09d1d47880fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994026"
---
# <a name="line_addressstate-message"></a><span data-ttu-id="db4a9-104">行 \_ ADDRESSSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="db4a9-104">LINE\_ADDRESSSTATE message</span></span>

<span data-ttu-id="db4a9-105">當地址的狀態變更在應用程式目前開啟的行上時，就會傳送 TAPI **線路 \_ ADDRESSSTATE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="db4a9-105">The TAPI **LINE\_ADDRESSSTATE** message is sent when the status of an address changes on a line that is currently open by the application.</span></span> <span data-ttu-id="db4a9-106">應用程式可以叫用 [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) 來判斷位址的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="db4a9-106">The application can invoke [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) to determine the current status of the address.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="db4a9-107">參數</span><span class="sxs-lookup"><span data-stu-id="db4a9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db4a9-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="db4a9-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="db4a9-109">線路裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="db4a9-109">A handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="db4a9-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="db4a9-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="db4a9-111">開啟行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="db4a9-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="db4a9-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="db4a9-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="db4a9-113">已變更狀態之位址的位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="db4a9-113">The address identifier of the address that changed status.</span></span>

</dd> <dt>

<span data-ttu-id="db4a9-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="db4a9-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="db4a9-115">變更的位址狀態。</span><span class="sxs-lookup"><span data-stu-id="db4a9-115">The address state that changed.</span></span> <span data-ttu-id="db4a9-116">可以是一或多個 [**LINEADDRESSSTATE \_ 常數**](lineaddressstate--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="db4a9-116">Can be one or more of the [**LINEADDRESSSTATE\_ constants**](lineaddressstate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="db4a9-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="db4a9-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="db4a9-118">未使用的。</span><span class="sxs-lookup"><span data-stu-id="db4a9-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db4a9-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="db4a9-119">Return value</span></span>

<span data-ttu-id="db4a9-120">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="db4a9-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db4a9-121">備註</span><span class="sxs-lookup"><span data-stu-id="db4a9-121">Remarks</span></span>

<span data-ttu-id="db4a9-122">**該行 \_ ADDRESSSTATE** 訊息會傳送至已開啟行裝置且已啟用此訊息的任何應用程式。</span><span class="sxs-lookup"><span data-stu-id="db4a9-122">The **LINE\_ADDRESSSTATE** message is sent to any application that has opened the line device and that has enabled this message.</span></span> <span data-ttu-id="db4a9-123">您可以使用 [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) 和 [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)來控制和查詢不同狀態專案的這項訊息傳送。</span><span class="sxs-lookup"><span data-stu-id="db4a9-123">The sending of this message for the various status items can be controlled and queried using [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) and [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span> <span data-ttu-id="db4a9-124">預設會停用 [位址狀態報表]。</span><span class="sxs-lookup"><span data-stu-id="db4a9-124">By default, address status reporting is disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="db4a9-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="db4a9-125">Requirements</span></span>



| <span data-ttu-id="db4a9-126">需求</span><span class="sxs-lookup"><span data-stu-id="db4a9-126">Requirement</span></span> | <span data-ttu-id="db4a9-127">值</span><span class="sxs-lookup"><span data-stu-id="db4a9-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="db4a9-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="db4a9-128">TAPI version</span></span><br/> | <span data-ttu-id="db4a9-129">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="db4a9-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="db4a9-130">標頭</span><span class="sxs-lookup"><span data-stu-id="db4a9-130">Header</span></span><br/>       | <dl> <span data-ttu-id="db4a9-131"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="db4a9-131"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db4a9-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db4a9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db4a9-133">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="db4a9-133">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="db4a9-134">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="db4a9-134">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[<span data-ttu-id="db4a9-135">**lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="db4a9-135">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[<span data-ttu-id="db4a9-136">**lineGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="db4a9-136">**lineGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages)
</dt> <dt>

[<span data-ttu-id="db4a9-137">**lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="db4a9-137">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> </dl>

 

 




