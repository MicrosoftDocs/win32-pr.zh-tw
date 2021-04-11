---
description: 原生 Wifi API 包含支援無線網路連線能力和無線設定檔管理的功能、結構和列舉。
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: 關於原生 Wifi API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d4f656145430e34d79e05b88bc2bdeb54fe5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194942"
---
# <a name="about-the-native-wifi-api"></a><span data-ttu-id="b9ed0-103">關於原生 Wifi API</span><span class="sxs-lookup"><span data-stu-id="b9ed0-103">About the Native Wifi API</span></span>

<span data-ttu-id="b9ed0-104">原生 Wifi API 包含支援無線網路連線能力和無線設定檔管理的功能、結構和列舉。</span><span class="sxs-lookup"><span data-stu-id="b9ed0-104">The Native Wifi API contains functions, structures, and enumerations that support wireless network connectivity and wireless profile management.</span></span> <span data-ttu-id="b9ed0-105">API 可用於基礎結構和臨機操作網路。</span><span class="sxs-lookup"><span data-stu-id="b9ed0-105">The API can be used for both infrastructure and ad hoc networks.</span></span> <span data-ttu-id="b9ed0-106">無線臨機操作 API 是簡化的物件導向介面，用來建立、管理和使用臨機操作網路。</span><span class="sxs-lookup"><span data-stu-id="b9ed0-106">The Wireless Ad Hoc API is a simplified object-oriented interface for creating, managing, and using ad hoc networks.</span></span>

> [!Note]  
> <span data-ttu-id="b9ed0-107">未來的 Windows 版本可能無法使用臨機操作模式。</span><span class="sxs-lookup"><span data-stu-id="b9ed0-107">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="b9ed0-108">從 Windows 8.1 和 Windows Server 2012 R2 開始，請改用 [Wi-Fi Direct](about-the-wi-fi-direct-api.md) 。</span><span class="sxs-lookup"><span data-stu-id="b9ed0-108">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

<span data-ttu-id="b9ed0-109">特定 API 的執行會使用原生 Wifi API。</span><span class="sxs-lookup"><span data-stu-id="b9ed0-109">The implementation of the Ad Hoc API uses the Native Wifi API.</span></span> <span data-ttu-id="b9ed0-110">這表示臨機操作 API 呼叫可以觸發原生 Wifi 通知，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="b9ed0-110">This means that Ad Hoc API calls can trigger Native Wifi notifications, and vice versa.</span></span>

<span data-ttu-id="b9ed0-111">不建議混合原生 Wifi API 呼叫和無線臨機操作 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="b9ed0-111">Mixing Native Wifi API calls and Wireless Ad Hoc API calls is not recommended.</span></span> <span data-ttu-id="b9ed0-112">開發人員應該在設計應用程式之前，先選擇程式設計方法。</span><span class="sxs-lookup"><span data-stu-id="b9ed0-112">Developers should choose a programming approach before designing an application.</span></span> <span data-ttu-id="b9ed0-113">如果您的應用程式使用或管理基礎結構網路，您應該使用原生 Wifi API。</span><span class="sxs-lookup"><span data-stu-id="b9ed0-113">If your application uses or manages infrastructure networks, you should use the Native Wifi API.</span></span> <span data-ttu-id="b9ed0-114">如果您的應用程式需要設定檔管理功能，您應該使用原生 Wifi API。</span><span class="sxs-lookup"><span data-stu-id="b9ed0-114">If your application requires profile management functionality, you should use the Native Wifi API.</span></span> <span data-ttu-id="b9ed0-115">否則，您應該使用無線特定 API。</span><span class="sxs-lookup"><span data-stu-id="b9ed0-115">Otherwise, you should use the Wireless Ad Hoc API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9ed0-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="b9ed0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9ed0-117">關於原生 Wifi</span><span class="sxs-lookup"><span data-stu-id="b9ed0-117">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="b9ed0-118">Windows XP 上的原生 Wifi API 支援</span><span class="sxs-lookup"><span data-stu-id="b9ed0-118">Native Wifi API Support on Windows XP</span></span>](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[<span data-ttu-id="b9ed0-119">原生 Wifi API 許可權</span><span class="sxs-lookup"><span data-stu-id="b9ed0-119">Native Wifi API Permissions</span></span>](native-wifi-api-permissions.md)
</dt> <dt>

[<span data-ttu-id="b9ed0-120">關於無線特定 API</span><span class="sxs-lookup"><span data-stu-id="b9ed0-120">About the Wireless Ad Hoc API</span></span>](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[<span data-ttu-id="b9ed0-121">下載 Windows Vista SDK</span><span class="sxs-lookup"><span data-stu-id="b9ed0-121">Download the Windows Vista SDK</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 



