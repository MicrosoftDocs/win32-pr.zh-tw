---
description: WoW64 現在是 Server Core 的選擇性功能
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: Server Core 中的 WoW64 狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fad947dac85707d3c9c89a2cffea38c4a4850a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084046"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a><span data-ttu-id="90243-103">WoW64 現在是 Server Core 的選擇性功能</span><span class="sxs-lookup"><span data-stu-id="90243-103">WoW64 Is Now an Optional Feature for Server Core</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="90243-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="90243-104">Affected Platforms</span></span>

<span data-ttu-id="90243-105">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="90243-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="90243-106">功能影響</span><span class="sxs-lookup"><span data-stu-id="90243-106">Feature Impact</span></span>

 <span data-ttu-id="90243-107">**嚴重性** -低</span><span class="sxs-lookup"><span data-stu-id="90243-107">**Severity** - Low</span></span>  
<span data-ttu-id="90243-108">**頻率** -低</span><span class="sxs-lookup"><span data-stu-id="90243-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="90243-109">Description</span><span class="sxs-lookup"><span data-stu-id="90243-109">Description</span></span>

<span data-ttu-id="90243-110">適用于 Windows Server 2008 R2 的 Server Core 安裝選項可讓您卸載 WoW64。</span><span class="sxs-lookup"><span data-stu-id="90243-110">The Server Core installation option for Windows Server 2008 R2 allows you to uninstall WoW64.</span></span> <span data-ttu-id="90243-111">WoW64 現在是選擇性功能，如果不需要執行32位的程式碼，您可以將其卸載。</span><span class="sxs-lookup"><span data-stu-id="90243-111">WoW64 is now an optional feature that you can uninstall if it is not necessary to run 32-bit code.</span></span>

<span data-ttu-id="90243-112">此外，Active Directory 和 Active Directory 輕量型目錄服務角色都需要 WoW64，才能在 Windows Server 2008 R2 中執行。</span><span class="sxs-lookup"><span data-stu-id="90243-112">In addition, the Active Directory and Active Directory Lightweight Directory Services roles require WoW64 in order to run in Windows Server 2008 R2.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="90243-113">影響的表現</span><span class="sxs-lookup"><span data-stu-id="90243-113">Manifestation of Impact</span></span>

<span data-ttu-id="90243-114">如果您卸載 WoW64，在 Server Core 上執行32位程式碼的系統管理員將會收到錯誤訊息，指出無法執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="90243-114">If you uninstall WoW64, Administrators running 32-bit code on Server Core will receive an error message that the application cannot be executed.</span></span> <span data-ttu-id="90243-115">如果系統管理員嘗試執行 Active Directory 並 Active Directory 輕量型目錄服務，則會收到錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="90243-115">If Administrators attempt to run Active Directory and Active Directory Lightweight Directory Services, they will receive an error message.</span></span>

## <a name="mitigation"></a><span data-ttu-id="90243-116">降低</span><span class="sxs-lookup"><span data-stu-id="90243-116">Mitigation</span></span>

<span data-ttu-id="90243-117">安裝 WoW64。</span><span class="sxs-lookup"><span data-stu-id="90243-117">Install WoW64.</span></span>

## <a name="solution"></a><span data-ttu-id="90243-118">解決方法</span><span class="sxs-lookup"><span data-stu-id="90243-118">Solution</span></span>

<span data-ttu-id="90243-119">慣用的解決方案是提供64位版本的程式碼，讓它可以在 Server Core 上執行，而不需要 WoW64。</span><span class="sxs-lookup"><span data-stu-id="90243-119">The preferred solution is to provide a 64-bit version of the code to enable it to run on Server Core without needing WoW64.</span></span>

<span data-ttu-id="90243-120">至少，請提供使用者檔，請注意，若要執行32位程式碼，他們必須安裝 WoW64。</span><span class="sxs-lookup"><span data-stu-id="90243-120">At a minimum, provide user documentation noting that to run 32-bit code they must install WoW64.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="90243-121">相容性、效能、可靠性和可用性測試</span><span class="sxs-lookup"><span data-stu-id="90243-121">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="90243-122">確認所有使用的程式碼都是64位。</span><span class="sxs-lookup"><span data-stu-id="90243-122">Verify that all code used is 64-bit.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="90243-123">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="90243-123">Links to Other Resources</span></span>

-   [<span data-ttu-id="90243-124">WOW64 執行詳細資料</span><span class="sxs-lookup"><span data-stu-id="90243-124">WOW64 Implementation Details</span></span>](../winprog64/wow64-implementation-details.md)
-   [<span data-ttu-id="90243-125">調試 WOW64</span><span class="sxs-lookup"><span data-stu-id="90243-125">Debugging WOW64</span></span>](../winprog64/debugging-wow64.md)
-   <span data-ttu-id="90243-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90243-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>

 

 
