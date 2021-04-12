---
description: .
ms.assetid: fb2c487a-d395-45eb-9010-936a61a414d0
title: Windows 疑難排解
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eacea2f4f62852da7fbaefd51db5834907a323ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320831"
---
# <a name="windows-troubleshooting"></a><span data-ttu-id="4b47e-103">Windows 疑難排解</span><span class="sxs-lookup"><span data-stu-id="4b47e-103">Windows Troubleshooting</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="4b47e-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="4b47e-104">Affected Platforms</span></span>

<span data-ttu-id="4b47e-105">**客戶** 端-Windows 7</span><span class="sxs-lookup"><span data-stu-id="4b47e-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="4b47e-106">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4b47e-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="description"></a><span data-ttu-id="4b47e-107">Description</span><span class="sxs-lookup"><span data-stu-id="4b47e-107">Description</span></span>

<span data-ttu-id="4b47e-108">新的 Windows 7 動作中心 (前身為解決方案中心) 功能，Windows 疑難排解，為使用者提供系統化的疑難排解體驗。</span><span class="sxs-lookup"><span data-stu-id="4b47e-108">A new Windows 7 Action Center (formerly known as Solutions Center) feature, Windows Troubleshooting, delivers a systematic troubleshooting experience for the user.</span></span> <span data-ttu-id="4b47e-109">動作中心是釘選在工作列中的五個圖示之一。</span><span class="sxs-lookup"><span data-stu-id="4b47e-109">The Action Center is one of the five icons pinned in the systray.</span></span> <span data-ttu-id="4b47e-110">Windows 疑難排解可讓您流覽或搜尋內建的疑難排解套件，以及針對網際網路上 Microsoft 伺服器上儲存的疑難排解套件，在連線 (BWC) 體驗時更好。</span><span class="sxs-lookup"><span data-stu-id="4b47e-110">Windows Troubleshooting allows you to browse or search for in-box troubleshooting packs and for troubleshooting packs that are stored on a Microsoft server on the Internet – a Better When Connected (BWC) experience.</span></span> <span data-ttu-id="4b47e-111">您可以選取並執行疑難排解套件，以嘗試解決其問題。</span><span class="sxs-lookup"><span data-stu-id="4b47e-111">You can select and run a troubleshooting pack to attempt to resolve their problem.</span></span> <span data-ttu-id="4b47e-112">如果您無法找出問題的解決方法，可以選擇搜尋說明、社區內容和支援文章，或其他相關內容的疑難排解套件。</span><span class="sxs-lookup"><span data-stu-id="4b47e-112">If you cannot identify a resolution to the problem, you have the option of searching help, community content, and support articles, or other troubleshooting packs for relevant related content.</span></span> <span data-ttu-id="4b47e-113">若未提供問題的解答，您可以將電腦還原到問題發生之前的時間，或透過遠端協助取得協助。</span><span class="sxs-lookup"><span data-stu-id="4b47e-113">Should that not provide an answer to the problem, you can restore the PC to a time prior to when the problem occurred or get help through remote assistance.</span></span> <span data-ttu-id="4b47e-114">其目的是讓您能夠輕鬆快速地找到問題的解決方案。</span><span class="sxs-lookup"><span data-stu-id="4b47e-114">The intent is to allow you to find a solution to the problem easily and quickly.</span></span>

## <a name="usage"></a><span data-ttu-id="4b47e-115">使用方式</span><span class="sxs-lookup"><span data-stu-id="4b47e-115">Usage</span></span>

<span data-ttu-id="4b47e-116">您可以從數個位置清楚地看見並提供動作中心。</span><span class="sxs-lookup"><span data-stu-id="4b47e-116">The Action Center is clearly visible and available from several locations.</span></span> <span data-ttu-id="4b47e-117">您可以從 [控制台] 中的 [動作中心] 的操作功能表，從 [控制台] 的 [系統和維護] 下的快捷方式連結、從 [動作中心] 的主頁面，以及從 [說明內容] 啟動它。</span><span class="sxs-lookup"><span data-stu-id="4b47e-117">You can launch it from the context menu of the Action Center in the systray, from the control panel as a shortcut link under system and maintenance, from the main page of the Action Center, and from Help content.</span></span>

<span data-ttu-id="4b47e-118">疑難排解套件是以 powershell 腳本為基礎。</span><span class="sxs-lookup"><span data-stu-id="4b47e-118">Troubleshooting packs are based upon powershell scripts.</span></span> <span data-ttu-id="4b47e-119">撰寫和發佈疑難排解套件的程式會公開，讓 Oem、Ihv、Isv 和 IT 專業人員開發和傳送自己的疑難排解內容。</span><span class="sxs-lookup"><span data-stu-id="4b47e-119">The process of authoring and publishing a troubleshooting pack will be made public to allow OEMs, IHVs, ISVs, and IT Professionals to develop and ship their own troubleshooting content.</span></span>

<span data-ttu-id="4b47e-120">針對一致的使用者體驗，請務必遵循 Windows 疑難排解工具組中所述的最佳作法和指導方針，以設計您自己的疑難排解套件。</span><span class="sxs-lookup"><span data-stu-id="4b47e-120">For a consistent user experience, be sure to follow the best practices and guidelines described in the Windows troubleshooting toolkit when designing your own troubleshooting packs.</span></span>

 

 



