---
description: PNRP 使用 WSANSPIoctl 函式來接收有關下列變更的通知。
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP 和 WSANSPIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36dc53fb3d00eeaa2b74be643a7ea62af436e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969366"
---
# <a name="pnrp-and-wsanspioctl"></a><span data-ttu-id="6362d-103">PNRP 和 WSANSPIoctl</span><span class="sxs-lookup"><span data-stu-id="6362d-103">PNRP and WSANSPIoctl</span></span>

<span data-ttu-id="6362d-104">PNRP 使用 [**WSANSPIoctl**](winsock-nsp-reference-links.md) 函式來接收有關下列變更的通知：</span><span class="sxs-lookup"><span data-stu-id="6362d-104">PNRP uses the [**WSANSPIoctl**](winsock-nsp-reference-links.md) function to receive notifications about changes to the following:</span></span>

-   <span data-ttu-id="6362d-105">網路雲端清單</span><span class="sxs-lookup"><span data-stu-id="6362d-105">A network cloud list</span></span>
-   <span data-ttu-id="6362d-106">名稱解析要求的結果可用性</span><span class="sxs-lookup"><span data-stu-id="6362d-106">Availability of results of a name resolution request</span></span>

<span data-ttu-id="6362d-107">第一次呼叫 [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) 時，會定義用戶端收到通知的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="6362d-107">The first call to [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) defines the type of information that a client is notified about.</span></span> <span data-ttu-id="6362d-108">您可以使用 Windows 訊息、完成常式、WSAEVENT 物件的控制碼，或埠來通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="6362d-108">A client can be notified with a Windows message, a completion routine, a handle to a WSAEVENT object, or a port.</span></span> <span data-ttu-id="6362d-109">如需選項和設定 *lpCompletion* 參數的詳細資訊，請參閱 **WSANSPIoctl**。</span><span class="sxs-lookup"><span data-stu-id="6362d-109">For more information about options and setting the *lpCompletion* parameter, see **WSANSPIoctl**.</span></span>

<span data-ttu-id="6362d-110">若要在呼叫 [**WSALookupServiceNext**](winsock-nsp-reference-links.md)之後繼續接收通知，應用程式必須再次呼叫 **WSANSPIoctl** 。</span><span class="sxs-lookup"><span data-stu-id="6362d-110">To continue receiving notifications after a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md), an application must call **WSANSPIoctl** again.</span></span>

<span data-ttu-id="6362d-111">[**WSALookupServiceNext**](winsock-nsp-reference-links.md)函式會封鎖，即使呼叫 **WSANSPIoctl** 也是一樣。</span><span class="sxs-lookup"><span data-stu-id="6362d-111">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function blocks even if **WSANSPIoctl** is called.</span></span> <span data-ttu-id="6362d-112">在呼叫 **WSALookupServiceNext** 之前，應用程式必須等到收到通知（如果封鎖發生問題）。</span><span class="sxs-lookup"><span data-stu-id="6362d-112">Before calling **WSALookupServiceNext**, an application must wait until it receives a notification—if blocking is an issue.</span></span>

<span data-ttu-id="6362d-113">呼叫此函式時，參數必須具有下列值：</span><span class="sxs-lookup"><span data-stu-id="6362d-113">When calling this function, the parameters must have the following values:</span></span>

<dl> <dt>

<span data-ttu-id="6362d-114"><span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*hLookup*</span><span class="sxs-lookup"><span data-stu-id="6362d-114"><span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*hLookup*</span></span>
</dt> <dd>

<span data-ttu-id="6362d-115">指定 [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) 傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6362d-115">Specifies the handle that [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) returns.</span></span>

</dd> <dt>

<span data-ttu-id="6362d-116"><span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*</span><span class="sxs-lookup"><span data-stu-id="6362d-116"><span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*</span></span>
</dt> <dd>

<span data-ttu-id="6362d-117">必須是 **SIO 的 \_ NSP \_ 通知 \_ 變更**。</span><span class="sxs-lookup"><span data-stu-id="6362d-117">Must be **SIO\_NSP\_NOTIFY\_CHANGE**.</span></span>

</dd> <dt>

<span data-ttu-id="6362d-118"><span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*</span><span class="sxs-lookup"><span data-stu-id="6362d-118"><span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="6362d-119">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6362d-119">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6362d-120"><span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*</span><span class="sxs-lookup"><span data-stu-id="6362d-120"><span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="6362d-121">必須為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="6362d-121">Must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="6362d-122"><span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="6362d-122"><span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="6362d-123">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6362d-123">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6362d-124"><span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="6362d-124"><span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="6362d-125">必須為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="6362d-125">Must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="6362d-126"><span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="6362d-126"><span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*</span></span>
</dt> <dd>

<span data-ttu-id="6362d-127">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6362d-127">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6362d-128"><span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*</span><span class="sxs-lookup"><span data-stu-id="6362d-128"><span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*</span></span>
</dt> <dd>

<span data-ttu-id="6362d-129">指定 **Null** 或 [**WSACOMPLETION**](winsock-nsp-reference-links.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6362d-129">Specifies either **NULL** or a pointer to a [**WSACOMPLETION**](winsock-nsp-reference-links.md) structure.</span></span>

</dd> </dl>

<span data-ttu-id="6362d-130">收到通知之後，請呼叫 [**WSALookupServiceNext**](winsock-nsp-reference-links.md) 一次以取得結果。</span><span class="sxs-lookup"><span data-stu-id="6362d-130">After a notification is received, call [**WSALookupServiceNext**](winsock-nsp-reference-links.md) one time to obtain the results.</span></span>

<span data-ttu-id="6362d-131">若要結束搜尋，請呼叫 [**WSALookupServiceEnd**](winsock-nsp-reference-links.md)。</span><span class="sxs-lookup"><span data-stu-id="6362d-131">To end a search, call [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).</span></span>

## <a name="resolution-notifications"></a><span data-ttu-id="6362d-132">解決方案通知</span><span class="sxs-lookup"><span data-stu-id="6362d-132">Resolution Notifications</span></span>

<span data-ttu-id="6362d-133">每當新增名稱解析專案時，就可以通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="6362d-133">A client can be notified any time that a name resolution entry is added.</span></span> <span data-ttu-id="6362d-134">然後，用戶端會呼叫 [**WSALookupServiceNext**](winsock-nsp-reference-links.md) 來取得解析資料。</span><span class="sxs-lookup"><span data-stu-id="6362d-134">The client then calls [**WSALookupServiceNext**](winsock-nsp-reference-links.md) to obtain the resolution data.</span></span>

<span data-ttu-id="6362d-135">如果用戶端未使用這項技術，就可以封鎖對 [**WSALookupServiceNext**](winsock-nsp-reference-links.md) 的呼叫，直到指定的超時時間發生為止。</span><span class="sxs-lookup"><span data-stu-id="6362d-135">If the client does not use this technique, a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md) can be blocked until the specified timeout occurs.</span></span>

## <a name="cloud-list-notifications"></a><span data-ttu-id="6362d-136">雲端清單通知</span><span class="sxs-lookup"><span data-stu-id="6362d-136">Cloud List Notifications</span></span>

<span data-ttu-id="6362d-137">當一組雲端發生變更時，就可以通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="6362d-137">A client can be notified any time there is a change to a set of clouds.</span></span>

<span data-ttu-id="6362d-138">[**WSALookupServiceNext**](winsock-nsp-reference-links.md)函式會將 **WSA \_ E \_ NO \_ 其他** 傳回為 set 分隔符號。</span><span class="sxs-lookup"><span data-stu-id="6362d-138">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function returns **WSA\_E\_NO\_MORE** as a set delimiter.</span></span> <span data-ttu-id="6362d-139">用戶端應用程式必須列舉現有的雲端，才會傳回此訊息，然後使用通知配置來取出後續變更。</span><span class="sxs-lookup"><span data-stu-id="6362d-139">The client application must enumerate existing clouds until this message is returned, and then use a notification scheme to retrieve subsequent changes as they occur.</span></span> <span data-ttu-id="6362d-140">用戶端應用程式也可以呼叫 **WSALookupServiceNext**，但呼叫會被封鎖，直到發生變更為止。</span><span class="sxs-lookup"><span data-stu-id="6362d-140">A client application can also call **WSALookupServiceNext**, but the call is blocked until a change occurs.</span></span>

<span data-ttu-id="6362d-141">[**WSALookupServiceNext**](winsock-nsp-reference-links.md)函數會傳回 **WSAQUERYSET** 結構中的雲端。</span><span class="sxs-lookup"><span data-stu-id="6362d-141">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function returns a cloud in a **WSAQUERYSET** structure.</span></span> <span data-ttu-id="6362d-142">**DwOutputFlags** 成員中會傳回下列其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="6362d-142">One of the following flags is returned in the **dwOutputFlags** member.</span></span>



| <span data-ttu-id="6362d-143">值</span><span class="sxs-lookup"><span data-stu-id="6362d-143">Value</span></span>               | <span data-ttu-id="6362d-144">描述</span><span class="sxs-lookup"><span data-stu-id="6362d-144">Description</span></span>                                             |
|---------------------|---------------------------------------------------------|
| <span data-ttu-id="6362d-145">\_已 \_ 新增結果</span><span class="sxs-lookup"><span data-stu-id="6362d-145">RESULT\_IS\_ADDED</span></span>   | <span data-ttu-id="6362d-146">已新增傳回的雲端。</span><span class="sxs-lookup"><span data-stu-id="6362d-146">The cloud that is returned is added.</span></span>                    |
| <span data-ttu-id="6362d-147">結果 \_ 已 \_ 變更</span><span class="sxs-lookup"><span data-stu-id="6362d-147">RESULT\_IS\_CHANGED</span></span> | <span data-ttu-id="6362d-148">傳回的雲端已變更。</span><span class="sxs-lookup"><span data-stu-id="6362d-148">The cloud that is returned is changed.</span></span>                  |
| <span data-ttu-id="6362d-149">結果 \_ 已 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="6362d-149">RESULT\_IS\_DELETED</span></span> | <span data-ttu-id="6362d-150">傳回的雲端已刪除且無效。</span><span class="sxs-lookup"><span data-stu-id="6362d-150">The cloud that is returned is deleted and is not valid.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6362d-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="6362d-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6362d-152">PNRP 和 WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="6362d-152">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="6362d-153">PNRP 和 WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="6362d-153">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="6362d-154">PNRP 和 WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="6362d-154">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="6362d-155">PNRP NSP 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="6362d-155">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="6362d-156">**WSANSPIoctl**</span><span class="sxs-lookup"><span data-stu-id="6362d-156">**WSANSPIoctl**</span></span>](winsock-nsp-reference-links.md)
</dt> <dt>

<span data-ttu-id="6362d-157">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="6362d-157">**WSALookupServiceBegin**</span></span>
</dt> <dt>

<span data-ttu-id="6362d-158">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="6362d-158">**WSALookupServiceEnd**</span></span>
</dt> <dt>

<span data-ttu-id="6362d-159">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="6362d-159">**WSAQUERYSET**</span></span>
</dt> </dl>

 

 



