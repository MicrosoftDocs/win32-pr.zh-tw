---
description: 指定傳送和接收要求與 Winsock 註冊的 i/o 擴充功能所使用的通訊端描述項。
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: 'RIO_RQ (Mswsockdef) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25abebbe40842532f3cca180868b5b3786e756d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318872"
---
# <a name="rio_rq"></a><span data-ttu-id="49336-103">RIO \_ RQ</span><span class="sxs-lookup"><span data-stu-id="49336-103">RIO\_RQ</span></span>

<span data-ttu-id="49336-104">**RIO \_ RQ** typedef 會指定傳送和接收要求所使用的通訊端描述項，以及 Winsock 註冊的 i/o 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="49336-104">The **RIO\_RQ** typedef specifies a socket descriptor used by send and receive requests with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

<span data-ttu-id="49336-105">**RIO \_ RQ**</span><span class="sxs-lookup"><span data-stu-id="49336-105">**RIO\_RQ**</span></span>
</dt> <dd>

<span data-ttu-id="49336-106">一種資料類型，可指定傳送和接收要求所使用的通訊端描述項。</span><span class="sxs-lookup"><span data-stu-id="49336-106">A data type that specifies a socket descriptor used by send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49336-107">備註</span><span class="sxs-lookup"><span data-stu-id="49336-107">Remarks</span></span>

<span data-ttu-id="49336-108">Winsock 註冊的 i/o 擴充功能主要是在 **RIO \_ RQ** 物件上運作，而不是通訊端。</span><span class="sxs-lookup"><span data-stu-id="49336-108">The Winsock registered I/O extensions operate primarily on a **RIO\_RQ** object rather than a socket.</span></span> <span data-ttu-id="49336-109">應用程式會使用 [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)函數取得現有通訊端的 **RIO \_ RQ** 。</span><span class="sxs-lookup"><span data-stu-id="49336-109">An application obtains a **RIO\_RQ** for an existing socket using the [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) function.</span></span> <span data-ttu-id="49336-110">您必須使用 *dwFlags* 參數中所設定的 **WSA \_ 旗標 \_ RIO** 旗標來呼叫 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)函式，以建立輸入通訊端。</span><span class="sxs-lookup"><span data-stu-id="49336-110">The input socket must have been created by calling the [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) function with the **WSA\_FLAG\_RIO** flag set in the *dwFlags* parameter.</span></span>

<span data-ttu-id="49336-111">取得 **RIO \_ RQ** 物件之後，基礎通訊端描述項會保持有效。</span><span class="sxs-lookup"><span data-stu-id="49336-111">After obtaining a **RIO\_RQ** object, the underlying socket descriptor remains valid.</span></span> <span data-ttu-id="49336-112">應用程式可能會繼續使用基礎通訊端來設定和查詢通訊端選項、發出 IOCTLs，最後關閉通訊端。</span><span class="sxs-lookup"><span data-stu-id="49336-112">An application may continue to use the underlying socket to set and query socket options, issue IOCTLs and ultimately close the socket.</span></span>

> [!Note]  
> <span data-ttu-id="49336-113">基於效率的目的， ([**RIO \_ CQ**](riocqueue.md) 結構) 和要求佇列 (**RIO \_ RQ** 結構) 不會受到同步處理原始物件的保護，因此可存取完成佇列。</span><span class="sxs-lookup"><span data-stu-id="49336-113">For purposes of efficiency, access to the completion queues ([**RIO\_CQ**](riocqueue.md) structs) and request queues (**RIO\_RQ** structs) are not protected by synchronization primitives.</span></span> <span data-ttu-id="49336-114">如果您需要從多個執行緒存取完成或要求佇列，存取應由重要區段、精簡型讀取器寫入鎖定或類似的機制進行協調。</span><span class="sxs-lookup"><span data-stu-id="49336-114">If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism.</span></span> <span data-ttu-id="49336-115">單一線程不需要此鎖定即可進行存取。</span><span class="sxs-lookup"><span data-stu-id="49336-115">This locking is not needed for access by a single thread.</span></span> <span data-ttu-id="49336-116">不同的執行緒可以存取個別的要求/完成佇列，而不需要鎖定。</span><span class="sxs-lookup"><span data-stu-id="49336-116">Different threads can access separate requests/completion queues without locks.</span></span> <span data-ttu-id="49336-117">只有當多個執行緒嘗試存取相同的佇列時，才會發生同步處理的需求。</span><span class="sxs-lookup"><span data-stu-id="49336-117">The need for synchronization occurs only when multiple threads try to access the same queue.</span></span> <span data-ttu-id="49336-118">如果多個執行緒發出相同通訊端上的傳送和接收，則也需要同步處理，因為傳送和接收作業會使用通訊端的要求佇列。</span><span class="sxs-lookup"><span data-stu-id="49336-118">Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.</span></span>

 

<span data-ttu-id="49336-119">[**RIO \_ RQ**](riocqueue.md) typedef 會定義在 *Mswsockdef .h* 標頭檔中，該檔案會自動包含在 *Mswsock. .h* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="49336-119">The [**RIO\_RQ**](riocqueue.md) typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="49336-120">不應直接使用 *Mswsockdef* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="49336-120">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="49336-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="49336-121">Requirements</span></span>



| <span data-ttu-id="49336-122">需求</span><span class="sxs-lookup"><span data-stu-id="49336-122">Requirement</span></span> | <span data-ttu-id="49336-123">值</span><span class="sxs-lookup"><span data-stu-id="49336-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49336-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49336-124">Minimum supported client</span></span><br/> | <span data-ttu-id="49336-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49336-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="49336-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49336-126">Minimum supported server</span></span><br/> | <span data-ttu-id="49336-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49336-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="49336-128">標頭</span><span class="sxs-lookup"><span data-stu-id="49336-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="49336-129"><dt>Mswsockdef (包含 Mswsock) </dt></span><span class="sxs-lookup"><span data-stu-id="49336-129"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49336-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49336-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49336-131">**RIOCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="49336-131">**RIOCreateRequestQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[<span data-ttu-id="49336-132">**RIOReceive**</span><span class="sxs-lookup"><span data-stu-id="49336-132">**RIOReceive**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[<span data-ttu-id="49336-133">**RIOReceiveEx**</span><span class="sxs-lookup"><span data-stu-id="49336-133">**RIOReceiveEx**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

<span data-ttu-id="49336-134">[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="49336-134">[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="49336-135">**RIOSend**</span><span class="sxs-lookup"><span data-stu-id="49336-135">**RIOSend**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

<span data-ttu-id="49336-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="49336-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="49336-137">**WSASocket**</span><span class="sxs-lookup"><span data-stu-id="49336-137">**WSASocket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
</dt> </dl>

 

 
