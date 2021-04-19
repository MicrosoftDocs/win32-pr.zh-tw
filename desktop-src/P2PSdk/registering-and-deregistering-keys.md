---
description: 註冊和取消註冊金鑰
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: 註冊和取消註冊金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009ee41e85027ff8eba3f6869359a9ba304f4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978266"
---
# <a name="registering-and-deregistering-keys"></a><span data-ttu-id="fe720-103">註冊和取消註冊金鑰</span><span class="sxs-lookup"><span data-stu-id="fe720-103">Registering and Deregistering Keys</span></span>

## <a name="registering-keys"></a><span data-ttu-id="fe720-104">註冊金鑰</span><span class="sxs-lookup"><span data-stu-id="fe720-104">Registering Keys</span></span>

<span data-ttu-id="fe720-105">節點可以隨時在 **drt \_ 主動**、drt 和 **drt \_ 沒有 \_ 網路** 狀態的情況 **下 \_**，向 [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey)註冊金鑰。</span><span class="sxs-lookup"><span data-stu-id="fe720-105">A node can register keys with [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) at anytime while in the **DRT\_ACTIVE**, **DRT\_ALONE**, and **DRT\_NO\_NETWORK** states.</span></span> <span data-ttu-id="fe720-106">只有在本機節點 **轉換為「使用中」 \_** 之後，其他 DRTs 才可辨識已在 drt 中登錄的金鑰，且不會有 **\_ 任何 \_ 網路** 狀態。 **\_**</span><span class="sxs-lookup"><span data-stu-id="fe720-106">Keys registered in **DRT\_ALONE** and **DRT\_NO\_NETWORK** states can only be recognized by other DRTs after the local node has transitioned to **DRT\_ACTIVE**.</span></span>

<span data-ttu-id="fe720-107">使用 [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider)時，不能在相同的 DRT 實例內註冊相同的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fe720-107">Identical keys cannot be registered within the same DRT instance when using [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider).</span></span> <span data-ttu-id="fe720-108">如果嘗試註冊相同的金鑰，則第二個金鑰的註冊將會失敗。</span><span class="sxs-lookup"><span data-stu-id="fe720-108">If the registration of identical keys is attempted, the registration of the second key will fail.</span></span> <span data-ttu-id="fe720-109">使用相同的金鑰也應避免不同的 DRT 實例之間使用。</span><span class="sxs-lookup"><span data-stu-id="fe720-109">The use of identical keys should also be avoided between different DRT instances.</span></span> <span data-ttu-id="fe720-110">搜尋唯一索引鍵的指定，這些相同的金鑰共用可能會傳回任何一個索引鍵，而不管與索引鍵相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="fe720-110">Searches against the unique key designation these identical keys share could return any one of the keys, regardless of what data is associated to the key.</span></span>

> [!Note]  
> <span data-ttu-id="fe720-111">如果執行時需要不同的行為，則可以建立安全性提供者來取代 [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) 以容納。</span><span class="sxs-lookup"><span data-stu-id="fe720-111">If different behavior is required for implementation, a security provider can be created in place of [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) to accommodate.</span></span>

 

## <a name="deregistering-keys"></a><span data-ttu-id="fe720-112">取消註冊金鑰</span><span class="sxs-lookup"><span data-stu-id="fe720-112">Deregistering Keys</span></span>

<span data-ttu-id="fe720-113">節點註冊之後，即可隨時取消註冊金鑰。</span><span class="sxs-lookup"><span data-stu-id="fe720-113">A node can deregister a key anytime after it has been registered.</span></span> <span data-ttu-id="fe720-114">不過，只有註冊金鑰的應用程式可以將它取消註冊。</span><span class="sxs-lookup"><span data-stu-id="fe720-114">However, only the application that registered the key can deregister it.</span></span> <span data-ttu-id="fe720-115">應用程式可以使用 [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) 函數，從本機節點取消註冊金鑰。</span><span class="sxs-lookup"><span data-stu-id="fe720-115">An application can deregister a key from the local node using the [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) function.</span></span> <span data-ttu-id="fe720-116">完成時，此函式會觸發 **DRT \_ 事件 \_ LEAFSET \_ 金鑰 \_ 變更** 事件; 通知應用程式，以及參與 DRT 網狀的其他節點。</span><span class="sxs-lookup"><span data-stu-id="fe720-116">Upon completion the function triggers a **DRT\_EVENT\_LEAFSET\_KEY\_CHANGE** event; informing the application as well as other nodes participating in the DRT mesh.</span></span>

<span data-ttu-id="fe720-117">在 Drt 發生 **錯誤 \_** 狀態時，所需的 [**DRTCLOSE**](/windows/desktop/api/drt/nf-drt-drtclose) 呼叫會導致 DRT 基礎結構將所有金鑰取消註冊。</span><span class="sxs-lookup"><span data-stu-id="fe720-117">While in the **DRT\_FAULTED** state, the required call of [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) will result in the DRT infrastructure deregistering all keys.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe720-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="fe720-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe720-119">搜尋分散式路由表</span><span class="sxs-lookup"><span data-stu-id="fe720-119">Searching a Distributed Routing Table</span></span>](searching-a-distributed-routing-table.md)
</dt> <dt>

[<span data-ttu-id="fe720-120">關於分散式路由表</span><span class="sxs-lookup"><span data-stu-id="fe720-120">About Distributed Routing Tables</span></span>](about-distributed-routing-tables.md)
</dt> <dt>

[<span data-ttu-id="fe720-121">分散式路由資料表 API 參考</span><span class="sxs-lookup"><span data-stu-id="fe720-121">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



