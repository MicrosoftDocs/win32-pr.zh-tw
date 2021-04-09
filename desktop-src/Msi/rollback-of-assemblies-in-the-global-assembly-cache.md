---
description: 兩個步驟的程式會將 Windows Installer 的交易模型延伸至包含 common language runtime 元件的產品。 這可讓安裝程式復原失敗的安裝和元件的移除。
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: 全域組件快取中的元件回復
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84bc3107355cb50c17043ee571edff708ba3f6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690236"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a><span data-ttu-id="8af1f-104">全域組件快取中的元件回復</span><span class="sxs-lookup"><span data-stu-id="8af1f-104">Rollback of Assemblies in the Global Assembly Cache</span></span>

<span data-ttu-id="8af1f-105">兩個步驟的程式會將 Windows Installer 的交易模型延伸至包含 common language runtime 元件的產品。</span><span class="sxs-lookup"><span data-stu-id="8af1f-105">A two-step process extends the Windows Installer's transaction model to products containing common language runtime assemblies.</span></span> <span data-ttu-id="8af1f-106">這可讓安裝程式復原失敗的安裝和元件的移除。</span><span class="sxs-lookup"><span data-stu-id="8af1f-106">This enables the installer to rollback unsuccessful installations and removals of assemblies.</span></span>

<span data-ttu-id="8af1f-107">在第一個步驟中，Windows Installer 會使用 Microsoft .NET Framework 為每個元件建立一個介面。</span><span class="sxs-lookup"><span data-stu-id="8af1f-107">During the first step, the Windows Installer uses the Microsoft .NET Framework to create one interface for each assembly.</span></span> <span data-ttu-id="8af1f-108">Windows Installer 使用的介面數目，與安裝的元件數目一樣。</span><span class="sxs-lookup"><span data-stu-id="8af1f-108">The Windows Installer uses as many interfaces as there are assemblies being installed.</span></span> <span data-ttu-id="8af1f-109">使用其中一個介面認可元件，只表示元件已準備好使用相同名稱取代任何現有的元件，但它並不會取代它。</span><span class="sxs-lookup"><span data-stu-id="8af1f-109">Committing an assembly using one of these interfaces only means that the assembly is ready to replace any existing assembly with the same name, it does not yet replace it.</span></span> <span data-ttu-id="8af1f-110">如果使用者取消安裝，或發生嚴重的安裝錯誤，則 Windows Installer 可以藉由釋放這些介面，將元件回復為先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="8af1f-110">If the user cancels the installation, or if there is a fatal installation error, the Windows Installer can still rollback the assembly to its previous state by releasing these interfaces.</span></span>

<span data-ttu-id="8af1f-111">在 Windows Installer 完成安裝所有元件和 Windows Installer 元件之後，安裝程式可能會起始安裝的第二個步驟。</span><span class="sxs-lookup"><span data-stu-id="8af1f-111">After the Windows Installer completes installing all assemblies and Windows Installer components, the installer may initiate the second step of the installation.</span></span> <span data-ttu-id="8af1f-112">第二個步驟會使用個別的函式來執行所有新的 common language runtime 元件的最終認可。</span><span class="sxs-lookup"><span data-stu-id="8af1f-112">The second step uses a separate function to do the final commit of all the new common language runtime assemblies.</span></span> <span data-ttu-id="8af1f-113">這會取代具有相同名稱的任何現有元件。</span><span class="sxs-lookup"><span data-stu-id="8af1f-113">This replaces any existing assemblies with the same name.</span></span>

 

 



