---
title: PreferredServerBitness
description: 設定此 COM 伺服器的慣用架構（32位或64位）。
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- PreferredServerBitness 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a8c5b1504c5a59ca2ab178cd46236335d44ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316546"
---
# <a name="preferredserverbitness"></a><span data-ttu-id="a8d8e-104">PreferredServerBitness</span><span class="sxs-lookup"><span data-stu-id="a8d8e-104">PreferredServerBitness</span></span>

<span data-ttu-id="a8d8e-105">設定此 COM 伺服器的慣用架構（32位或64位）。</span><span class="sxs-lookup"><span data-stu-id="a8d8e-105">Sets the preferred architecture, 32-bit or 64-bit, for this COM server.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a8d8e-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="a8d8e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a><span data-ttu-id="a8d8e-107">備註</span><span class="sxs-lookup"><span data-stu-id="a8d8e-107">Remarks</span></span>

<span data-ttu-id="a8d8e-108">這是只能在64位版本的 Windows 上使用的 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="a8d8e-108">This is a **REG\_DWORD** value that is available only on 64-bit versions of Windows.</span></span>



| <span data-ttu-id="a8d8e-109">值</span><span class="sxs-lookup"><span data-stu-id="a8d8e-109">Value</span></span> | <span data-ttu-id="a8d8e-110">描述</span><span class="sxs-lookup"><span data-stu-id="a8d8e-110">Description</span></span>                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d8e-111">1</span><span class="sxs-lookup"><span data-stu-id="a8d8e-111">1</span></span>     | <span data-ttu-id="a8d8e-112">將伺服器架構與用戶端架構比對。</span><span class="sxs-lookup"><span data-stu-id="a8d8e-112">Match the server architecture to the client architecture.</span></span> <span data-ttu-id="a8d8e-113">例如，如果用戶端是32位，請使用32位版本的伺服器（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a8d8e-113">For example, if the client is 32-bit, use a 32-bit version of the server, if it is available.</span></span> <span data-ttu-id="a8d8e-114">如果沒有，用戶端的啟用要求將會失敗。</span><span class="sxs-lookup"><span data-stu-id="a8d8e-114">If not, the client's activation request will fail.</span></span> |
| <span data-ttu-id="a8d8e-115">2</span><span class="sxs-lookup"><span data-stu-id="a8d8e-115">2</span></span>     | <span data-ttu-id="a8d8e-116">使用32位版本的伺服器。</span><span class="sxs-lookup"><span data-stu-id="a8d8e-116">Use a 32-bit version of the server.</span></span> <span data-ttu-id="a8d8e-117">如果不存在，用戶端的啟用要求將會失敗。</span><span class="sxs-lookup"><span data-stu-id="a8d8e-117">If one does not exist, the client's activation request will fail.</span></span>                                                                                                      |
| <span data-ttu-id="a8d8e-118">3</span><span class="sxs-lookup"><span data-stu-id="a8d8e-118">3</span></span>     | <span data-ttu-id="a8d8e-119">使用64位版本的伺服器。</span><span class="sxs-lookup"><span data-stu-id="a8d8e-119">Use a 64-bit version of the server.</span></span> <span data-ttu-id="a8d8e-120">如果不存在，用戶端的啟用要求將會失敗。</span><span class="sxs-lookup"><span data-stu-id="a8d8e-120">If one does not exist, the client's activation request will fail.</span></span>                                                                                                      |



 

<span data-ttu-id="a8d8e-121">如果此值不存在，則：</span><span class="sxs-lookup"><span data-stu-id="a8d8e-121">If this value is not present, then:</span></span>

-   <span data-ttu-id="a8d8e-122">如果裝載伺服器的電腦執行的是 Windows XP 或 Windows Server 2003 （未安裝 SP1 或更新版本），則 COM 會偏好使用64位版本的伺服器（如果有的話）：否則，它會啟用32位版本的伺服器。</span><span class="sxs-lookup"><span data-stu-id="a8d8e-122">If the computer that hosts the server is running Windows XP or Windows Server 2003 without SP1 or later installed, then COM will prefer a 64-bit version of the server if available; otherwise it will activate a 32-bit version of the server.</span></span>
-   <span data-ttu-id="a8d8e-123">如果裝載伺服器的電腦執行的是 Windows Server 2003 SP1 或更新版本，則 COM 會嘗試將伺服器架構與用戶端架構比對。</span><span class="sxs-lookup"><span data-stu-id="a8d8e-123">If the computer that hosts the server is running Windows Server 2003 with SP1 or later installed, then COM will try to match the server architecture to the client architecture.</span></span> <span data-ttu-id="a8d8e-124">換句話說，對於32位用戶端，COM 會啟用32位伺服器（如果有的話）。否則，它會啟用64位版本的伺服器。</span><span class="sxs-lookup"><span data-stu-id="a8d8e-124">In other words, for a 32-bit client, COM will activate a 32-bit server if available; otherwise it will activate a 64-bit version of the server.</span></span> <span data-ttu-id="a8d8e-125">若為64位用戶端，COM 會啟用64位伺服器（如果有的話）。否則會啟動32位伺服器。</span><span class="sxs-lookup"><span data-stu-id="a8d8e-125">For a 64-bit client, COM will activate a 64-bit server if available; otherwise it will activate a 32-bit server.</span></span>

<span data-ttu-id="a8d8e-126">用戶端也可以透過 CLSCTX \_ activate \_ 32 \_ 位 \_ 伺服器和 CLSCTX activate 64 bit 伺服器旗標來指定自己的架構喜好設定 \_ \_ \_ \_ ，這些將覆寫伺服器的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="a8d8e-126">The client can also specify its own architecture preference via the CLSCTX\_ACTIVATE\_32\_BIT\_SERVER and CLSCTX\_ACTIVATE\_64\_BIT\_SERVER flags, and these will override the server's preference.</span></span> <span data-ttu-id="a8d8e-127">如需詳細資訊，以及用戶端與伺服器架構喜好設定之間可能互動的圖表，請參閱 [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)。</span><span class="sxs-lookup"><span data-stu-id="a8d8e-127">For more information, and a chart of possible interactions between client and server architecture preferences, see [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8d8e-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="a8d8e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8d8e-129">**CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="a8d8e-129">**CLSCTX**</span></span>](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 