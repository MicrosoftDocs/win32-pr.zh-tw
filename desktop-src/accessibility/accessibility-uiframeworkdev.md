---
description: 概述可併入 UI 架構的 Windows 協助工具功能。
title: 開發適用於 Windows 的無障礙 UI 架構
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 9083bdb8b9c7ab9dd7dd30c675a72fafa4c065c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111464"
---
# <a name="developing-accessible-ui-frameworks-for-windows"></a><span data-ttu-id="3817b-103">開發適用於 Windows 的無障礙 UI 架構</span><span class="sxs-lookup"><span data-stu-id="3817b-103">Developing accessible UI frameworks for Windows</span></span>

<span data-ttu-id="3817b-104">為了盡可能地使用，針對 Windows 平臺所建立的 UI 架構應該支援協助工具功能，讓殘障人士、個人喜好設定或特定工作樣式的使用者可以更輕鬆地使用其 Windows 裝置。</span><span class="sxs-lookup"><span data-stu-id="3817b-104">To be usable by as many people as possible, UI frameworks built for the Windows platform should support accessibility features that make it easier for those with disabilities, personal preferences, or specific work styles to use their Windows devices successfully.</span></span>

<span data-ttu-id="3817b-105">本總覽說明如何建立支援功能的 UI 架構，例如程式設計存取和自動化、鍵盤流覽和命令、色彩和主題選項，以及透過使用者設定進行個人化。</span><span class="sxs-lookup"><span data-stu-id="3817b-105">This overview describes how to build a UI framework that supports features such as programmatic access and automation, keyboard navigation and commanding, color and theme options, and personalization through user settings.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3817b-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="3817b-106">In this section</span></span>

- [<span data-ttu-id="3817b-107">適用于 Win32 的消費者介面自動化</span><span class="sxs-lookup"><span data-stu-id="3817b-107">UI Automation for Win32</span></span>](/windows/desktop/winauto/entry-uiauto-win32)
- [<span data-ttu-id="3817b-108">鍵盤協助工具</span><span class="sxs-lookup"><span data-stu-id="3817b-108">Keyboard accessibility</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
- [<span data-ttu-id="3817b-109">尊重高對比</span><span class="sxs-lookup"><span data-stu-id="3817b-109">Respecting High Contrast</span></span>](/windows/desktop/w8cookbook/high-contrast-mode)
- [<span data-ttu-id="3817b-110">使用者設定</span><span class="sxs-lookup"><span data-stu-id="3817b-110">User settings</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
- [<span data-ttu-id="3817b-111">使用者設定的 blog 文章</span><span class="sxs-lookup"><span data-stu-id="3817b-111">User settings blog post</span></span>](https://devblogs.microsoft.com/oldnewthing/?p=36243)

<span data-ttu-id="3817b-112">範例</span><span class="sxs-lookup"><span data-stu-id="3817b-112">Samples</span></span>

- [<span data-ttu-id="3817b-113">消費者介面自動化 WPF Framework 執行範例</span><span class="sxs-lookup"><span data-stu-id="3817b-113">UI Automation WPF Framework Implementation sample</span></span>](https://github.com/Microsoft/WPF-Samples/tree/master/Accessibility)
- <span data-ttu-id="3817b-114">[UI 對比和設定範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/UI%20contrast%20and%20settings%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="3817b-114">[UI contrast and settings sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/UI%20contrast%20and%20settings%20sample%20(Windows%208))</span></span>
