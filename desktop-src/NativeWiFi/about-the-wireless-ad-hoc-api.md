---
description: 關於無線特定 API
ms.assetid: 9e6e32c5-454b-41c8-b00e-70a2e82266f1
title: 關於無線特定 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d3ac7d87159505a3d69f65ff2e8f5d59adc35b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987793"
---
# <a name="about-the-wireless-ad-hoc-api"></a><span data-ttu-id="d4c46-103">關於無線特定 API</span><span class="sxs-lookup"><span data-stu-id="d4c46-103">About the Wireless Ad Hoc API</span></span>

<span data-ttu-id="d4c46-104">無線臨機操作 API 會公開介面，以列舉及連接至802.11 的臨機操作網路。</span><span class="sxs-lookup"><span data-stu-id="d4c46-104">The Wireless Ad Hoc API exposes interfaces for enumerating and connecting to 802.11 ad hoc networks.</span></span> <span data-ttu-id="d4c46-105">這些介面可提供簡化的物件導向方法來進行臨機操作網路管理。</span><span class="sxs-lookup"><span data-stu-id="d4c46-105">These interfaces provide a simplified object-oriented approach to ad hoc network management.</span></span> <span data-ttu-id="d4c46-106">系統會提供網路和介面的標準枚舉器。</span><span class="sxs-lookup"><span data-stu-id="d4c46-106">Standard enumerators are provided for networks and interfaces.</span></span> <span data-ttu-id="d4c46-107">您可以篩選這些列舉值，只列舉應用程式所建立的特定網路。</span><span class="sxs-lookup"><span data-stu-id="d4c46-107">These enumerators can be filtered to enumerate only ad hoc networks created by your application.</span></span>

> [!Note]  
> <span data-ttu-id="d4c46-108">未來的 Windows 版本可能無法使用臨機操作模式。</span><span class="sxs-lookup"><span data-stu-id="d4c46-108">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="d4c46-109">從 Windows 8.1 和 Windows Server 2012 R2 開始，請改用 [Wi-Fi Direct](about-the-wi-fi-direct-api.md) 。</span><span class="sxs-lookup"><span data-stu-id="d4c46-109">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

<span data-ttu-id="d4c46-110">使用臨機操作 API 的開發人員應該注意，使用原生 Wifi API 所建立的網路和設定檔，可以使用原生 Wifi API 來操作，而不會通知相關的特定 API 通知接聽程式。</span><span class="sxs-lookup"><span data-stu-id="d4c46-110">Developers using the Ad Hoc API should be aware that networks and profiles created using the Ad Hoc API can be manipulated using the Native Wifi API without notifying the relevant Ad Hoc API notification listeners.</span></span>

<span data-ttu-id="d4c46-111">無線臨機操作 [參考](wireless-ad-hoc-reference.md)的詳細說明無線臨機操作 API。</span><span class="sxs-lookup"><span data-stu-id="d4c46-111">The Wireless Ad Hoc API is described in detail in the [Wireless Ad Hoc Reference](wireless-ad-hoc-reference.md).</span></span>

> [!Note]  
> <span data-ttu-id="d4c46-112">只有在 Windows Vista 和更新版本的作業系統上才支援無線臨機操作 API。</span><span class="sxs-lookup"><span data-stu-id="d4c46-112">The Wireless Ad Hoc API is only supported on Windows Vista and later versions of the operating system.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d4c46-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4c46-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4c46-114">關於原生 Wifi</span><span class="sxs-lookup"><span data-stu-id="d4c46-114">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="d4c46-115">關於原生 Wifi API</span><span class="sxs-lookup"><span data-stu-id="d4c46-115">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> </dl>

 

 



