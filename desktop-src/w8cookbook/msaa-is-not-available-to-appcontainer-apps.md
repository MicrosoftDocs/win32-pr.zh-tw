---
title: MSAA 無法供 Windows Store 應用程式使用
description: MSAA 無法供 Windows Store 應用程式使用
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e9c1221850b1fa97a3a0d5fcef119c21277486
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104024229"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a><span data-ttu-id="a8bcd-103">MSAA 無法供 Windows Store 應用程式使用</span><span class="sxs-lookup"><span data-stu-id="a8bcd-103">MSAA is not available to Windows Store apps</span></span>

## <a name="platform"></a><span data-ttu-id="a8bcd-104">平台</span><span class="sxs-lookup"><span data-stu-id="a8bcd-104">Platform</span></span>

<span data-ttu-id="a8bcd-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="a8bcd-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="a8bcd-106">Description</span><span class="sxs-lookup"><span data-stu-id="a8bcd-106">Description</span></span>

<span data-ttu-id="a8bcd-107">Windows 8 不支援從 Windows Store 應用程式讀取或自動化可存取資料的 MSAA (Microsoft Active Accessibility) 。</span><span class="sxs-lookup"><span data-stu-id="a8bcd-107">Windows 8 does not support MSAA (Microsoft Active Accessibility) for reading or automating accessible data from Windows Store apps.</span></span> <span data-ttu-id="a8bcd-108">消費者介面自動化 (UIA) API （自 Windows 7 起提供）應改用。</span><span class="sxs-lookup"><span data-stu-id="a8bcd-108">The UI Automation (UIA) API, available since Windows 7, should be used instead.</span></span> <span data-ttu-id="a8bcd-109">因為沒有任何現有的 Windows Store 應用程式功能，所以沒有受此變更影響的現有實施。</span><span class="sxs-lookup"><span data-stu-id="a8bcd-109">Since there are no existing Windows Store app features, there are no existing implementations that are affected by this change.</span></span> <span data-ttu-id="a8bcd-110">這只會影響針對 Windows 8 所撰寫的新應用程式和功能。</span><span class="sxs-lookup"><span data-stu-id="a8bcd-110">This affects only new apps and features written for Windows 8.</span></span> <span data-ttu-id="a8bcd-111">開發人員仍然可以使用 MSAA 來公開其協助工具資料。</span><span class="sxs-lookup"><span data-stu-id="a8bcd-111">Developers can still use MSAA to expose their accessibility data.</span></span> <span data-ttu-id="a8bcd-112">如果 MSAA 資料是由 Windows Store 應用程式提供者所提供，UIA 用戶端仍然可以讀取資料並將其自動化。</span><span class="sxs-lookup"><span data-stu-id="a8bcd-112">If MSAA data is provided by Windows Store app provider, UIA clients will still be able to read and automate the data.</span></span>

<span data-ttu-id="a8bcd-113">為了簡化 Windows 8Windows Store 應用程式的 API，我們決定只支援將消費者介面自動化作為這些應用程式的用戶端。</span><span class="sxs-lookup"><span data-stu-id="a8bcd-113">To simplify the API for Windows 8Windows Store apps, we decided to support only UI Automation as a client for these apps.</span></span> <span data-ttu-id="a8bcd-114">UIA 用戶端可以原生方式讀取 UIA 提供者，而不會轉譯。</span><span class="sxs-lookup"><span data-stu-id="a8bcd-114">UIA clients can read UIA providers natively, with no translation.</span></span> <span data-ttu-id="a8bcd-115">UIA 用戶端可以讀取 MSAA 提供者，以透過 UIA 對 MSAA Proxy 轉譯。</span><span class="sxs-lookup"><span data-stu-id="a8bcd-115">UIA clients can read MSAA providers as translated through the UIA-to-MSAA Proxy.</span></span> <span data-ttu-id="a8bcd-116">這會降低 Windows Store 應用程式開發人員的測試負擔。</span><span class="sxs-lookup"><span data-stu-id="a8bcd-116">This will reduce the testing burden for Windows Store app developers.</span></span>

<span data-ttu-id="a8bcd-117">消除 MSAA 提供者的支援可進一步減少測試矩陣，但是有主要的應用程式仍然是 MSAA 型，我們不想要將它們轉譯為無法存取。</span><span class="sxs-lookup"><span data-stu-id="a8bcd-117">Eliminating support for MSAA providers would further reduce the testing matrix, but there are major apps that are still MSAA-based and we do not want to render them inaccessible.</span></span>

## <a name="manifestation"></a><span data-ttu-id="a8bcd-118">表現</span><span class="sxs-lookup"><span data-stu-id="a8bcd-118">Manifestation</span></span>

<span data-ttu-id="a8bcd-119">Windows Store 應用程式開發人員將無法在應用程式模型記憶體取 MSAA 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a8bcd-119">Windows Store app developers will not be able to access the details of MSAA within the app model.</span></span>

## <a name="solution"></a><span data-ttu-id="a8bcd-120">解決方法</span><span class="sxs-lookup"><span data-stu-id="a8bcd-120">Solution</span></span>

<span data-ttu-id="a8bcd-121">針對 Windows Store 應用程式的功能，不應在 MSAA 中撰寫新的自動化案例。</span><span class="sxs-lookup"><span data-stu-id="a8bcd-121">No new automated cases should be authored in MSAA for features of Windows Store apps.</span></span>

<span data-ttu-id="a8bcd-122">如果有任何現有的現成可用工具需要與 Windows Store 應用程式互動，請將其切換為 UIA。</span><span class="sxs-lookup"><span data-stu-id="a8bcd-122">Switch any existing in-box tools that use MSAA to UIA if they need to interact with Windows Store apps.</span></span> <span data-ttu-id="a8bcd-123">Windows Store 應用程式開發人員應該使用消費者介面自動化 API。</span><span class="sxs-lookup"><span data-stu-id="a8bcd-123">Windows Store app developers should use the UI Automation API.</span></span>

## <a name="resources"></a><span data-ttu-id="a8bcd-124">資源</span><span class="sxs-lookup"><span data-stu-id="a8bcd-124">Resources</span></span>

-   [<span data-ttu-id="a8bcd-125">UI 自動化基礎</span><span class="sxs-lookup"><span data-stu-id="a8bcd-125">UI Automation Fundamentals</span></span>](../winauto/entry-uiauto-win32.md)

 

 