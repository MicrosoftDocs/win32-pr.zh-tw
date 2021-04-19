---
description: '\_系統會傳送 TAPI 行移除訊息，通知應用程式移除 (從線路裝置的系統) 刪除。'
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: 'LINE_REMOVE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567ead3ad2941845dd22405f0d8706eca74bfbd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976106"
---
# <a name="line_remove-message"></a><span data-ttu-id="e50f2-103">行 \_ 移除訊息</span><span class="sxs-lookup"><span data-stu-id="e50f2-103">LINE\_REMOVE message</span></span>

<span data-ttu-id="e50f2-104">系統會傳送 TAPI **行 \_ 移除** 訊息，通知應用程式移除 (從線路裝置的系統) 刪除。</span><span class="sxs-lookup"><span data-stu-id="e50f2-104">The TAPI **LINE\_REMOVE** message is sent to inform an application of the removal (deletion from the system) of a line device.</span></span> <span data-ttu-id="e50f2-105">一般而言，這不會用於暫時移除（例如，將 PCMCIA 裝置解壓縮），但僅適用于永久移除，如果重新初始化 TAPI，服務提供者將不會再回報該裝置。</span><span class="sxs-lookup"><span data-stu-id="e50f2-105">Generally, this is not used for temporary removals, such as extraction of PCMCIA devices, but only for permanent removals in which the device would no longer be reported by the service provider if TAPI were reinitialized.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="e50f2-106">參數</span><span class="sxs-lookup"><span data-stu-id="e50f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e50f2-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="e50f2-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="e50f2-108">保留的。</span><span class="sxs-lookup"><span data-stu-id="e50f2-108">Reserved.</span></span> <span data-ttu-id="e50f2-109">設定為零。</span><span class="sxs-lookup"><span data-stu-id="e50f2-109">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e50f2-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="e50f2-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="e50f2-111">保留的。</span><span class="sxs-lookup"><span data-stu-id="e50f2-111">Reserved.</span></span> <span data-ttu-id="e50f2-112">設定為零。</span><span class="sxs-lookup"><span data-stu-id="e50f2-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e50f2-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e50f2-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="e50f2-114">已移除之行裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e50f2-114">Identifier of the line device that was removed.</span></span>

</dd> <dt>

<span data-ttu-id="e50f2-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e50f2-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="e50f2-116">保留的。</span><span class="sxs-lookup"><span data-stu-id="e50f2-116">Reserved.</span></span> <span data-ttu-id="e50f2-117">設定為零。</span><span class="sxs-lookup"><span data-stu-id="e50f2-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e50f2-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="e50f2-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="e50f2-119">保留的。</span><span class="sxs-lookup"><span data-stu-id="e50f2-119">Reserved.</span></span> <span data-ttu-id="e50f2-120">設定為零。</span><span class="sxs-lookup"><span data-stu-id="e50f2-120">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e50f2-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="e50f2-121">Return value</span></span>

<span data-ttu-id="e50f2-122">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="e50f2-122">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e50f2-123">備註</span><span class="sxs-lookup"><span data-stu-id="e50f2-123">Remarks</span></span>

<span data-ttu-id="e50f2-124">支援 TAPI 2.0 版或更新版本的應用程式會傳送 **一行 \_ 移除** 訊息。</span><span class="sxs-lookup"><span data-stu-id="e50f2-124">Applications supporting TAPI version 2.0 or later are sent a **LINE\_REMOVE** message.</span></span> <span data-ttu-id="e50f2-125">這會通知他們裝置已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="e50f2-125">This informs them that the device has been removed from the system.</span></span> <span data-ttu-id="e50f2-126">如果應用程式已開啟行，則在每個行控制碼上的行 **\_ 移除** 訊息前面會有 [**一行 \_ 關閉**](line-close.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="e50f2-126">The **LINE\_REMOVE** message is preceded by a [**LINE\_CLOSE**](line-close.md) message on each line handle, if the application had the line open.</span></span> <span data-ttu-id="e50f2-127">此訊息會傳送至所有支援 TAPI 2.0 版或更新版本的應用程式，這些應用程式已呼叫 [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)，包括當時沒有任何線路裝置開啟的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e50f2-127">This message is sent to all applications supporting TAPI version 2.0 or later that have called [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), including those that do not have any line devices open at the time.</span></span>

<span data-ttu-id="e50f2-128">較舊的應用程式會傳送 [**一行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息 \_ ，指定 LINEDEVSTATE 已移除，後面接著行 \_ 關閉訊息。</span><span class="sxs-lookup"><span data-stu-id="e50f2-128">Older applications are sent a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message specifying LINEDEVSTATE\_REMOVED, followed by a LINE\_CLOSE message.</span></span> <span data-ttu-id="e50f2-129">但是，這些較舊的應用程式不像 **行 \_ 移除** 訊息，只有在移除時有行開啟時，才可以接收這些訊息。</span><span class="sxs-lookup"><span data-stu-id="e50f2-129">Unlike the **LINE\_REMOVE** message, however, these older applications can receive these messages only if they have the line open when it is removed.</span></span> <span data-ttu-id="e50f2-130">如果它們沒有開啟的行，表示裝置已移除的唯一指示將會 \_ 在嘗試存取裝置時收到 LINEERR 的 NODEVICE 錯誤。</span><span class="sxs-lookup"><span data-stu-id="e50f2-130">If they do not have the line open, their only indication that the device was removed would be receiving a LINEERR\_NODEVICE error when they attempt to access the device.</span></span>

<span data-ttu-id="e50f2-131">移除裝置之後，依裝置識別碼存取裝置的任何嘗試都會導致 LINEERR \_ NODEVICE 錯誤。</span><span class="sxs-lookup"><span data-stu-id="e50f2-131">After a device has been removed, any attempt to access the device by its device identifier results in a LINEERR\_NODEVICE error.</span></span> <span data-ttu-id="e50f2-132">在所有 TAPI 應用程式都關機之後，重新開機 tapi 之後，當 TAPI 重新初始化時，移除的裝置就不再佔用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e50f2-132">After all TAPI applications have shutdown so that TAPI can restart, and when TAPI is reinitialized, the removed device no longer occupies a device identifier.</span></span>

> [!Note]  
> <span data-ttu-id="e50f2-133">執行：此為 TAPI 會傳回這個 LINEERR \_ NODEVICE; 從服務提供者收到 **行 \_ 移除** 訊息之後，就不會使用該線路裝置識別碼對該服務提供者進行進一步的呼叫。</span><span class="sxs-lookup"><span data-stu-id="e50f2-133">Implementation: it is TAPI that returns this LINEERR\_NODEVICE; after a **LINE\_REMOVE** message is received from a service provider; no further calls are made to that service provider using that line device identifier.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e50f2-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="e50f2-134">Requirements</span></span>



| <span data-ttu-id="e50f2-135">需求</span><span class="sxs-lookup"><span data-stu-id="e50f2-135">Requirement</span></span> | <span data-ttu-id="e50f2-136">值</span><span class="sxs-lookup"><span data-stu-id="e50f2-136">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e50f2-137">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="e50f2-137">TAPI version</span></span><br/> | <span data-ttu-id="e50f2-138">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e50f2-138">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e50f2-139">標頭</span><span class="sxs-lookup"><span data-stu-id="e50f2-139">Header</span></span><br/>       | <dl> <span data-ttu-id="e50f2-140"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="e50f2-140"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e50f2-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e50f2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e50f2-142">**行 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="e50f2-142">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="e50f2-143">**行 \_ LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="e50f2-143">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="e50f2-144">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="e50f2-144">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




