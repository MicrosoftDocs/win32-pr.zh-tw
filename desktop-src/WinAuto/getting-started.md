---
title: '開始使用 (Microsoft Active Accessibility) '
description: Microsoft Active Accessibility 是一組元件物件模型 (COM) 介面和 API 元素，可提供可靠的方式來公開和收集 Microsoft Windows UI 元素和 web 內容的相關資訊。
ms.assetid: 13148049-dbb0-4529-b1d7-0c41ebeb7543
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65713143e241a11d29782a4adc0f919ab9ebc3e0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444979"
---
# <a name="getting-started-microsoft-active-accessibility"></a><span data-ttu-id="daa13-103">開始使用 (Microsoft Active Accessibility) </span><span class="sxs-lookup"><span data-stu-id="daa13-103">Getting Started (Microsoft Active Accessibility)</span></span>

<span data-ttu-id="daa13-104">Microsoft Active Accessibility 是一組元件物件模型 (COM) 介面和 API 元素，可提供可靠的方式來公開和收集 Microsoft Windows UI 元素和 web 內容的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="daa13-104">Microsoft Active Accessibility is a set of Component Object Model (COM) interfaces and API elements that provide a reliable way to expose and collect information about Microsoft Windows-based UI elements and web content.</span></span> <span data-ttu-id="daa13-105">使用這項資訊時，輔助技術廠商可以用替代格式（例如語音或盲文）來表示 UI，而語音命令和控制應用程式可以從遠端操作介面。</span><span class="sxs-lookup"><span data-stu-id="daa13-105">Using this information, assistive technology vendors can represent the UI in alternative formats, such as speech or Braille, and voice command and control applications can remotely manipulate the interface.</span></span> <span data-ttu-id="daa13-106">Microsoft Active Accessibility 依賴 Windows 技術，而且只能與 Windows 控制項和其他 Windows 應用程式搭配使用。</span><span class="sxs-lookup"><span data-stu-id="daa13-106">Microsoft Active Accessibility relies on Windows technology and can be used in conjunction only with Windows-based controls and other Windows applications.</span></span>

<span data-ttu-id="daa13-107">這份檔的組織方式，是為了滿足開發人員的新功能，以及熟悉的 Microsoft Active Accessibility 的需求。</span><span class="sxs-lookup"><span data-stu-id="daa13-107">This documentation is organized to meet the needs of developers new to, as well as those familiar with, Microsoft Active Accessibility.</span></span> <span data-ttu-id="daa13-108">檔的主要章節如下所述：</span><span class="sxs-lookup"><span data-stu-id="daa13-108">The major sections of the documentation are described below:</span></span>



|  <span data-ttu-id="daa13-109">區段</span><span class="sxs-lookup"><span data-stu-id="daa13-109">Section</span></span>                                                      |  <span data-ttu-id="daa13-110">描述</span><span class="sxs-lookup"><span data-stu-id="daa13-110">Description</span></span>                                                                                                                                                                 |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="daa13-111">技術總覽</span><span class="sxs-lookup"><span data-stu-id="daa13-111">Technical Overview</span></span>](technical-overview.md)           | <span data-ttu-id="daa13-112">Microsoft Active Accessibility 用戶端和伺服器開發人員的 Microsoft Active Accessibility 和一般方針的總覽。</span><span class="sxs-lookup"><span data-stu-id="daa13-112">Overview of Microsoft Active Accessibility and general guidelines for Microsoft Active Accessibility client and server developers.</span></span>                                |
| [<span data-ttu-id="daa13-113">C/c + + 開發人員指南</span><span class="sxs-lookup"><span data-stu-id="daa13-113">C/C++ Developer's Guide</span></span>](c-c---developer-s-guide.md) | <span data-ttu-id="daa13-114">重要 Microsoft Active Accessibility 應用程式 API 元素和概念的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="daa13-114">In-depth information about the key Microsoft Active Accessibility application API elements and concepts.</span></span> <span data-ttu-id="daa13-115">使用 C 或 c + + 開發人員熟悉的詞彙和範例。</span><span class="sxs-lookup"><span data-stu-id="daa13-115">Uses terms and examples familiar to C or C++ developers.</span></span> |
| [<span data-ttu-id="daa13-116">C/c + + 參考</span><span class="sxs-lookup"><span data-stu-id="daa13-116">C/C++ Reference</span></span>](c-c---reference.md)                 | <span data-ttu-id="daa13-117">所有 Microsoft Active Accessibility 介面、函數、資料類型、資料結構和訊息的完整參考。</span><span class="sxs-lookup"><span data-stu-id="daa13-117">A comprehensive reference for all the Microsoft Active Accessibility interfaces, functions , data types, data structures, and messages.</span></span>                           |
| [<span data-ttu-id="daa13-118">附錄</span><span class="sxs-lookup"><span data-stu-id="daa13-118">Appendixes</span></span>](appendixes.md)                           | <span data-ttu-id="daa13-119">Microsoft Active Accessibility 用戶端、伺服器開發人員和 Microsoft Visual Basicdevelopers 的其他參考資料。</span><span class="sxs-lookup"><span data-stu-id="daa13-119">Additional reference material for Microsoft Active Accessibility client and server developers and Microsoft Visual Basicdevelopers.</span></span>                               |



 

## <a name="in-this-section"></a><span data-ttu-id="daa13-120">本節內容</span><span class="sxs-lookup"><span data-stu-id="daa13-120">In this section</span></span>

-   [<span data-ttu-id="daa13-121">Active Accessibility 元件</span><span class="sxs-lookup"><span data-stu-id="daa13-121">Active Accessibility Components</span></span>](sdk-components.md)
-   [<span data-ttu-id="daa13-122">支援的平臺</span><span class="sxs-lookup"><span data-stu-id="daa13-122">Supported Platforms</span></span>](supported-platforms.md)
-   [<span data-ttu-id="daa13-123">Active Accessibility 和消費者介面自動化</span><span class="sxs-lookup"><span data-stu-id="daa13-123">Active Accessibility and UI Automation</span></span>](active-accessibility-and-ui-automation.md)

 

 




