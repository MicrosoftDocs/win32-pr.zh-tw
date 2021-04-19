---
description: 復原是指應用程式從遺失重要元件，或已被不相容版本取代的情況下，能夠正常復原的能力。
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: 災害復原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d57e5c5a342a8e1c295afd97a69fe2828362a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975245"
---
# <a name="resiliency"></a><span data-ttu-id="ac889-103">災害復原</span><span class="sxs-lookup"><span data-stu-id="ac889-103">Resiliency</span></span>

<span data-ttu-id="ac889-104">復原是指應用程式從遺失重要元件，或已被不相容版本取代的情況下，能夠正常復原的能力。</span><span class="sxs-lookup"><span data-stu-id="ac889-104">Resiliency is the ability of an application to recover gracefully from situations in which a vital component is missing, or has been replaced by an incompatible version.</span></span> <span data-ttu-id="ac889-105">藉由撰寫安裝套件並使用 [安裝程式功能](installer-functions.md)，開發人員可以使用 Windows Installer 來產生可從這類情況復原的復原應用程式。</span><span class="sxs-lookup"><span data-stu-id="ac889-105">By authoring an installation package and using the [Installer Functions](installer-functions.md), developers can use the Windows Installer to produce resilient applications capable of recovering from such situations.</span></span>

-   <span data-ttu-id="ac889-106">使用安裝程式的來源清單來提高依賴網路資源的應用程式的復原能力。</span><span class="sxs-lookup"><span data-stu-id="ac889-106">Use the installer's source list to increase the resiliency of applications that rely on network resources.</span></span> <span data-ttu-id="ac889-107">如需詳細資訊，請參閱 [來源復原](source-resiliency.md)。</span><span class="sxs-lookup"><span data-stu-id="ac889-107">For more information, see [Source Resiliency](source-resiliency.md).</span></span>
-   <span data-ttu-id="ac889-108">使用安裝程式的 API 來檢查是否已安裝重要功能、元件、檔案或檔案版本。</span><span class="sxs-lookup"><span data-stu-id="ac889-108">Use the installer's API to check whether a vital feature, component, file, or file version is installed.</span></span>
-   <span data-ttu-id="ac889-109">使用安裝程式的 API，在執行時間檢查元件的路徑。</span><span class="sxs-lookup"><span data-stu-id="ac889-109">Use the installer's API to check the path to a component at run time.</span></span> <span data-ttu-id="ac889-110">這可減少應用程式對靜態檔案路徑的相依性，這通常會在電腦之間有所不同。</span><span class="sxs-lookup"><span data-stu-id="ac889-110">This reduces your application's dependency on static file paths, which commonly differ between computers.</span></span>
-   <span data-ttu-id="ac889-111">您可以使用安裝程式來重新安裝損毀的快捷方式、登錄專案和其他元件，而不需要重新執行安裝程式。</span><span class="sxs-lookup"><span data-stu-id="ac889-111">Use the installer to reinstall damaged shortcuts, registry entries, and other components without having to rerun setup.</span></span>
-   <span data-ttu-id="ac889-112">藉由讓安裝程式的復原功能保持啟用，來提高產品安裝的復原能力。</span><span class="sxs-lookup"><span data-stu-id="ac889-112">Increase the resiliency of your product's installation by leaving the rollback capability of the installer enabled.</span></span> <span data-ttu-id="ac889-113">如需詳細資訊，請參閱 [復原安裝](rollback-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="ac889-113">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

 

 



