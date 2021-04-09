---
description: Microsoft Windows 作業系統使用時間提供者架構，提供各種硬體裝置和網路時間通訊協定的支援。
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: 時間提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c844e2c4d0d49e87e978a47621338b167c4f5a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851264"
---
# <a name="time-provider"></a><span data-ttu-id="9e249-103">時間提供者</span><span class="sxs-lookup"><span data-stu-id="9e249-103">Time Provider</span></span>

<span data-ttu-id="9e249-104">Microsoft Windows 作業系統使用 *時間提供者* 架構，提供各種硬體裝置和網路時間通訊協定的支援。</span><span class="sxs-lookup"><span data-stu-id="9e249-104">The Microsoft Windows operating system provides support for a variety of hardware devices and network time protocols using the *time provider* architecture.</span></span> <span data-ttu-id="9e249-105">輸入時間提供者會從硬體或網路取得準確的時間戳記，而輸出時間提供者則會提供時間戳記給網路上的其他用戶端。</span><span class="sxs-lookup"><span data-stu-id="9e249-105">Input time providers retrieve accurate time stamps from hardware or the network, and output time providers provide time stamps to other clients on the network.</span></span>

<span data-ttu-id="9e249-106">時間提供者是由 *時間提供者管理員* 管理。</span><span class="sxs-lookup"><span data-stu-id="9e249-106">Time providers are managed by the *time provider manager*.</span></span> <span data-ttu-id="9e249-107">它負責載入、啟動和停止服務控制管理員所導向的時間提供者。</span><span class="sxs-lookup"><span data-stu-id="9e249-107">It is responsible for loading, starting, and stopping time providers as directed by the service control manager.</span></span> <span data-ttu-id="9e249-108">這個介面讓撰寫時間提供者的程式比撰寫完整的服務更容易。</span><span class="sxs-lookup"><span data-stu-id="9e249-108">This interface makes writing a time provider easier than writing a full service.</span></span>

-   [<span data-ttu-id="9e249-109">建立時間提供者</span><span class="sxs-lookup"><span data-stu-id="9e249-109">Creating a Time Provider</span></span>](creating-a-time-provider.md)
-   [<span data-ttu-id="9e249-110">註冊時間提供者</span><span class="sxs-lookup"><span data-stu-id="9e249-110">Registering a Time Provider</span></span>](registering-a-time-provider.md)
-   [<span data-ttu-id="9e249-111">範例時間提供者</span><span class="sxs-lookup"><span data-stu-id="9e249-111">Sample Time Provider</span></span>](sample-time-provider.md)

## <a name="related-topics"></a><span data-ttu-id="9e249-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="9e249-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e249-113">Windows Time 服務</span><span class="sxs-lookup"><span data-stu-id="9e249-113">Windows Time Service</span></span>](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



