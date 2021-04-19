---
description: 家長監護 Top-Level 消費者介面
ms.assetid: c6dfd3bc-191f-42d1-b9de-cc85a2da0a99
title: 家長監護 Top-Level 消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321475097e25b812aca8d1e65f8b88843ebb1055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977946"
---
# <a name="parental-controls-top-level-user-interface"></a><span data-ttu-id="2765f-103">家長監護 Top-Level 消費者介面</span><span class="sxs-lookup"><span data-stu-id="2765f-103">Parental Controls Top-Level User Interface</span></span>

<span data-ttu-id="2765f-104">系列安全與 Windows 使用者帳戶之間的增強式連結，在 Windows Vista 的取用者導向 Sku 主控台中，會以 **使用者帳戶和家庭安全** 的形式出現在相同的組合類別中。</span><span class="sxs-lookup"><span data-stu-id="2765f-104">The strong link between Family Safety and Windows user accounts has driven a combined category appearing as **User Accounts and Family Safety** in Control Panel for consumer-oriented SKUs of Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="2765f-105">當聯結了具有網域加入功能的電腦時，類別目錄會顯示為 **使用者帳戶** 。</span><span class="sxs-lookup"><span data-stu-id="2765f-105">The category will appear as **User Accounts** when a computer with domain-join capability is joined.</span></span>

 

<span data-ttu-id="2765f-106">如果尚未為受控制的使用者設定標準使用者帳戶，主控台中的連結會提供簡單的工作流程，以新增新的 parentally 控制帳戶。</span><span class="sxs-lookup"><span data-stu-id="2765f-106">If a standard user account has not yet been set up for the controlled user, a link in Control Panel provides a simple workflow for adding a new parentally controlled account.</span></span>

<span data-ttu-id="2765f-107">建立帳戶之後，[家長監護] 主控台會為受控制的使用者公開最上層的使用者面向功能。</span><span class="sxs-lookup"><span data-stu-id="2765f-107">After an account is created, the Parental Controls Control Panel exposes the top-level user-facing functionality for the controlled user.</span></span> <span data-ttu-id="2765f-108">元素：</span><span class="sxs-lookup"><span data-stu-id="2765f-108">Elements:</span></span>

-   <span data-ttu-id="2765f-109">整體家長監護會控制選項按鈕的限制。</span><span class="sxs-lookup"><span data-stu-id="2765f-109">Overall Parental Controls restrictions on or off radio buttons.</span></span>
-   <span data-ttu-id="2765f-110">獨立活動報告開啟或關閉控制選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="2765f-110">Independent Activity Reporting on or off control radio buttons.</span></span>
-   <span data-ttu-id="2765f-111">[設定] 區段中會有條件地顯示 Microsoft 所執行的 Web 限制連結，並顯示可用的核心離線 Microsoft 執行的限制類型。</span><span class="sxs-lookup"><span data-stu-id="2765f-111">A Settings section with the Microsoft-implemented Web Restrictions link conditionally shown, and available core offline Microsoft-implemented restrictions types shown.</span></span>
-   <span data-ttu-id="2765f-112">當 Microsoft 或協力廠商註冊消費者介面延伸模組時，會出現 [其他設定] 區域。</span><span class="sxs-lookup"><span data-stu-id="2765f-112">A More Settings area that appears if User Interface extensions are registered by Microsoft or third parties.</span></span>
-   <span data-ttu-id="2765f-113">摘要狀態區域，顯示使用者名稱和磚、[View activity reports] 連結，以及 [家長監護] 設定的狀態。</span><span class="sxs-lookup"><span data-stu-id="2765f-113">A summary status area showing the user name and tile, the View activity reports link, and the state of Parental Controls settings.</span></span> <span data-ttu-id="2765f-114">如果開啟，則顯示會包含 Web 內容篩選器設定層級 (如果 Microsoft 篩選準則為使用中) 或篩選名稱（如果是由協力廠商延伸模組覆寫），以及使用者的離線設定狀態。</span><span class="sxs-lookup"><span data-stu-id="2765f-114">If on, the display includes the Web Content Filter setting level (if the Microsoft filter is active) or filter name if overridden by a third-party extension, and state of offline settings for the user.</span></span>

<span data-ttu-id="2765f-115">整體家長監護 [啟用] 選項按鈕一開始會設定為 [關閉] 狀態。</span><span class="sxs-lookup"><span data-stu-id="2765f-115">The overall Parental Controls enable radio button is initially set to the off state.</span></span> <span data-ttu-id="2765f-116">當系統管理員開啟時，預設也會開啟活動報告，但可能會獨立關閉。</span><span class="sxs-lookup"><span data-stu-id="2765f-116">When turned on by an administrator, Activity Reporting will also be on by default, but may be turned off independently.</span></span> <span data-ttu-id="2765f-117">如同家長監護中幾乎所有的設定，設定可能會透過可用的 Api 以程式設計方式執行。</span><span class="sxs-lookup"><span data-stu-id="2765f-117">As with nearly all settings in Parental Controls, configuration may be performed programmatically through the available APIs.</span></span>

 

 



