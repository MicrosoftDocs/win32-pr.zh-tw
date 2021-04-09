---
title: 服務如何撰寫其 Spn
description: 服務可以使用兩個函式來撰寫其 Spn DsGetSpn 是用來撰寫 Spn 的一般用途函式，而 DsServerRegisterSpn 則是專門用來撰寫及註冊主機服務之簡單 Spn 的特殊函式。
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- 服務主體名稱 AD，服務的組合方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5611527cc3c240eebc195058ce39daab71aeef23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839312"
---
# <a name="how-a-service-composes-its-spns"></a><span data-ttu-id="0f4d8-104">服務如何撰寫其 Spn</span><span class="sxs-lookup"><span data-stu-id="0f4d8-104">How a Service Composes its SPNs</span></span>

<span data-ttu-id="0f4d8-105">服務可以使用兩個函式來撰寫其 Spn： [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) 是用來撰寫 spn 的一般用途函式，而 [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) 則是專門用來撰寫和註冊主機服務之簡單 spn 的特殊函式。</span><span class="sxs-lookup"><span data-stu-id="0f4d8-105">A service can use two functions to compose its SPNs: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) is a general-purpose function for composing SPNs and [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) is a specialized function for composing and registering simple SPNs for a host-based service.</span></span>

<span data-ttu-id="0f4d8-106">服務安裝程式通常會使用 [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) 函式來撰寫 spn，然後使用 [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) 函數來註冊服務的登入帳戶。</span><span class="sxs-lookup"><span data-stu-id="0f4d8-106">A service installer typically uses the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to compose SPNs, which it then registers on the service's logon account using the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function.</span></span> <span data-ttu-id="0f4d8-107">**DsGetSpn** 可執行下列功能。</span><span class="sxs-lookup"><span data-stu-id="0f4d8-107">The **DsGetSpn** can perform the following functions.</span></span>

-   <span data-ttu-id="0f4d8-108">使用 " <service class> / <host> " 格式來建立以主機為基礎的服務的簡單 SPN。</span><span class="sxs-lookup"><span data-stu-id="0f4d8-108">Create a simple SPN with the "<service class>/<host>" format for a host-based service.</span></span>
-   <span data-ttu-id="0f4d8-109">建立包含可複製服務所使用之「服務名稱」元件的複雜 SPN， &lt; &gt; 或在 &lt; &gt; 單一主機上區分服務之多個實例的「埠」元件。</span><span class="sxs-lookup"><span data-stu-id="0f4d8-109">Create a complex SPN that includes the "&lt;service name&gt;" component used by replicable services or the "&lt;port&gt;" component that distinguishes multiple instances of a service on a single host.</span></span>
-   <span data-ttu-id="0f4d8-110">建立單一 SPN，並將 " &lt; host &gt; " 元件設定為指定主機的名稱，或預設為本機電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f4d8-110">Create a single SPN with the "&lt;host&gt;" component set to either the name of a specified host or the name of the local computer by default.</span></span>
-   <span data-ttu-id="0f4d8-111">針對將在整個樹系的多部主機上執行的多個服務實例，建立 Spn 的陣列。</span><span class="sxs-lookup"><span data-stu-id="0f4d8-111">Create an array of SPNs for multiple service instances that will run on multiple hosts throughout the forest.</span></span> <span data-ttu-id="0f4d8-112">每個 SPN 都會指定服務實例的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="0f4d8-112">Each SPN specifies the name of the host for a service instance.</span></span>
-   <span data-ttu-id="0f4d8-113">針對將在相同主機上執行的多個服務實例，建立 Spn 的陣列。</span><span class="sxs-lookup"><span data-stu-id="0f4d8-113">Create an array of SPNs for multiple service instances that will run on the same host.</span></span> <span data-ttu-id="0f4d8-114">每個 SPN 都會指定主機的名稱，以及服務實例的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="0f4d8-114">Each SPN specifies the name of the host and a port number for a service instance.</span></span>

<span data-ttu-id="0f4d8-115">[**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna)傳回的名稱陣列必須藉由呼叫 [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya)函數來釋出。</span><span class="sxs-lookup"><span data-stu-id="0f4d8-115">The array of names returned by [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) must be freed by calling the [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) function.</span></span>

<span data-ttu-id="0f4d8-116">請注意， [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna)、 [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)和 [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) 函式不會驗證 spn 是否是唯一的。</span><span class="sxs-lookup"><span data-stu-id="0f4d8-116">Be aware that the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna), and [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) functions do not verify that SPNs are unique.</span></span> <span data-ttu-id="0f4d8-117">因為如果用戶端出示的 SPN 不是唯一的，所以相互驗證會失敗，請在註冊 SPN 之前確認唯一性。</span><span class="sxs-lookup"><span data-stu-id="0f4d8-117">Because mutual authentication fails if a client presents an SPN that is not unique, verify uniqueness before registering an SPN.</span></span> <span data-ttu-id="0f4d8-118">若要這樣做，請針對符合您 SPN 的 **servicePrincipalName** 屬性，搜尋通用類別目錄 (GC) 。</span><span class="sxs-lookup"><span data-stu-id="0f4d8-118">To do this, search the global catalog (GC) for **servicePrincipalName** attributes that match your SPN.</span></span> <span data-ttu-id="0f4d8-119">如需有關搜尋 GC 的詳細資訊，請參閱 [搜尋通用類別目錄](searching-global-catalog-contents.md)。</span><span class="sxs-lookup"><span data-stu-id="0f4d8-119">For more information about searching the GC, see [Searching the Global Catalog](searching-global-catalog-contents.md).</span></span>

 

 




