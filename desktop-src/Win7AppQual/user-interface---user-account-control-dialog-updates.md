---
description: 消費者介面-使用者帳戶控制對話方塊更新
ms.assetid: f2d4b82d-a84a-4fc1-b7ad-cdc92a24f889
title: 消費者介面-使用者帳戶控制對話方塊更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cd6cc6709283c7bd9cba3e26bd2df29bb02ec2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094416"
---
# <a name="user-interface---user-account-control-dialog-updates"></a><span data-ttu-id="fa2dc-103">消費者介面-使用者帳戶控制對話方塊更新</span><span class="sxs-lookup"><span data-stu-id="fa2dc-103">User Interface - User Account Control Dialog Updates</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="fa2dc-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="fa2dc-104">Affected Platforms</span></span>

<span data-ttu-id="fa2dc-105">**客戶** 端-Windows 7</span><span class="sxs-lookup"><span data-stu-id="fa2dc-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="fa2dc-106">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fa2dc-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="fa2dc-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="fa2dc-107">Feature Impact</span></span>

<span data-ttu-id="fa2dc-108">**嚴重性** -低</span><span class="sxs-lookup"><span data-stu-id="fa2dc-108">**Severity** - Low</span></span>  
<span data-ttu-id="fa2dc-109">**頻率** -中型</span><span class="sxs-lookup"><span data-stu-id="fa2dc-109">**Frequency** - Medium</span></span>  











## <a name="description"></a><span data-ttu-id="fa2dc-110">Description</span><span class="sxs-lookup"><span data-stu-id="fa2dc-110">Description</span></span>

<span data-ttu-id="fa2dc-111">在 Windows 7 中，我們已將 UAC 對話方塊的選項標準化。</span><span class="sxs-lookup"><span data-stu-id="fa2dc-111">In Windows 7, we have standardized the UAC dialog box choices.</span></span> <span data-ttu-id="fa2dc-112">之前，使用者必須從多個選項中選取，例如「繼續」、「取消」等等。</span><span class="sxs-lookup"><span data-stu-id="fa2dc-112">Previously, users had to select from multiple options, for example, "Continue," "Cancel," and so on.</span></span> <span data-ttu-id="fa2dc-113">現在所有對話方塊都提供使用者簡單的「是」或「否」。</span><span class="sxs-lookup"><span data-stu-id="fa2dc-113">Now all dialog boxes give users a simple "Yes" or "No."</span></span> <span data-ttu-id="fa2dc-114">對話版面配置現在也清楚地顯示程式名稱、發行者和來源。</span><span class="sxs-lookup"><span data-stu-id="fa2dc-114">The dialog layout now also clearly shows the program name, publisher, and origin.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="fa2dc-115">運用功能功能</span><span class="sxs-lookup"><span data-stu-id="fa2dc-115">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="fa2dc-116">適用于 UAC 相容性的 Windows 7 應用程式開發需求與 Windows Vista 中的相同。</span><span class="sxs-lookup"><span data-stu-id="fa2dc-116">The application development requirements in Windows 7 for UAC compatibility are the same as in Windows Vista.</span></span> <span data-ttu-id="fa2dc-117">Windows Vista 相容的應用程式將會與 Windows 7 中的 UAC 互動，而不需要任何修改。</span><span class="sxs-lookup"><span data-stu-id="fa2dc-117">Windows Vista-compatible applications will interact with UAC in Windows 7 without any modifications.</span></span> <span data-ttu-id="fa2dc-118">請參閱《 *Windows Vista 應用程式相容性手冊* 》中的「使用者帳戶控制」主題，以取得如何讓 windows XP 應用程式在 windows 7 上正常運作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fa2dc-118">See the User Account Control topics in the *Windows Vista Application Compatibility Cookbook* for information about how to make Windows XP applications work correctly on Windows 7.</span></span> <span data-ttu-id="fa2dc-119">雖然 Windows 7 的 UAC 增強功能會影響使用者體驗，但不會影響應用程式介面。</span><span class="sxs-lookup"><span data-stu-id="fa2dc-119">While the UAC improvements for Windows 7 will impact the user's experience, they will not impact the application interface.</span></span> <span data-ttu-id="fa2dc-120">但是，如果有任何連結至 UAC 對話方塊的說明內容，您可能需要更新螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="fa2dc-120">However, if there is any help content linked to the UAC dialogs, you may need to update the screenshots.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="fa2dc-121">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="fa2dc-121">Links to Other Resources</span></span>

-   <span data-ttu-id="fa2dc-122">[Windows Vista 應用程式相容性操作手冊](/previous-versions/bb757005(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="fa2dc-122">[Windows Vista Application Compatibility Cookbook](/previous-versions/bb757005(v=msdn.10))</span></span>
-   [<span data-ttu-id="fa2dc-123">應用程式相容性工具組下載</span><span class="sxs-lookup"><span data-stu-id="fa2dc-123">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="fa2dc-124">[標準使用者分析器](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="fa2dc-124">[Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span></span>

> [!Note]  
> <span data-ttu-id="fa2dc-125">這些資源可能無法在某些語言及國家/地區中使用。</span><span class="sxs-lookup"><span data-stu-id="fa2dc-125">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
