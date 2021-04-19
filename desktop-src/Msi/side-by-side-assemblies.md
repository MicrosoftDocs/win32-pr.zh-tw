---
description: 並存元件共用是一種基礎結構，用來執行下列作業：安全地在多個 applicationsOffset 之間共用元件。共用的負面影響，例如 DLL 衝突。
ms.assetid: ba73e7c3-a9d7-4cc3-b5ce-2483a594fcc0
title: 並存元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da0493b9d16d3943053b32a8a06eaa371cfd1d79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990315"
---
# <a name="side-by-side-assemblies"></a><span data-ttu-id="8dbcd-103">並存元件</span><span class="sxs-lookup"><span data-stu-id="8dbcd-103">Side-by-Side Assemblies</span></span>

<span data-ttu-id="8dbcd-104">並存元件共用是一種基礎結構，可用來執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="8dbcd-104">Side-by-Side assembly sharing is an infrastructure that is used to do the following:</span></span>

-   <span data-ttu-id="8dbcd-105">安全地在多個應用程式之間共用元件</span><span class="sxs-lookup"><span data-stu-id="8dbcd-105">Safely share assemblies among multiple applications</span></span>
-   <span data-ttu-id="8dbcd-106">位移一些共用的負面影響，例如 DLL 衝突。</span><span class="sxs-lookup"><span data-stu-id="8dbcd-106">Offset some negative effects of sharing, for example, DLL conflicts.</span></span>

<span data-ttu-id="8dbcd-107">除了具有單一版本的元件（假設與所有應用程式的回溯相容性）之外，並存元件共用也可讓多個版本的 COM 或 Win32 元件在系統上同時執行。</span><span class="sxs-lookup"><span data-stu-id="8dbcd-107">Instead of having a single version of an assembly that assumes backward compatibility with all applications, side-by-side assembly sharing enables multiple versions of a COM or Win32 assembly to run simultaneously on a system.</span></span> <span data-ttu-id="8dbcd-108">如需詳細資訊，請參閱 [隔離的應用程式和並存元件](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="8dbcd-108">For more information, see [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

<span data-ttu-id="8dbcd-109">並存元件可以安裝為 [共用元件](shared-assemblies.md) 或 [私用元件](private-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="8dbcd-109">Side-by-Side Assemblies can be installed as [Shared Assemblies](shared-assemblies.md) or as [Private Assemblies](private-assemblies.md).</span></span>

<span data-ttu-id="8dbcd-110">在 Windows XP 之前的系統上無法使用並存元件。</span><span class="sxs-lookup"><span data-stu-id="8dbcd-110">Side-by-Side Assemblies are not available on systems earlier than Windows XP.</span></span>

 

 
