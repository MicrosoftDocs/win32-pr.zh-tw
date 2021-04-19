---
description: '\_系統會傳送 TAPI 電話移除訊息，以通知移除從電話裝置的系統) 移除 (刪除。'
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: 'PHONE_REMOVE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab32ba8b8a8e003c5d87109dd2d0c9dbe98c236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987118"
---
# <a name="phone_remove-message"></a><span data-ttu-id="73a38-103">手機 \_ 移除訊息</span><span class="sxs-lookup"><span data-stu-id="73a38-103">PHONE\_REMOVE message</span></span>

<span data-ttu-id="73a38-104">系統會傳送 TAPI **電話 \_ 移除** 訊息，以通知移除從電話裝置的系統) 移除 (刪除。</span><span class="sxs-lookup"><span data-stu-id="73a38-104">The TAPI **PHONE\_REMOVE** message is sent to inform an application of the removal (deletion from the system) of a phone device.</span></span> <span data-ttu-id="73a38-105">一般而言，這不會用於暫時移除（例如，將 PCMCIA 裝置解壓縮），但僅適用于永久移除，如果重新初始化 TAPI，服務提供者將不會再回報該裝置。</span><span class="sxs-lookup"><span data-stu-id="73a38-105">Generally, this is not used for temporary removals, such as extraction of PCMCIA devices, but only for permanent removals in which the device would no longer be reported by the service provider if TAPI were reinitialized.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="73a38-106">參數</span><span class="sxs-lookup"><span data-stu-id="73a38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73a38-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="73a38-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="73a38-108">保留的。</span><span class="sxs-lookup"><span data-stu-id="73a38-108">Reserved.</span></span> <span data-ttu-id="73a38-109">設定為零。</span><span class="sxs-lookup"><span data-stu-id="73a38-109">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="73a38-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="73a38-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="73a38-111">保留的。</span><span class="sxs-lookup"><span data-stu-id="73a38-111">Reserved.</span></span> <span data-ttu-id="73a38-112">設定為零。</span><span class="sxs-lookup"><span data-stu-id="73a38-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="73a38-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="73a38-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="73a38-114">已移除之手機裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="73a38-114">Identifier of the phone device that was removed.</span></span>

</dd> <dt>

<span data-ttu-id="73a38-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="73a38-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="73a38-116">保留的。</span><span class="sxs-lookup"><span data-stu-id="73a38-116">Reserved.</span></span> <span data-ttu-id="73a38-117">設定為零。</span><span class="sxs-lookup"><span data-stu-id="73a38-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="73a38-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="73a38-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="73a38-119">保留的。</span><span class="sxs-lookup"><span data-stu-id="73a38-119">Reserved.</span></span> <span data-ttu-id="73a38-120">設定為零。</span><span class="sxs-lookup"><span data-stu-id="73a38-120">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73a38-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="73a38-121">Return value</span></span>

<span data-ttu-id="73a38-122">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="73a38-122">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73a38-123">備註</span><span class="sxs-lookup"><span data-stu-id="73a38-123">Remarks</span></span>

<span data-ttu-id="73a38-124">應用程式 TAPI 2.0 版或更新版本會傳送 **電話 \_ 移除** 訊息。</span><span class="sxs-lookup"><span data-stu-id="73a38-124">Applications TAPI version 2.0 or later are sent a **PHONE\_REMOVE** message.</span></span> <span data-ttu-id="73a38-125">這會通知他們裝置已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="73a38-125">This informs them that the device has been removed from the system.</span></span> <span data-ttu-id="73a38-126">如果應用程式已開啟電話，則 **電話 \_ 移除** 訊息前面會有每個電話控制碼上的 [**電話 \_ 關閉**](phone-close.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="73a38-126">The **PHONE\_REMOVE** message is preceded by a [**PHONE\_CLOSE**](phone-close.md) message on each phone handle, if the application had the phone open.</span></span> <span data-ttu-id="73a38-127">這則訊息會傳送至所有支援 TAPI 2.0 版或更新版本的應用程式，這些應用程式已呼叫 [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)，包括當時未開啟任何手機裝置的應用程式。</span><span class="sxs-lookup"><span data-stu-id="73a38-127">This message is sent to all applications supporting TAPI version 2.0 or later that have called [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), including those that do not have any phone devices open at the time.</span></span>

<span data-ttu-id="73a38-128">繼承應用程式 (協商 TAPI 1.4 或更早版本的) 會傳送 [**電話 \_ 狀態**](phone-state.md) 消息，指出 PHONESTATE \_ 已移除，後面接著 [**電話 \_ 關閉**](phone-close.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="73a38-128">Older applications (that negotiated TAPI version 1.4 or earlier) are sent a [**PHONE\_STATE**](phone-state.md) message specifying PHONESTATE\_REMOVED, followed by a [**PHONE\_CLOSE**](phone-close.md) message.</span></span> <span data-ttu-id="73a38-129">不過，不同于 **行動電話 \_ 的** 訊息，這些較舊的應用程式只有在移除手機時，才會收到這些訊息。</span><span class="sxs-lookup"><span data-stu-id="73a38-129">Unlike the **PHONE\_REMOVE** message, however, these older applications can receive these messages only if they have the phone open when it is removed.</span></span> <span data-ttu-id="73a38-130">如果他們沒有開啟電話，則只有在裝置 \_ 嘗試存取裝置時，才會收到 PHONEERR NODEVICE 的指示。</span><span class="sxs-lookup"><span data-stu-id="73a38-130">If they do not have the phone open, their only indication that the device was removed would be receiving a PHONEERR\_NODEVICE when they attempt to access the device.</span></span>

<span data-ttu-id="73a38-131">移除裝置之後，依裝置識別碼存取裝置的任何嘗試都會導致 PHONEERR \_ NODEVICE 錯誤。</span><span class="sxs-lookup"><span data-stu-id="73a38-131">After a device has been removed, any attempt to access the device by its device identifier results in a PHONEERR\_NODEVICE error.</span></span> <span data-ttu-id="73a38-132">在所有 TAPI 應用程式都關機之後，重新開機 tapi 之後，當 TAPI 重新初始化時，移除的裝置就不再佔用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="73a38-132">After all TAPI applications have shutdown so that TAPI can restart, and when TAPI is reinitialized, the removed device no longer occupies a device identifier.</span></span>

> [!Note]  
> <span data-ttu-id="73a38-133">執行：它是 \_ 從服務提供者收到電話移除訊息之後，會傳回此 PHONEERR NODEVICE 訊息的 TAPI \_ ; 不會使用該電話裝置識別碼對該服務提供者進行其他呼叫。</span><span class="sxs-lookup"><span data-stu-id="73a38-133">Implementation: it is TAPI that returns this PHONEERR\_NODEVICE message after a PHONE\_REMOVE message is received from a service provider; no further calls are made to that service provider using that phone device identifier.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="73a38-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="73a38-134">Requirements</span></span>



| <span data-ttu-id="73a38-135">需求</span><span class="sxs-lookup"><span data-stu-id="73a38-135">Requirement</span></span> | <span data-ttu-id="73a38-136">值</span><span class="sxs-lookup"><span data-stu-id="73a38-136">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="73a38-137">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="73a38-137">TAPI version</span></span><br/> | <span data-ttu-id="73a38-138">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="73a38-138">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="73a38-139">標頭</span><span class="sxs-lookup"><span data-stu-id="73a38-139">Header</span></span><br/>       | <dl> <span data-ttu-id="73a38-140"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="73a38-140"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73a38-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73a38-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73a38-142">**電話 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="73a38-142">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="73a38-143">**電話 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="73a38-143">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="73a38-144">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="73a38-144">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="73a38-145">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="73a38-145">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




