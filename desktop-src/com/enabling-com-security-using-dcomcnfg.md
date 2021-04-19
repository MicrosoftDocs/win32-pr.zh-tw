---
title: 使用 DCOMCNFG 啟用 COM 安全性
description: Dcomcnfg.exe 提供使用者介面，可供修改登錄中的某些設定。
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01139584b715fccdad923bc5eb3d6a863a63ef8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106996553"
---
# <a name="enabling-com-security-using-dcomcnfg"></a><span data-ttu-id="b06fb-103">使用 DCOMCNFG 啟用 COM 安全性</span><span class="sxs-lookup"><span data-stu-id="b06fb-103">Enabling COM Security Using DCOMCNFG</span></span>

<span data-ttu-id="b06fb-104">Dcomcnfg.exe 提供使用者介面，可供修改登錄中的某些設定。</span><span class="sxs-lookup"><span data-stu-id="b06fb-104">Dcomcnfg.exe provides a user interface for modifying certain settings in the registry.</span></span> <span data-ttu-id="b06fb-105">藉由使用 Dcomcnfg.exe，您可以在整個電腦或整個進程的基礎上啟用安全性。</span><span class="sxs-lookup"><span data-stu-id="b06fb-105">By using Dcomcnfg.exe, you can enable security either on a computer-wide or a process-wide basis.</span></span> <span data-ttu-id="b06fb-106">您可以啟用特定電腦的安全性，如此一來，當處理常式未提供本身的安全性設定時，您可以透過程式設計方式或透過登錄值，將會使用 Dcomcnfg.exe 設定的值。</span><span class="sxs-lookup"><span data-stu-id="b06fb-106">You can enable security for a particular computer so that when a process does not provide its own security settings, either programmatically or through registry values, the values set by Dcomcnfg.exe will be used.</span></span> <span data-ttu-id="b06fb-107">或者，您可以使用 Dcomcnfg.exe 來啟用特定應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="b06fb-107">Or you can use Dcomcnfg.exe to enable security for a particular application only.</span></span>

<span data-ttu-id="b06fb-108">啟用安全性時，有兩個主要工作要完成：</span><span class="sxs-lookup"><span data-stu-id="b06fb-108">When enabling security, there are two primary tasks to accomplish:</span></span>

-   <span data-ttu-id="b06fb-109">設定不是 None 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="b06fb-109">Set an authentication level that is not None.</span></span>
-   <span data-ttu-id="b06fb-110">設定許可權，包括啟動和存取權限。</span><span class="sxs-lookup"><span data-stu-id="b06fb-110">Set permissions, including both launch and access permissions.</span></span>

<span data-ttu-id="b06fb-111">完成這些工作所採取的步驟取決於您是要為整個電腦還是只針對特定應用程式啟用安全性。</span><span class="sxs-lookup"><span data-stu-id="b06fb-111">The steps taken to accomplish these tasks depend on whether you are enabling security for the whole computer or just for a particular application.</span></span> <span data-ttu-id="b06fb-112">此外，您可能會想要設定電腦或應用程式的其他值。</span><span class="sxs-lookup"><span data-stu-id="b06fb-112">Also, you may want to set other values for the computer or application.</span></span>

> [!Note]  
> <span data-ttu-id="b06fb-113">您必須是系統管理員，才能執行 Dcomcnfg.exe。</span><span class="sxs-lookup"><span data-stu-id="b06fb-113">You must be an administrator to run Dcomcnfg.exe.</span></span>

 

<span data-ttu-id="b06fb-114">下列主題提供有關如何使用 Dcomcnfg.exe 設定安全性的逐步程式：</span><span class="sxs-lookup"><span data-stu-id="b06fb-114">The following topics provide step-by-step procedures on how to set security with Dcomcnfg.exe:</span></span>

-   [<span data-ttu-id="b06fb-115">使用 DCOMCNFG 設定 System-Wide 安全性</span><span class="sxs-lookup"><span data-stu-id="b06fb-115">Setting System-Wide Security Using DCOMCNFG</span></span>](setting-machine-wide-security-using-dcomcnfg.md)
-   [<span data-ttu-id="b06fb-116">使用 DCOMCNFG 設定 Processwide 安全性</span><span class="sxs-lookup"><span data-stu-id="b06fb-116">Setting Processwide Security Using DCOMCNFG</span></span>](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a><span data-ttu-id="b06fb-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="b06fb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b06fb-118">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="b06fb-118">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="b06fb-119">關閉安全性</span><span class="sxs-lookup"><span data-stu-id="b06fb-119">Turning Off Security</span></span>](turning-off-security.md)
</dt> </dl>

 

 




