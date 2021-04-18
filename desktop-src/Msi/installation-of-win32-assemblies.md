---
description: 將 Win32 元件設為 Microsoft Windows Installer 套件的元件，以安裝或更新您的應用程式。
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Win32 元件的安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d47847c0c69185a28fa41bbe5c5a05deec1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983365"
---
# <a name="installation-of-win32-assemblies"></a><span data-ttu-id="9165b-103">Win32 元件的安裝</span><span class="sxs-lookup"><span data-stu-id="9165b-103">Installation of Win32 Assemblies</span></span>

<span data-ttu-id="9165b-104">將 Win32 元件設為 Microsoft Windows Installer 套件的元件，以安裝或更新您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9165b-104">Install Win32 assemblies by making them a component of Microsoft Windows Installer package that installs or updates your application.</span></span> <span data-ttu-id="9165b-105">當您撰寫 [MsiAssembly 資料表](msiassembly-table.md) 和 [MsiAssemblyName 資料表](msiassemblyname-table.md)時，這會將元件資料行中的元件識別 \_ 為元件。</span><span class="sxs-lookup"><span data-stu-id="9165b-105">When you author the [MsiAssembly table](msiassembly-table.md) and [MsiAssemblyName table](msiassemblyname-table.md), this identifies the component in the Component\_ column as an assembly.</span></span> <span data-ttu-id="9165b-106">安裝程式會將 [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) 屬性設定為可支援 Win32 元件的作業系統上 Sxs.dll 的檔案版本，否則不會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="9165b-106">The installer will set the [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) property to the file version of Sxs.dll on operating systems that can support Win32 assemblies and not set this property otherwise.</span></span>

<span data-ttu-id="9165b-107">在 Windows Vista 和 Windows XP 中，Windows Installer 不會將元件資訊寫入登錄中。</span><span class="sxs-lookup"><span data-stu-id="9165b-107">In Windows Vista and Windows XP, Windows Installer does not write assembly information into the registry.</span></span> <span data-ttu-id="9165b-108">此外，也可以使用共用元件、私用元件和並存元件。</span><span class="sxs-lookup"><span data-stu-id="9165b-108">In addition, shared assemblies, private assemblies, and side-by-side assemblies can be used.</span></span> <span data-ttu-id="9165b-109">如需詳細資訊，請參閱 [共用元件](shared-assemblies.md)、 [私用元件](private-assemblies.md)和 [並存元件](side-by-side-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="9165b-109">For information, see [Shared Assemblies](shared-assemblies.md), [Private Assemblies](private-assemblies.md), and [Side-by-Side Assemblies](side-by-side-assemblies.md).</span></span>

<span data-ttu-id="9165b-110">下列章節說明如何撰寫 Windows Installer 套件，以在不同的 Windows 作業系統上，將 Win32 元件安裝為共用、私用或並存。</span><span class="sxs-lookup"><span data-stu-id="9165b-110">The following sections describe how to author a Windows Installer package to install Win32 assemblies as shared, private, or side-by-side on different Windows operating systems.</span></span>

-   [<span data-ttu-id="9165b-111">在 Windows XP 上安裝適用于並存共用的 Win32 元件</span><span class="sxs-lookup"><span data-stu-id="9165b-111">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [<span data-ttu-id="9165b-112">在 Windows XP 上安裝 Win32 元件以私用應用程式</span><span class="sxs-lookup"><span data-stu-id="9165b-112">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



