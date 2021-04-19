---
description: 共用元件是可供電腦上的多個應用程式使用的元件。
ms.assetid: E42688E0-83D8-4C64-98A8-1BE82E4348FA
title: 關於共用元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed044f2c0f6b8e8e04927035991da651b4c26674
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979780"
---
# <a name="about-shared-assemblies"></a><span data-ttu-id="3a8a6-103">關於共用元件</span><span class="sxs-lookup"><span data-stu-id="3a8a6-103">About Shared Assemblies</span></span>

<span data-ttu-id="3a8a6-104">共用元件是可供電腦上的多個應用程式使用的元件。</span><span class="sxs-lookup"><span data-stu-id="3a8a6-104">A shared assembly is an assembly available for use by multiple applications on the computer.</span></span> <span data-ttu-id="3a8a6-105">在 Windows Vista 和 Windows XP 上， [並存元件](about-side-by-side-assemblies-.md) 可以安裝為共用的元件。</span><span class="sxs-lookup"><span data-stu-id="3a8a6-105">On Windows Vista and Windows XP, [side-by-side assemblies](about-side-by-side-assemblies-.md) can be installed as shared assemblies.</span></span> <span data-ttu-id="3a8a6-106">共用並存元件並不會在系統上進行全域登錄，但在 [資訊清單](manifests.md)中指定對元件之相依性的應用程式可全域使用。</span><span class="sxs-lookup"><span data-stu-id="3a8a6-106">Shared side-by-side assemblies are not registered globally on the system, but they are globally available to applications that specify a dependence on the assembly in [manifests](manifests.md).</span></span> <span data-ttu-id="3a8a6-107">並行元件的多個版本可由同時執行的不同應用程式共用。</span><span class="sxs-lookup"><span data-stu-id="3a8a6-107">Multiple versions of side-by-side assemblies can be shared by different applications running at the same time.</span></span> <span data-ttu-id="3a8a6-108">如需詳細資訊，請參閱 [關於隔離應用程式和並存元件](about-isolated-applications-and-side-by-side-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="3a8a6-108">For more information, see [About Isolated Applications and Side-by-Side Assemblies](about-isolated-applications-and-side-by-side-assemblies.md).</span></span> <span data-ttu-id="3a8a6-109">例如，隨附于 Windows XP 的 [支援 Microsoft 並存元件](supported-microsoft-side-by-side-assemblies.md) ，通常是由多個應用程式用來作為共用的元件。</span><span class="sxs-lookup"><span data-stu-id="3a8a6-109">For example, the [supported Microsoft side-by-side assemblies](supported-microsoft-side-by-side-assemblies.md) shipped with Windows XP are typically used as shared assemblies by multiple applications.</span></span>

<span data-ttu-id="3a8a6-110">共用並存元件會安裝在 WinSxS 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="3a8a6-110">Shared side-by-side assemblies are installed in the WinSxS folder.</span></span> <span data-ttu-id="3a8a6-111">元件發行者、應用程式和系統管理員 [可以在部署](configuration.md)完成之後，變更並存元件相依性的版本。</span><span class="sxs-lookup"><span data-stu-id="3a8a6-111">Assembly publishers, applications, and administrators can change the version of side-by-side assembly dependencies after deployment through the [configuration](configuration.md).</span></span> <span data-ttu-id="3a8a6-112">共用並存元件可以由作業系統更新或安裝或更新應用程式的 Windows Installer 套件來安裝。</span><span class="sxs-lookup"><span data-stu-id="3a8a6-112">Shared side-by-side assemblies can be installed by an operating system update, or by a Windows Installer package that installs or updates an application.</span></span> <span data-ttu-id="3a8a6-113">如需詳細資訊，請參閱 [Win32 元件的安裝](../msi/installation-of-win32-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="3a8a6-113">For more information, see [Installation of Win32 Assemblies](../msi/installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="3a8a6-114">在 Windows XP 之前，共用的元件是全域註冊的，並且安裝在 Windows 系統資料夾中。</span><span class="sxs-lookup"><span data-stu-id="3a8a6-114">Prior to Windows XP, shared assemblies were registered globally and installed in the Windows System folder.</span></span> <span data-ttu-id="3a8a6-115">在此情況下，元件的最新安裝版本可供任何系結至該元件的應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="3a8a6-115">In this case, the latest installed version of the assembly is available to any application that binds to it.</span></span> <span data-ttu-id="3a8a6-116">並存元件也可以安裝為私用元件，以用於應用程式的專屬用途。</span><span class="sxs-lookup"><span data-stu-id="3a8a6-116">A side-by-side assembly can also be installed as a private assembly for the exclusive use of an application.</span></span> <span data-ttu-id="3a8a6-117">如需詳細資訊，請參閱 [私用組件](/windows/desktop/Msi/private-assemblies)。</span><span class="sxs-lookup"><span data-stu-id="3a8a6-117">For more information, see [Private Assemblies](/windows/desktop/Msi/private-assemblies).</span></span>

 

 
