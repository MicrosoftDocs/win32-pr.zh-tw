---
description: 關聯提供者可讓 Windows Management Instrumentation (WMI) 用戶端，以從不同的命名空間來進行設定檔和相關聯的類別實例。
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: 存取 Interop 命名空間中的資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a217a7a44651b1a6c94476b53193eedac7f0d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945114"
---
# <a name="accessing-data-in-the-interop-namespace"></a><span data-ttu-id="d42ec-103">存取 Interop 命名空間中的資料</span><span class="sxs-lookup"><span data-stu-id="d42ec-103">Accessing Data in the Interop Namespace</span></span>

<span data-ttu-id="d42ec-104">關聯提供者可讓 Windows Management Instrumentation (WMI) 用戶端，以從不同的命名空間來進行設定檔和相關聯的類別實例。</span><span class="sxs-lookup"><span data-stu-id="d42ec-104">Association providers enable Windows Management Instrumentation (WMI) clients to traverse and retrieve profiles and associated class instances from different namespaces.</span></span>

<span data-ttu-id="d42ec-105">關聯提供者和類別位於 \\ \\ 根 \\ interop 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="d42ec-105">Association providers and classes reside in the \\\\root\\interop namespace.</span></span> <span data-ttu-id="d42ec-106">如需詳細資訊，請參閱 [跨命名空間關聯的遍歷](cross-namespace-association-traversal.md) 和 [寫入關聯提供者](writing-an-association-provider-for-interop.md)。</span><span class="sxs-lookup"><span data-stu-id="d42ec-106">For more information, see [Cross Namespace Association Traversal](cross-namespace-association-traversal.md) and [Writing an Association Provider](writing-an-association-provider-for-interop.md).</span></span>

<span data-ttu-id="d42ec-107">關聯提供者會公開標準設定檔，例如電源設定檔。</span><span class="sxs-lookup"><span data-stu-id="d42ec-107">Association providers expose standard profiles, like a power profile.</span></span> <span data-ttu-id="d42ec-108">下列範例會使用電源設定檔來說明如何透過 interop 命名空間來探索及存取資料。</span><span class="sxs-lookup"><span data-stu-id="d42ec-108">The following examples use the power profile to illustrate how to discover and access data through the interop namespace.</span></span>

<span data-ttu-id="d42ec-109">Windows PowerShell 提供簡單的機制，可透過適當的關聯、取出裝置設定檔，以及呼叫方法來進行。</span><span class="sxs-lookup"><span data-stu-id="d42ec-109">Windows PowerShell provides a simple mechanism to traverse through the appropriate association, retrieve a device profile, and call a method.</span></span>

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a><span data-ttu-id="d42ec-110">列舉根/interop 命名空間中的設定檔</span><span class="sxs-lookup"><span data-stu-id="d42ec-110">Enumerating profiles in the root/interop namespace</span></span>

<span data-ttu-id="d42ec-111">下列 Windows PowerShell 命令會列舉 Windows 7 電腦上的分散式管理工作強制 ([DMTF](https://www.dmtf.org/standards/wsman)) 支援的設定檔：</span><span class="sxs-lookup"><span data-stu-id="d42ec-111">The following Windows PowerShell command enumerates the Distributed Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman))-supported profiles on a Windows 7 computer:</span></span>


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a><span data-ttu-id="d42ec-112">正在抓取特定裝置設定檔的實例</span><span class="sxs-lookup"><span data-stu-id="d42ec-112">Retrieving instances of a specific device profile</span></span>

<span data-ttu-id="d42ec-113">下列 Windows PowerShell 命令會透過 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))來傳回指定之設定檔的所有實例：</span><span class="sxs-lookup"><span data-stu-id="d42ec-113">The following Windows PowerShell command returns all instances of a specified profile through [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)):</span></span>


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a><span data-ttu-id="d42ec-114">將電源設定檔指派給變數</span><span class="sxs-lookup"><span data-stu-id="d42ec-114">Assigning the power profile to a variable</span></span>

<span data-ttu-id="d42ec-115">下列 Windows PowerShell 命令會將電源設定檔實例指派給變數：</span><span class="sxs-lookup"><span data-stu-id="d42ec-115">The following Windows PowerShell command assigns the power profile instance to a variable:</span></span>


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a><span data-ttu-id="d42ec-116">列舉電腦上的電源計劃</span><span class="sxs-lookup"><span data-stu-id="d42ec-116">Enumerating the power plans on a computer</span></span>

<span data-ttu-id="d42ec-117">下列 Windows PowerShell 命令會列舉可用的電源設定檔方案：</span><span class="sxs-lookup"><span data-stu-id="d42ec-117">The following Windows PowerShell command enumerates the available power profile plans:</span></span>


```PowerShell
$pplan
```



## <a name="calling-a-method"></a><span data-ttu-id="d42ec-118">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="d42ec-118">Calling a method</span></span>

<span data-ttu-id="d42ec-119">下列 Windows PowerShell 命令會呼叫電源計劃的 [**啟動**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) 方法：</span><span class="sxs-lookup"><span data-stu-id="d42ec-119">The following Windows PowerShell command calls the [**Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) method for the power plan:</span></span>


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a><span data-ttu-id="d42ec-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="d42ec-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d42ec-121">跨命名空間關聯的遍歷</span><span class="sxs-lookup"><span data-stu-id="d42ec-121">Cross Namespace Association Traversal</span></span>](cross-namespace-association-traversal.md)
</dt> <dt>

[<span data-ttu-id="d42ec-122">撰寫關聯提供者</span><span class="sxs-lookup"><span data-stu-id="d42ec-122">Writing an Association Provider</span></span>](writing-an-association-provider-for-interop.md)
</dt> <dt>

<span data-ttu-id="d42ec-123">[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d42ec-123">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d42ec-124">[**Win32 \_ PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d42ec-124">[**Win32\_PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))</span></span>
</dt> </dl>

 

 
