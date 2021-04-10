---
description: .
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: Microsoft Message Queuing (MSMQ) -SHA 2 是預設的雜湊演算法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f0d2476133ca7939bc90effa3842c0b90482ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194157"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a><span data-ttu-id="3eb4d-103">Microsoft Message Queuing (MSMQ) -SHA 2 是預設的雜湊演算法</span><span class="sxs-lookup"><span data-stu-id="3eb4d-103">Microsoft Message Queuing (MSMQ) - SHA 2 Is the Default Hash Algorithm</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="3eb4d-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="3eb4d-104">Affected Platforms</span></span>

 <span data-ttu-id="3eb4d-105">**客戶** 端-windows XP \| windows Vista \| windows 7</span><span class="sxs-lookup"><span data-stu-id="3eb4d-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="3eb4d-106">**伺服器** -windows server 2003 \| windows Server 2008 \| windows server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3eb4d-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="3eb4d-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="3eb4d-107">Feature Impact</span></span>

 <span data-ttu-id="3eb4d-108">**嚴重性** -低</span><span class="sxs-lookup"><span data-stu-id="3eb4d-108">**Severity** - Low</span></span>  
<span data-ttu-id="3eb4d-109">**頻率** -低</span><span class="sxs-lookup"><span data-stu-id="3eb4d-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="3eb4d-110">Description</span><span class="sxs-lookup"><span data-stu-id="3eb4d-110">Description</span></span>

<span data-ttu-id="3eb4d-111">在 Windows 7 中，MSMQ 會使用 SHA-2 做為簽署外寄訊息時的預設值。</span><span class="sxs-lookup"><span data-stu-id="3eb4d-111">In Windows 7, MSMQ uses SHA-2 as the default when signing an outgoing message.</span></span> <span data-ttu-id="3eb4d-112">此外，所有傳入的訊息都必須使用 SHA-1 簽署。</span><span class="sxs-lookup"><span data-stu-id="3eb4d-112">Additionally, all incoming messages must be signed with SHA-2.</span></span> <span data-ttu-id="3eb4d-113">您可以透過系統管理員可存取的登錄機碼來啟用較低加密演算法的支援。</span><span class="sxs-lookup"><span data-stu-id="3eb4d-113">You can enable support for a lower encryption algorithm through an administrator-accessible registry key.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="3eb4d-114">影響的表現</span><span class="sxs-lookup"><span data-stu-id="3eb4d-114">Manifestation of Impact</span></span>

-   <span data-ttu-id="3eb4d-115">Windows 2003 或更低的 MSMQ 在 Windows 7 中不接受源自 MSMQ 的已簽署訊息</span><span class="sxs-lookup"><span data-stu-id="3eb4d-115">MSMQ in Windows 2003 or below will not accept signed messages originating from MSMQ in Windows 7</span></span>
-   <span data-ttu-id="3eb4d-116">Windows 7 中的 MSMQ 不會接受源自 Windows 2008 或更低的已簽署訊息</span><span class="sxs-lookup"><span data-stu-id="3eb4d-116">MSMQ in Windows 7 will not accept signed messages originating from Windows 2008 or below</span></span>

## <a name="mitigation"></a><span data-ttu-id="3eb4d-117">降低</span><span class="sxs-lookup"><span data-stu-id="3eb4d-117">Mitigation</span></span>

<span data-ttu-id="3eb4d-118">使用者應考慮升級至 Windows 7，以利用強式簽署演算法。</span><span class="sxs-lookup"><span data-stu-id="3eb4d-118">Users should consider upgrading to Windows 7 to leverage the stronger signing algorithm.</span></span> <span data-ttu-id="3eb4d-119">若要在 Windows 7 和任何舊版作業系統之間啟用無縫簽署的訊息交換，系統管理員必須在 MSMQ 電腦上新增適當的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="3eb4d-119">To enable seamless signed message exchange between Windows 7 and any down-level operating system, the Administrator must add appropriate exceptions on the MSMQ machines.</span></span>

 

 



