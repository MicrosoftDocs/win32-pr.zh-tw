---
title: Windows 環境
description: Windows 環境是 Windows 所提供的螢幕上的工作區，類似于實體桌面，以及作業系統的核心擴充點。
ms.assetid: 9485459D-AE46-43D1-941C-3B5EE784391F
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 1cb6e731f2bccb7b2f9508432ec63754f177eafc
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106975584"
---
# <a name="windows-environment"></a><span data-ttu-id="638b7-103">Windows 環境</span><span class="sxs-lookup"><span data-stu-id="638b7-103">Windows Environment</span></span>

> [!NOTE]
> <span data-ttu-id="638b7-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="638b7-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="638b7-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="638b7-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="638b7-106">Windows 環境是 Windows 所提供的螢幕上的工作區，類似于實體桌面，以及作業系統的核心擴充點。</span><span class="sxs-lookup"><span data-stu-id="638b7-106">The Windows environment is the onscreen work area provided by Windows, analogous to a physical desktop, and the operating system's core extension points.</span></span> <span data-ttu-id="638b7-107">瞭解如何利用應用程式的桌面、工作列、通知區域、控制台、說明和使用者帳戶控制。</span><span class="sxs-lookup"><span data-stu-id="638b7-107">Learn how to leverage the desktop, taskbar, notification area, control panels, help, and user account control for your app.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="638b7-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="638b7-108">In this section</span></span>



| <span data-ttu-id="638b7-109">主題</span><span class="sxs-lookup"><span data-stu-id="638b7-109">Topic</span></span>                                                   | <span data-ttu-id="638b7-110">描述</span><span class="sxs-lookup"><span data-stu-id="638b7-110">Description</span></span>                                                                                                                                                                                                               |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="638b7-111">桌上型電腦</span><span class="sxs-lookup"><span data-stu-id="638b7-111">Desktop</span></span>](winenv-desktop.md)<br/>                | <span data-ttu-id="638b7-112">桌面是其程式的使用者工作區。</span><span class="sxs-lookup"><span data-stu-id="638b7-112">The desktop is the user's work area for their programs.</span></span> <span data-ttu-id="638b7-113">它無法提升您對程式或其品牌的認知。</span><span class="sxs-lookup"><span data-stu-id="638b7-113">It's not a way to promote awareness of your program or its brand.</span></span> <span data-ttu-id="638b7-114">不要濫用！</span><span class="sxs-lookup"><span data-stu-id="638b7-114">Don't abuse it!</span></span> <br/>                                                                     |
| [<span data-ttu-id="638b7-115">工作列</span><span class="sxs-lookup"><span data-stu-id="638b7-115">Taskbar</span></span>](winenv-taskbar.md)<br/>                | <span data-ttu-id="638b7-116">工作列是顯示在桌面上的程式存取點。</span><span class="sxs-lookup"><span data-stu-id="638b7-116">The taskbar is the access point for programs displayed on the desktop.</span></span> <span data-ttu-id="638b7-117">透過新的 Windows 7 工作列功能，使用者可以直接從工作列提供命令、存取資源，以及查看程式狀態。</span><span class="sxs-lookup"><span data-stu-id="638b7-117">With the new Windows 7 taskbar features, users can give commands, access resources, and view program status directly from the taskbar.</span></span> <br/> |
| [<span data-ttu-id="638b7-118">通知區域</span><span class="sxs-lookup"><span data-stu-id="638b7-118">Notification Area</span></span>](winenv-notification.md)<br/> | <span data-ttu-id="638b7-119">通知區域會提供通知和狀態。</span><span class="sxs-lookup"><span data-stu-id="638b7-119">The notification area provides notifications and status.</span></span> <span data-ttu-id="638b7-120">設計完善的程式會適當地使用通知區域，而不會干擾或困擾。</span><span class="sxs-lookup"><span data-stu-id="638b7-120">Well-designed programs use the notification area appropriately, without being annoying or distracting.</span></span> <br/>                                               |
| [<span data-ttu-id="638b7-121">控制台</span><span class="sxs-lookup"><span data-stu-id="638b7-121">Control Panels</span></span>](winenv-ctrl-panels.md)<br/>     | <span data-ttu-id="638b7-122">使用控制台專案來協助使用者設定系統層級的功能，並執行相關工作。</span><span class="sxs-lookup"><span data-stu-id="638b7-122">Use control panel items to help users configure system-level features and perform related tasks.</span></span> <span data-ttu-id="638b7-123">具有使用者介面的程式應該改為從其 UI 直接設定。</span><span class="sxs-lookup"><span data-stu-id="638b7-123">Programs that have a user interface should be configured directly from their UI instead.</span></span> <br/>                     |
| [<span data-ttu-id="638b7-124">說明</span><span class="sxs-lookup"><span data-stu-id="638b7-124">Help</span></span>](winenv-help.md)<br/>                      | <span data-ttu-id="638b7-125">使用「說明」做為次要機制，以協助使用者完成及更瞭解主要機制成為 UI 本身的工作。</span><span class="sxs-lookup"><span data-stu-id="638b7-125">Use Help as a secondary mechanism to help users complete and better understand tasks the primary mechanism being the UI itself.</span></span> <span data-ttu-id="638b7-126">套用這些指導方針，讓內容真正實用且容易找到。</span><span class="sxs-lookup"><span data-stu-id="638b7-126">Apply these guidelines to make the content truly helpful and easy to find.</span></span> <br/>    |
| [<span data-ttu-id="638b7-127">使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="638b7-127">User Account Control</span></span>](winenv-uac.md)<br/>       | <span data-ttu-id="638b7-128">設計完善的使用者帳戶控制體驗，可協助您以可預測的方式來避免不必要的全系統變更，並需要進行極低的努力。</span><span class="sxs-lookup"><span data-stu-id="638b7-128">A well designed User Account Control experience helps prevent unwanted system-wide changes in a way that is predictable and requires minimal effort.</span></span> <br/>                                                          |



 

 

