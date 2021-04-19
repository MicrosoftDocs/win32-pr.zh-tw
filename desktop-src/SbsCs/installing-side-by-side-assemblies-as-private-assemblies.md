---
description: 若要安裝並存元件做為私用元件，您可以將元件安裝為安裝程式套件的元件。
ms.assetid: 1cfd836f-a1b9-4339-8756-5488c88b3c2b
title: 將並存元件安裝為私用元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7719a9887f9e92d81e2ad65fe2e75424f0b6957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973037"
---
# <a name="installing-side-by-side-assemblies-as-private-assemblies"></a><span data-ttu-id="419d6-103">將並存元件安裝為私用元件</span><span class="sxs-lookup"><span data-stu-id="419d6-103">Installing Side-by-side Assemblies as Private Assemblies</span></span>

<span data-ttu-id="419d6-104">若要安裝 [並存](about-side-by-side-assemblies-.md) 元件做為私用 [元件](/windows/desktop/Msi/private-assemblies)，您可以將元件安裝為安裝程式套件的元件。</span><span class="sxs-lookup"><span data-stu-id="419d6-104">To install [side-by-side assemblies](about-side-by-side-assemblies-.md) as [private assemblies](/windows/desktop/Msi/private-assemblies), you can install the assembly as a component of an installer package.</span></span> <span data-ttu-id="419d6-105">這可以是用來安裝或更新應用程式的相同安裝套件。</span><span class="sxs-lookup"><span data-stu-id="419d6-105">This can be the same installation package used to install or update your application.</span></span> <span data-ttu-id="419d6-106">安裝元件需要 Windows Installer 2.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="419d6-106">Windows Installer version 2.0 or later is required to install assemblies.</span></span> <span data-ttu-id="419d6-107">如需詳細資訊，請參閱 [Windows Installer](../msi/windows-installer-portal.md) SDK 和 [Win32 元件安裝](../msi/installation-of-win32-assemblies.md)中的章節。</span><span class="sxs-lookup"><span data-stu-id="419d6-107">For more information, see the [Windows Installer](../msi/windows-installer-portal.md) SDK and the sections under [Installation of Win32 Assemblies](../msi/installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="419d6-108">或者，您可以使用安裝程式，將私用元件和資訊清單複製到與應用程式可執行檔相同的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="419d6-108">As an alternative, you can use the installer to copy a private assembly and manifest into the same folder as the application's executable file.</span></span>

 

 
