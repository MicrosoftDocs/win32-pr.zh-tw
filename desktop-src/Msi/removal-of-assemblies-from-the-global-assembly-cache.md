---
description: Windows Installer 會根據用戶端清單，決定是否允許移除通用語言執行時間元件，它會獨立于元件之外。
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: 從全域組件快取移除元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d50bc2856891c67952a27b27a27cf1cf2d1d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192777"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a><span data-ttu-id="032b1-103">從全域組件快取移除元件</span><span class="sxs-lookup"><span data-stu-id="032b1-103">Removal of Assemblies from the Global Assembly Cache</span></span>

<span data-ttu-id="032b1-104">Windows Installer 會根據用戶端清單，決定是否允許移除通用語言執行時間元件，它會獨立于元件之外。</span><span class="sxs-lookup"><span data-stu-id="032b1-104">The Windows Installer determines whether to allow the removal of a common language runtime assembly based upon a client list it keeps independently of the assembly.</span></span> <span data-ttu-id="032b1-105">Windows Installer 會保留一個 pin 位來代表元件 Windows Installer 的用戶端。</span><span class="sxs-lookup"><span data-stu-id="032b1-105">The Windows Installer keeps one pin bit to represent Windows Installer clients of the assembly.</span></span> <span data-ttu-id="032b1-106">安裝程式會釘選第一個 Windows Installer 用戶端的元件，並在移除最後一個 Windows Installer 用戶端時取消固定它。</span><span class="sxs-lookup"><span data-stu-id="032b1-106">The installer pins the assembly for the first Windows Installer client and unpins it when the last Windows Installer client is removed.</span></span> <span data-ttu-id="032b1-107">元件會為元件的每個用戶端維護一個 pin 位。</span><span class="sxs-lookup"><span data-stu-id="032b1-107">The assembly maintains a pin bit for every client of an assembly.</span></span>

<span data-ttu-id="032b1-108">Windows Installer 不會直接負責從電腦實際移除 common language runtime 元件。</span><span class="sxs-lookup"><span data-stu-id="032b1-108">The Windows Installer is not directly responsible for the physical removal of common language runtime assemblies from the computer.</span></span> <span data-ttu-id="032b1-109">移除最後一個 Windows Installer 用戶端時，安裝程式會取消固定元件。</span><span class="sxs-lookup"><span data-stu-id="032b1-109">The installer unpins the assembly when the last Windows Installer client is removed.</span></span> <span data-ttu-id="032b1-110">如果 Windows Installer 是元件的最後一個用戶端，則 common language runtime 會提供強制同步清除元件的選項。</span><span class="sxs-lookup"><span data-stu-id="032b1-110">If the Windows Installer is the last client of the assembly, the common language runtime provides the option to force a synchronous cleanup of the assembly.</span></span> <span data-ttu-id="032b1-111">清除程式是不可部分完成的，此時不會提供「復原」。</span><span class="sxs-lookup"><span data-stu-id="032b1-111">The cleanup process is atomic and there is no provision for a "rollback" at this point.</span></span> <span data-ttu-id="032b1-112">當使用者有機會取消安裝或移除時，所有的 common language runtime 元件解除釘選都必須執行。</span><span class="sxs-lookup"><span data-stu-id="032b1-112">All unpinning of common language runtime assemblies must occur after the user has had a chance to cancel the installation or removal.</span></span>

 

 



