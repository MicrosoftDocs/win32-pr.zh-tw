---
title: 建立遠端桌面通訊協定提供者
description: 建立遠端桌面通訊協定提供者的相關資訊。 通訊協定管理員會實作為 COM 伺服器，並在遠端桌面服務服務啟動時搜尋的位置註冊。
ms.assetid: 9a3e6d5c-464f-4227-a06f-16eb8ed1079e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41265a350b4d5c559731a09abc21aa4c81b9b29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968005"
---
# <a name="creating-a-remote-desktop-protocol-provider"></a><span data-ttu-id="e1310-104">建立遠端桌面通訊協定提供者</span><span class="sxs-lookup"><span data-stu-id="e1310-104">Creating a Remote Desktop Protocol Provider</span></span>

<span data-ttu-id="e1310-105">下列各節包含有關建立遠端桌面通訊協定提供者的資訊。</span><span class="sxs-lookup"><span data-stu-id="e1310-105">The following sections contain information about creating a Remote Desktop Protocol Provider.</span></span> <span data-ttu-id="e1310-106">通訊協定管理員會實作為 COM 伺服器，並在遠端桌面服務服務啟動時搜尋的位置註冊。</span><span class="sxs-lookup"><span data-stu-id="e1310-106">The protocol manager is implemented as a COM server and registered in a location searched when the Remote Desktop Services service starts.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e1310-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="e1310-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="e1310-108">註冊通訊協定管理員</span><span class="sxs-lookup"><span data-stu-id="e1310-108">Registering the Protocol Manager</span></span>](registering-the-custom-protocol.md)
</dt> <dd>

<span data-ttu-id="e1310-109">您至少必須為通訊協定管理員建立一個登錄值專案，遠端桌面服務服務才能將它具現化。</span><span class="sxs-lookup"><span data-stu-id="e1310-109">You must create at least one registry value entry for your protocol manager so that the Remote Desktop Services service can instantiate it.</span></span>

</dd> <dt>

[<span data-ttu-id="e1310-110">方法呼叫順序</span><span class="sxs-lookup"><span data-stu-id="e1310-110">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dd>

<span data-ttu-id="e1310-111">遠端桌面服務服務和您的通訊協定提供者會以明確定義的序列彼此呼叫。</span><span class="sxs-lookup"><span data-stu-id="e1310-111">The Remote Desktop Services service and your protocol provider call each other in clearly defined sequences.</span></span>

</dd> </dl>

-   [<span data-ttu-id="e1310-112">註冊通訊協定管理員</span><span class="sxs-lookup"><span data-stu-id="e1310-112">Registering the Protocol Manager</span></span>](registering-the-custom-protocol.md)
-   [<span data-ttu-id="e1310-113">方法呼叫順序</span><span class="sxs-lookup"><span data-stu-id="e1310-113">Method Call Sequence</span></span>](method-call-sequence.md)

## <a name="related-topics"></a><span data-ttu-id="e1310-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1310-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1310-115">遠端桌面通訊協定提供者 API</span><span class="sxs-lookup"><span data-stu-id="e1310-115">Remote Desktop Protocol Provider API</span></span>](custom-remote-desktop-protocols.md)
</dt> <dt>

[<span data-ttu-id="e1310-116">使用遠端桌面服務</span><span class="sxs-lookup"><span data-stu-id="e1310-116">Using Remote Desktop Services</span></span>](using-terminal-services.md)
</dt> </dl>

 

 




