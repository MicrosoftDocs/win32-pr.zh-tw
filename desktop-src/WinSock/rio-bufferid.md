---
description: 指定搭配 Winsock 註冊的 i/o 擴充功能使用的已註冊緩衝區描述元。
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: 'RIO_BUFFERID (Mswsockdef) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75bb439a567c361a056b750728d986891a1da468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026499"
---
# <a name="rio_bufferid"></a><span data-ttu-id="b3d9e-103">RIO \_ BUFFERID</span><span class="sxs-lookup"><span data-stu-id="b3d9e-103">RIO\_BUFFERID</span></span>

<span data-ttu-id="b3d9e-104">**RIO \_ BUFFERID** typedef 會指定搭配 Winsock 註冊之 i/o 延伸模組使用的已註冊緩衝區描述元。</span><span class="sxs-lookup"><span data-stu-id="b3d9e-104">The **RIO\_BUFFERID** typedef specifies a registered buffer descriptor used with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

<span data-ttu-id="b3d9e-105">**RIO \_ BUFFERID**</span><span class="sxs-lookup"><span data-stu-id="b3d9e-105">**RIO\_BUFFERID**</span></span>
</dt> <dd>

<span data-ttu-id="b3d9e-106">資料類型，指定與傳送和接收要求搭配使用的已註冊緩衝區描述元。</span><span class="sxs-lookup"><span data-stu-id="b3d9e-106">A data type that specifies a registered buffer descriptor used with send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3d9e-107">備註</span><span class="sxs-lookup"><span data-stu-id="b3d9e-107">Remarks</span></span>

<span data-ttu-id="b3d9e-108">Winsock 註冊的 i/o 擴充功能主要是在使用 **RIO \_ BUFFERID** 物件的已註冊緩衝區上運作。</span><span class="sxs-lookup"><span data-stu-id="b3d9e-108">The Winsock registered I/O extensions operate primarily on registered buffers using **RIO\_BUFFERID** objects.</span></span> <span data-ttu-id="b3d9e-109">應用程式會使用 [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))函數取得現有緩衝區的 **RIO \_ BUFFERID** 。</span><span class="sxs-lookup"><span data-stu-id="b3d9e-109">An application obtains a **RIO\_BUFFERID** for an existing buffer using the [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) function.</span></span> <span data-ttu-id="b3d9e-110">應用程式可以使用 [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) 函式釋放註冊。</span><span class="sxs-lookup"><span data-stu-id="b3d9e-110">An application can release a registration using the [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) function.</span></span>

<span data-ttu-id="b3d9e-111">使用 [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))函式將現有的緩衝區註冊為 **RIO \_ BUFFERID** 物件時，會從實體記憶體配置特定的內部資源，而現有的應用程式緩衝區將會鎖定到實體記憶體中。</span><span class="sxs-lookup"><span data-stu-id="b3d9e-111">When an existing buffer is registered as a **RIO\_BUFFERID** object using the [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) function, certain internal resources are allocated from physical memory, and the existing application buffer will be locked into physical memory.</span></span> <span data-ttu-id="b3d9e-112">[**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)函式會被呼叫以取消註冊緩衝區、釋放這些內部資源，並允許將緩衝區解除鎖定並從實體記憶體釋放。</span><span class="sxs-lookup"><span data-stu-id="b3d9e-112">The [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) function is called to deregister the buffer, free these internal resources, and allow the buffer to be unlocked and released from physical memory.</span></span>

<span data-ttu-id="b3d9e-113">使用 Winsock 註冊的 i/o 擴充功能，重複註冊和解除登錄應用程式緩衝區可能會造成顯著的效能降低。</span><span class="sxs-lookup"><span data-stu-id="b3d9e-113">Repeated registration and deregistration of application buffers using the Winsock registered I/O extensions may cause significant performance degradation.</span></span> <span data-ttu-id="b3d9e-114">使用 Winsock 註冊的 i/o 擴充功能來設計應用程式時，應考慮下列緩衝區管理方法，以將應用程式緩衝區的重複註冊和解除登錄降至最低：</span><span class="sxs-lookup"><span data-stu-id="b3d9e-114">The following buffer management approaches should be considered when designing an application using the Winsock registered I/O extensions to minimize repeated registration and deregistration of application buffers:</span></span>

-   <span data-ttu-id="b3d9e-115">•最大化重複使用緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b3d9e-115">• Maximize the reuse of buffers.</span></span>
-   <span data-ttu-id="b3d9e-116">•維護受限的未使用已註冊緩衝區集區，以供應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="b3d9e-116">• Maintain a limited pool of unused registered buffers for use by the application.</span></span>
-   <span data-ttu-id="b3d9e-117">•維護受限的已註冊緩衝區集區，並在這些已註冊的緩衝區和其他未註冊的緩衝區之間執行緩衝區複製。</span><span class="sxs-lookup"><span data-stu-id="b3d9e-117">• Maintain a limited pool of registered buffers and perform buffer copies between these registered buffers and other unregistered buffers.</span></span>

<span data-ttu-id="b3d9e-118">**RIO \_ BUFFERID** typedef 會定義在 *Mswsockdef .h* 標頭檔中，該檔案會自動包含在 *Mswsock. .h* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="b3d9e-118">The **RIO\_BUFFERID** typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="b3d9e-119">不應直接使用 *Mswsockdef* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="b3d9e-119">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3d9e-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3d9e-120">Requirements</span></span>



| <span data-ttu-id="b3d9e-121">需求</span><span class="sxs-lookup"><span data-stu-id="b3d9e-121">Requirement</span></span> | <span data-ttu-id="b3d9e-122">值</span><span class="sxs-lookup"><span data-stu-id="b3d9e-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d9e-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3d9e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b3d9e-124">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3d9e-124">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="b3d9e-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3d9e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b3d9e-126">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3d9e-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="b3d9e-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b3d9e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3d9e-128"><dt>Mswsockdef (包含 Mswsock) </dt></span><span class="sxs-lookup"><span data-stu-id="b3d9e-128"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3d9e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3d9e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3d9e-130">**RIO \_ BUF**</span><span class="sxs-lookup"><span data-stu-id="b3d9e-130">**RIO\_BUF**</span></span>](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
</dt> <dt>

[<span data-ttu-id="b3d9e-131">**RIODeregisterBuffer**</span><span class="sxs-lookup"><span data-stu-id="b3d9e-131">**RIODeregisterBuffer**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)
</dt> <dt>

[<span data-ttu-id="b3d9e-132">**RIOReceive**</span><span class="sxs-lookup"><span data-stu-id="b3d9e-132">**RIOReceive**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[<span data-ttu-id="b3d9e-133">**RIOReceiveEx**</span><span class="sxs-lookup"><span data-stu-id="b3d9e-133">**RIOReceiveEx**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

<span data-ttu-id="b3d9e-134">[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b3d9e-134">[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b3d9e-135">**RIOSend**</span><span class="sxs-lookup"><span data-stu-id="b3d9e-135">**RIOSend**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

<span data-ttu-id="b3d9e-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b3d9e-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span></span>
</dt> </dl>

 

 
