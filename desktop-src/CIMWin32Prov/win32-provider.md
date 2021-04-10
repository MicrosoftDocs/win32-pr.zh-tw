---
description: Microsoft&\# 160;Win32 提供者會抓取和更新 Windows 系統&郵件的相關資料， \# 例如環境變數目前的設定和邏輯磁片的屬性。
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Win32 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dfb29b6f80ed833de0f4185070d46770c6cd2f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688628"
---
# <a name="win32-provider"></a><span data-ttu-id="10b46-103">Win32 提供者</span><span class="sxs-lookup"><span data-stu-id="10b46-103">Win32 Provider</span></span>

<span data-ttu-id="10b46-104">Microsoft Win32 提供者會抓取和更新與 Windows 系統相關的資料—像是環境變數目前的設定和邏輯磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="10b46-104">The Microsoft Win32 provider retrieves and updates data relevant to Windows systems—data such as the current settings of environment variables and the attributes of a logical disk.</span></span> <span data-ttu-id="10b46-105">使用 Win32 提供者時，管理應用程式可以使用 WMI 輕鬆地存取此資料。</span><span class="sxs-lookup"><span data-stu-id="10b46-105">With the Win32 provider, management applications can use WMI to easily access this data.</span></span> <span data-ttu-id="10b46-106">Win32 提供者會藉由發出 Windows 函數呼叫和查詢系統登錄來抓取其資訊。</span><span class="sxs-lookup"><span data-stu-id="10b46-106">The Win32 provider retrieves its information by making Windows function calls and querying the system registry.</span></span>

<span data-ttu-id="10b46-107">Win32 提供者會定義用來描述 Windows 系統上可用之硬體或軟體的類別，以及它們之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="10b46-107">The Win32 provider defines the classes used to describe hardware or software available on Windows systems and the relationships between them.</span></span>

<span data-ttu-id="10b46-108">Win32 提供者是實例和方法提供者，它會實作為標準 [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) 介面，以及下列 [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) 方法：</span><span class="sxs-lookup"><span data-stu-id="10b46-108">As an instance and method provider, the Win32 provider implements the standard [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface as well as the following [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="10b46-109">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="10b46-109">**CreateInstanceEnumAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="10b46-110">**DeleteInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="10b46-110">**DeleteInstanceAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [<span data-ttu-id="10b46-111">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="10b46-111">**ExecMethodAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="10b46-112">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="10b46-112">**ExecQueryAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="10b46-113">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="10b46-113">**GetObjectAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="10b46-114">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="10b46-114">**PutInstanceAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="10b46-115">下表列出 Win32 提供者類別類別目錄。</span><span class="sxs-lookup"><span data-stu-id="10b46-115">The following table lists the Win32 provider class categories.</span></span>



| <span data-ttu-id="10b46-116">類別</span><span class="sxs-lookup"><span data-stu-id="10b46-116">Classes</span></span>                                                                             | <span data-ttu-id="10b46-117">Description</span><span class="sxs-lookup"><span data-stu-id="10b46-117">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="10b46-118">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="10b46-118">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)<br/> | <span data-ttu-id="10b46-119">與硬體相關的物件。</span><span class="sxs-lookup"><span data-stu-id="10b46-119">Hardware-related objects.</span></span><br/>                                      |
| [<span data-ttu-id="10b46-120">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="10b46-120">Operating System Classes</span></span>](operating-system-classes.md)<br/>                 | <span data-ttu-id="10b46-121">作業系統相關物件。</span><span class="sxs-lookup"><span data-stu-id="10b46-121">Operating system related objects.</span></span><br/>                              |
| [<span data-ttu-id="10b46-122">效能計數器類別</span><span class="sxs-lookup"><span data-stu-id="10b46-122">Performance Counter Classes</span></span>](performance-counter-classes.md)<br/>           | <span data-ttu-id="10b46-123">效能計數器中的原始和計算效能資料。</span><span class="sxs-lookup"><span data-stu-id="10b46-123">Raw and calculated performance data from performance counters.</span></span><br/> |
| [<span data-ttu-id="10b46-124">WMI 服務管理類別</span><span class="sxs-lookup"><span data-stu-id="10b46-124">WMI Service Management Classes</span></span>](wmi-service-management-classes.md)<br/>     | <span data-ttu-id="10b46-125">WMI 的管理。</span><span class="sxs-lookup"><span data-stu-id="10b46-125">Management for WMI.</span></span><br/>                                            |



 

## <a name="related-topics"></a><span data-ttu-id="10b46-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="10b46-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10b46-127">CIMWin32 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="10b46-127">CIMWin32 WMI Provider</span></span>](cimwin32-wmi-providers.md)
</dt> </dl>

 

 
