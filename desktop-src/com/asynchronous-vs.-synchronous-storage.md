---
title: 非同步和同步儲存體
description: 非同步和同步儲存體
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884b8613bebf8ef401f76e4761f48fa0ddd831c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104508163"
---
# <a name="asynchronous-and-synchronous-storage"></a><span data-ttu-id="c4567-103">非同步和同步儲存體</span><span class="sxs-lookup"><span data-stu-id="c4567-103">Asynchronous and Synchronous Storage</span></span>

<span data-ttu-id="c4567-104">非同步名字可能也會傳回 [**IBindStatusCallback：： OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))通知中的 [非同步儲存](/windows/desktop/Stg/asynchronous-storage)物件。</span><span class="sxs-lookup"><span data-stu-id="c4567-104">Asynchronous monikers may also return an [Asynchronous Storage](/windows/desktop/Stg/asynchronous-storage) object in the [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) notification.</span></span> <span data-ttu-id="c4567-105">當系結仍在進行時，這個儲存物件可能會允許存取某些物件的持續性資料。</span><span class="sxs-lookup"><span data-stu-id="c4567-105">This storage object may allow access to some of the object's persistent data while the binding is still in progress.</span></span> <span data-ttu-id="c4567-106">用戶端可以選擇兩種儲存模式：封鎖和非封鎖。</span><span class="sxs-lookup"><span data-stu-id="c4567-106">A client can choose between two modes for the storage: blocking and nonblocking.</span></span>

<span data-ttu-id="c4567-107">在封鎖模式中，如果資料無法使用，則呼叫會封鎖，直到資料到達為止。</span><span class="sxs-lookup"><span data-stu-id="c4567-107">In blocking mode, which is compatible with current implementations of storage objects, if data is unavailable, the call blocks until data arrives.</span></span> <span data-ttu-id="c4567-108">在非封鎖模式中，儲存物件不會封鎖呼叫，而是在 \_ 資料無法使用時，傳回新的錯誤 E。</span><span class="sxs-lookup"><span data-stu-id="c4567-108">In nonblocking mode, rather than blocking the call, the storage object returns a new error E\_PENDING when data is unavailable.</span></span> <span data-ttu-id="c4567-109">用戶端注意到非同步系結和儲存體會記下此錯誤，並等候進一步的通知 ([**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) 重試作業。</span><span class="sxs-lookup"><span data-stu-id="c4567-109">A client aware of asynchronous binding and storage notes this error and waits for further notifications ([**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) to retry the operation.</span></span> <span data-ttu-id="c4567-110">用戶端可以選擇是否要 \_ 在傳回 [**IBindStatusCallback：： GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85))的 *GRFBINDF* 值中設定 BINDF ASYNCSTORAGE 旗標，以在同步 (封鎖) 和非同步 (非封鎖) 儲存體之間選擇。</span><span class="sxs-lookup"><span data-stu-id="c4567-110">A client can choose between a synchronous (blocking) and asynchronous (nonblocking) storage by choosing whether to set the BINDF\_ASYNCSTORAGE flag in the *grfBINDF* value returned to [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4567-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4567-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4567-112">非同步名字</span><span class="sxs-lookup"><span data-stu-id="c4567-112">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 