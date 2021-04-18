---
description: Win32 元件可以安裝為私用元件，並且可供一個應用程式使用。 私用元件應該由用來安裝或更新應用程式的 Windows Installer 套件進行安裝。
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: 私用組件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1073426e080cc4b8b30358ce26feb99515abb185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193100"
---
# <a name="private-assemblies"></a><span data-ttu-id="0d3d5-104">私用組件</span><span class="sxs-lookup"><span data-stu-id="0d3d5-104">Private Assemblies</span></span>

<span data-ttu-id="0d3d5-105">Win32 元件可以安裝為私用元件，並且可供一個應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-105">A Win32 assembly can be installed as a private assembly and be exclusively available for use by one application.</span></span> <span data-ttu-id="0d3d5-106">私用元件應該由用來安裝或更新應用程式的 Windows Installer 套件進行安裝。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-106">Private assemblies should be installed by a Windows Installer package used to install or update an application.</span></span>

<span data-ttu-id="0d3d5-107">在 Windows XP 上，私用元件是以 [並存元件](side-by-side-assemblies.md)的形式安裝。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-107">On Windows XP, private assemblies are installed as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="0d3d5-108">Windows Installer 會在應用程式私用的資料夾中安裝私用並存元件。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-108">The Windows Installer installs private side-by-side assemblies in a folder private to the application.</span></span> <span data-ttu-id="0d3d5-109">通常是包含應用程式可執行檔的資料夾。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-109">Commonly the folder that contains the applications executable file.</span></span> <span data-ttu-id="0d3d5-110">私用元件上的應用程式相依性是在應用程式資訊清單檔中指定的。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-110">The dependency of the application on the private assembly is specified in an application manifest file.</span></span> <span data-ttu-id="0d3d5-111">如需詳細資訊，請參閱 [隔離的應用程式和並存元件](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-111">For more information, see [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

<span data-ttu-id="0d3d5-112">在 Windows XP 之前的作業系統上，私用元件和本機檔案的複本會安裝到私人資料夾中，以供應用程式獨佔使用。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-112">On operating systems earlier than Windows XP, a copy of the private assembly and a .local file is installed into a private folder for the exclusive use of the application.</span></span> <span data-ttu-id="0d3d5-113">元件的版本也會在系統上全域註冊，而且可供任何系結至該元件的應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-113">A version of the assembly is also globally registered on the system and available for any application that binds to it.</span></span> <span data-ttu-id="0d3d5-114">元件的全域版本可能是隨應用程式安裝的版本，或是較早的版本。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-114">The global version of the assembly may be the version installed with the application or an earlier version.</span></span> <span data-ttu-id="0d3d5-115">全域版本是由 [獨立元件](isolated-components.md)所使用的相同規則所決定。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-115">The global version is determined by the same rules use by [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="0d3d5-116">請注意，Windows Installer 無法將私用元件安裝在路徑包含超過234個字元的位置，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="0d3d5-116">Note that the Windows Installer cannot install a private assembly in a location having a path that contains more than 234 characters, including the terminating null character.</span></span>

 

 
