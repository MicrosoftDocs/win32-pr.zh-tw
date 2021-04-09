---
description: 本節說明可用來開發自訂監視的 helper 函數。
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: 監視函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9391927104196e282d4438c0b047e233d61f3619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848159"
---
# <a name="monitor-functions"></a><span data-ttu-id="134fb-103">監視函式</span><span class="sxs-lookup"><span data-stu-id="134fb-103">Monitor Functions</span></span>

<span data-ttu-id="134fb-104">本節說明可用來開發自訂監視的 helper 函數。</span><span class="sxs-lookup"><span data-stu-id="134fb-104">This section describes the helper functions you can use to develop custom monitors.</span></span>



| <span data-ttu-id="134fb-105">函式</span><span class="sxs-lookup"><span data-stu-id="134fb-105">Function</span></span>                                       | <span data-ttu-id="134fb-106">描述</span><span class="sxs-lookup"><span data-stu-id="134fb-106">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="134fb-107">DllGetMonitorObject</span><span class="sxs-lookup"><span data-stu-id="134fb-107">DllGetMonitorObject</span></span>](dllgetmonitorobject.md) | <span data-ttu-id="134fb-108">建立監視的實例。</span><span class="sxs-lookup"><span data-stu-id="134fb-108">Creates an instance of the monitor.</span></span>                                                                                                                              |
| [<span data-ttu-id="134fb-109">HTMLValueToUnicode</span><span class="sxs-lookup"><span data-stu-id="134fb-109">HTMLValueToUnicode</span></span>](htmlvaluetounicode.md)   | <span data-ttu-id="134fb-110">將 HTML CP \_ UTF8 版本字串轉換成 Unicode。</span><span class="sxs-lookup"><span data-stu-id="134fb-110">Converts an HTML CP\_UTF8 version string to Unicode.</span></span>                                                                                                             |
| [<span data-ttu-id="134fb-111">LoadDWORD</span><span class="sxs-lookup"><span data-stu-id="134fb-111">LoadDWORD</span></span>](loaddword.md)                     | <span data-ttu-id="134fb-112">從 HTML 設定字串載入 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="134fb-112">Loads a **DWORD** from an HTML configuration string.</span></span>                                                                                                             |
| [<span data-ttu-id="134fb-113">LoadIPAddresses</span><span class="sxs-lookup"><span data-stu-id="134fb-113">LoadIPAddresses</span></span>](loadipaddresses.md)         | <span data-ttu-id="134fb-114">從 HTML TEXTAREA 設定字串載入 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="134fb-114">Loads an IP address list from an HTML TEXTAREA configuration string.</span></span>                                                                                             |
| [<span data-ttu-id="134fb-115">LoadIPXAddresses</span><span class="sxs-lookup"><span data-stu-id="134fb-115">LoadIPXAddresses</span></span>](loadipxaddresses.md)       | <span data-ttu-id="134fb-116">從 HTML TEXTAREA 設定字串載入 IPX 地址清單。</span><span class="sxs-lookup"><span data-stu-id="134fb-116">Loads an IPX address list from an HTML TEXTAREA configuration string.</span></span>                                                                                            |
| [<span data-ttu-id="134fb-117">LoadMACAddresses</span><span class="sxs-lookup"><span data-stu-id="134fb-117">LoadMACAddresses</span></span>](loadmacaddresses.md)       | <span data-ttu-id="134fb-118">從 HTML TEXTAREA 設定字串載入 MAC 地址清單。</span><span class="sxs-lookup"><span data-stu-id="134fb-118">Loads a MAC address list from an HTML TEXTAREA configuration string.</span></span>                                                                                             |
| [<span data-ttu-id="134fb-119">LoadStringAddr</span><span class="sxs-lookup"><span data-stu-id="134fb-119">LoadStringAddr</span></span>](loadstringaddr.md)           | <span data-ttu-id="134fb-120">將字串 (例如 "157.54.32.45" ) 轉換為 **DWORD** 位址。</span><span class="sxs-lookup"><span data-stu-id="134fb-120">Transforms a string (such as "157.54.32.45") to a **DWORD** address.</span></span>                                                                                             |
| [<span data-ttu-id="134fb-121">LoadTCHAR</span><span class="sxs-lookup"><span data-stu-id="134fb-121">LoadTCHAR</span></span>](loadtchar.md)                     | <span data-ttu-id="134fb-122">在設定字串中搜尋要求的變數名稱，並使用 **HeapAllocMemory**) 來儲存、複製和傳回，以配置足夠的空間 (。</span><span class="sxs-lookup"><span data-stu-id="134fb-122">Searches for a requested variable name in the configuration string, and allocates sufficient space (by using **HeapAllocMemory**) to store, copy, and return it.</span></span> |
| [<span data-ttu-id="134fb-123">OnLoadingDLL</span><span class="sxs-lookup"><span data-stu-id="134fb-123">OnLoadingDLL</span></span>](onloadingdll.md)               | <span data-ttu-id="134fb-124">表示已開始載入 DLL。</span><span class="sxs-lookup"><span data-stu-id="134fb-124">Indicates that the DLL has begun to load.</span></span> <span data-ttu-id="134fb-125">當 MCSVC 第一次載入監視器 DLL 時，會呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="134fb-125">The MCSVC calls this function when it first loads the monitor DLL.</span></span>                                                     |



 

 

 



