---
description: NLA 能夠為其用戶端提供網路位置變更的通知。 用來要求變更事件通知的機制是 WSALookupServiceBegin、WSANSPIoctl 和 WSALookupServiceNext 函數的組合。
ms.assetid: fed5a90d-0bc5-46e7-b3d3-edc4b303d305
title: 來自 NLA 的通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ee0ad0530725db27c8f5df39b6fc573f7e97c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511412"
---
# <a name="notification-from-nla"></a><span data-ttu-id="112b8-104">來自 NLA 的通知</span><span class="sxs-lookup"><span data-stu-id="112b8-104">Notification from NLA</span></span>

<span data-ttu-id="112b8-105">NLA 能夠為其用戶端提供網路位置變更的通知。</span><span class="sxs-lookup"><span data-stu-id="112b8-105">NLA is capable of providing its clients with notification of network location changes.</span></span> <span data-ttu-id="112b8-106">用來要求變更事件通知的機制是 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)、 [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl)和 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) 函數的組合。</span><span class="sxs-lookup"><span data-stu-id="112b8-106">The mechanism used to request notification of change events is a combination of the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl), and [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) functions.</span></span>

<span data-ttu-id="112b8-107">為了接收來自 NLA 的變更通知，用戶端必須先呼叫 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) 來取得有效的 NLA SP 查閱控制碼。</span><span class="sxs-lookup"><span data-stu-id="112b8-107">In order to receive change notification from NLA, a client must first call the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) to obtain a valid NLA SP lookup handle.</span></span> <span data-ttu-id="112b8-108">接下來，用戶端可以依任何順序呼叫 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)或 [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) ;若要註冊通知，請呼叫 **WSANSPIoctl** 函式，並 \_ \_ 在 DWCONTROLCODE 參數中以 SIO 的 NSP 通知 \_ 變更控制程式碼集。 </span><span class="sxs-lookup"><span data-stu-id="112b8-108">Next, the client can call [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) or [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) in any order; to register for notification, call the **WSANSPIoctl** function with the SIO\_NSP\_NOTIFY\_CHANGE control code set in the *dwControlCode* parameter.</span></span>

<span data-ttu-id="112b8-109">[**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)函式會 \_ 將 WSA E \_ NO 其他傳回 \_ 為 set 分隔符號。</span><span class="sxs-lookup"><span data-stu-id="112b8-109">The [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) function returns WSA\_E\_NO\_MORE as a set delimiter.</span></span> <span data-ttu-id="112b8-110">當用戶端已使用 [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) 函式註冊通知，而 **WSALookupServiceNext** 傳回 \_ 不超過的 WSA E 時 \_ \_ ，再次呼叫 **WSALookupServiceNext** 會顯示是否發生變更：</span><span class="sxs-lookup"><span data-stu-id="112b8-110">When a client has registered for notification using the [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) function and **WSALookupServiceNext** returns WSA\_E\_NO\_MORE, calling **WSALookupServiceNext** again reveals whether a change has occurred:</span></span>

-   <span data-ttu-id="112b8-111">如果自先前的 WSA e 起未發生任何變更 \_ \_ \_ ，則不 \_ 會再傳回 WSA e \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="112b8-111">If no changes have occurred since the previous WSA\_E\_NO\_MORE, WSA\_E\_NO\_MORE is returned.</span></span>
-   <span data-ttu-id="112b8-112">如果發生變更，或是發生了變更並進行輪詢呼叫， [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) 函式呼叫會將網路傳回為 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 結構，並在其 **dwOutputFlags** 成員中設定下列其中一個旗標：</span><span class="sxs-lookup"><span data-stu-id="112b8-112">If a change has occurred, or if a change has occurred and a polling call is made, the [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) function call returns networks as [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structures, with one of the following flags set in its **dwOutputFlags** member:</span></span>

    <dl> <span data-ttu-id="112b8-113">\_已 \_ 新增結果</span><span class="sxs-lookup"><span data-stu-id="112b8-113">RESULT\_IS\_ADDED</span></span>  
    <span data-ttu-id="112b8-114">結果 \_ 已 \_ 變更</span><span class="sxs-lookup"><span data-stu-id="112b8-114">RESULT\_IS\_CHANGED</span></span>  
    <span data-ttu-id="112b8-115">結果 \_ 已 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="112b8-115">RESULT\_IS\_DELETED</span></span>  
    </dl>

<span data-ttu-id="112b8-116">針對已變更的任何欄位，會提供變更通知，因為使用 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) 函式呼叫取得 NLA 查閱控制碼，或自最後一個列舉產生 WSA \_ E \_ 沒有 \_ 其他錯誤。</span><span class="sxs-lookup"><span data-stu-id="112b8-116">Change notification is provided for any fields that changed since the NLA lookup handle was obtained with the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function call, or since the last enumeration that resulted in the WSA\_E\_NO\_MORE error.</span></span> <span data-ttu-id="112b8-117">提供所有已變更的網路位置資訊時， \_ 不 \_ 會再傳回 WSA E \_ 。</span><span class="sxs-lookup"><span data-stu-id="112b8-117">When all changed network location information is provided, WSA\_E\_NO\_MORE is returned.</span></span> <span data-ttu-id="112b8-118">用戶端可以在任何時間（一次一個）重新發出相同查詢控制碼上的 [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) 函式呼叫，並 \_ 設定 SIO 的 NSP \_ 通知 \_ 變更旗標。</span><span class="sxs-lookup"><span data-stu-id="112b8-118">Clients can reissue a [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) function call on the same query handle at any time, one at a time, with the SIO\_NSP\_NOTIFY\_CHANGE flag set.</span></span> <span data-ttu-id="112b8-119">這項功能可讓用戶端持續回收查詢控制碼，藉此讓用戶端不需要自行維護變更狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="112b8-119">This capability enables a client to recycle the query handle on an ongoing basis, thereby relieving the client from having to maintain change-state information on its own.</span></span> <span data-ttu-id="112b8-120">一旦用戶端不再需要變更通知，就應該使用 [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) 函式來關閉查詢控制碼。</span><span class="sxs-lookup"><span data-stu-id="112b8-120">Once a client no longer needs change notifications, it should close the query handle using the [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) function.</span></span>

 

 



