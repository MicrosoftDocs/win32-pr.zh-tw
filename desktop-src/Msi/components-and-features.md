---
description: Windows Installer 會根據元件和功能的概念來組織安裝。
ms.assetid: c560441e-89c5-4f82-837b-988c3f404d37
title: 元件和功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b21241c98fbb701bd6a3ef5869045ef8c46da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114177"
---
# <a name="components-and-features"></a><span data-ttu-id="2f630-103">元件和功能</span><span class="sxs-lookup"><span data-stu-id="2f630-103">Components and Features</span></span>

<span data-ttu-id="2f630-104">Windows Installer 會根據元件和功能的概念來組織安裝。</span><span class="sxs-lookup"><span data-stu-id="2f630-104">The Windows Installer organizes an installation around the concepts of components and features.</span></span>

<span data-ttu-id="2f630-105">功能是應用程式的總功能的一部分，使用者可能會決定個別安裝。</span><span class="sxs-lookup"><span data-stu-id="2f630-105">A feature is a part of the application's total functionality that a user may decide to install independently.</span></span> <span data-ttu-id="2f630-106">如需詳細資訊，請參閱 [Windows Installer 功能](windows-installer-features.md)。</span><span class="sxs-lookup"><span data-stu-id="2f630-106">For more information, see [Windows Installer Features](windows-installer-features.md).</span></span>

<span data-ttu-id="2f630-107">元件是要安裝的應用程式或產品的一部分。</span><span class="sxs-lookup"><span data-stu-id="2f630-107">A component is a piece of the application or product to be installed.</span></span> <span data-ttu-id="2f630-108">安裝程式一律會從使用者的電腦安裝或移除元件，做為一致的部分。</span><span class="sxs-lookup"><span data-stu-id="2f630-108">The installer always installs or removes a component from a user's computer as a coherent piece.</span></span> <span data-ttu-id="2f630-109">元件通常會隱藏在使用者之外。</span><span class="sxs-lookup"><span data-stu-id="2f630-109">Components are usually hidden from the user.</span></span> <span data-ttu-id="2f630-110">當使用者選取安裝的功能時，安裝程式會決定必須安裝哪些元件才能提供該功能。</span><span class="sxs-lookup"><span data-stu-id="2f630-110">When a user selects a feature for installation, the installer determines which components must be installed to provide that feature.</span></span> <span data-ttu-id="2f630-111">如需詳細資訊，請參閱 [Windows Installer 元件](windows-installer-components.md)。</span><span class="sxs-lookup"><span data-stu-id="2f630-111">For more information, see [Windows Installer Components](windows-installer-components.md).</span></span>

<span data-ttu-id="2f630-112">安裝套件的作者必須決定如何將其應用程式分成功能和元件。</span><span class="sxs-lookup"><span data-stu-id="2f630-112">Authors of installation packages need to decide how to divide their application into features and components.</span></span> <span data-ttu-id="2f630-113">特性的選擇主要取決於應用程式從使用者的觀點來看的功能。</span><span class="sxs-lookup"><span data-stu-id="2f630-113">The selection of features is primarily determined by the application's functionality from the user's perspective.</span></span> <span data-ttu-id="2f630-114">因為通常必須在應用程式之間共用元件，或甚至是在各產品之間共用元件，所以建議作者遵循標準方法來選取元件。</span><span class="sxs-lookup"><span data-stu-id="2f630-114">Because components commonly must be shared across applications, or even across products, it is recommended that authors follow a standard method for selecting components.</span></span> <span data-ttu-id="2f630-115">如需詳細資訊，請參閱將 [應用程式組織成元件](organizing-applications-into-components.md)。</span><span class="sxs-lookup"><span data-stu-id="2f630-115">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

 

 



