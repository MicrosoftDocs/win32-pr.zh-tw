---
title: WPD 程式設計指南
description: 此程式設計指南著重于如何使用介面中找到的 WPD 介面和方法來完成範例工作。
ms.assetid: 87777b0b-a7a0-4032-99bb-92b717d3c452
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db13d50942c28cd4937d27a745d61d7a30a01a15
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409861"
---
# <a name="wpd-programming-guide"></a><span data-ttu-id="095d3-103">WPD 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="095d3-103">WPD programming guide</span></span>

<span data-ttu-id="095d3-104">此程式設計指南的主要來源是 Windows 可攜式裝置 (WPD) 軟體發展工具組 (SDK) 隨附的範例。</span><span class="sxs-lookup"><span data-stu-id="095d3-104">The primary source for this programming guide is a sample that ships with the Windows Portable Devices (WPD) Software Development Kit (SDK).</span></span> <span data-ttu-id="095d3-105">這個名為 WpdApiSample.exe 的範例包含七個 .cpp 模組。</span><span class="sxs-lookup"><span data-stu-id="095d3-105">This sample, named WpdApiSample.exe, consists of seven .cpp modules.</span></span> <span data-ttu-id="095d3-106">其中六個模組包含的程式碼會示範應用程式可使用 WPD 應用程式設計介面完成的26個工作 (API) 。</span><span class="sxs-lookup"><span data-stu-id="095d3-106">Six of these modules contain the code that demonstrates 26 tasks that an application can accomplish using the WPD application programming interface (API).</span></span>

<span data-ttu-id="095d3-107">上述的例外狀況是描述的主題：裝置服務工作、內容功能表和屬性工作表延伸;這些主題並非取自 WpdApiSample。</span><span class="sxs-lookup"><span data-stu-id="095d3-107">The exceptions to the above are the topics that describe: device service tasks, the context menu and property sheet extensions; these topics were not taken from WpdApiSample.</span></span> <span data-ttu-id="095d3-108">裝置服務工作是以名為 WpdServiceApiSample 的範例為基礎。</span><span class="sxs-lookup"><span data-stu-id="095d3-108">The device service tasks are based on the sample named WpdServiceApiSample.</span></span> <span data-ttu-id="095d3-109">內容功能表和屬性工作表延伸模組是取自未隨附于 Windows SDK 的應用程式的程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="095d3-109">The context menu and property sheet extensions are snippets taken from applications that do not ship with the Windows SDK.</span></span>

<span data-ttu-id="095d3-110">下列各節將焦點放在這些範例所完成的工作，並說明如何使用 WPD 介面和這些介面中找到的一些方法來完成每一個作業。</span><span class="sxs-lookup"><span data-stu-id="095d3-110">The following sections focus on the tasks accomplished by these samples and explain how each is accomplished using the WPD interfaces and a number of the methods found in these interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="095d3-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="095d3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="095d3-112">**Windows 可攜式裝置**</span><span class="sxs-lookup"><span data-stu-id="095d3-112">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
