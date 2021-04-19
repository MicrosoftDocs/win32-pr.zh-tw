---
description: 安裝套件包含安裝或卸載應用程式或產品，以及執行安裝程式使用者介面時，Windows Installer 所需的所有資訊。
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: 安裝套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5e5ff79d0c868036dd12ed533b1cd18f9f70d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976944"
---
# <a name="installation-package"></a><span data-ttu-id="9c33a-103">安裝套件</span><span class="sxs-lookup"><span data-stu-id="9c33a-103">Installation Package</span></span>

<span data-ttu-id="9c33a-104">安裝套件包含安裝或卸載應用程式或產品，以及執行安裝程式使用者介面時，Windows Installer 所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="9c33a-104">An installation package contains all of the information that the Windows Installer requires to install or uninstall an application or product and to run the setup user interface.</span></span> <span data-ttu-id="9c33a-105">每個安裝套件都包含一個 .msi 檔案，其中包含安裝資料庫、摘要資訊資料流程，以及安裝的各部分的資料流程。</span><span class="sxs-lookup"><span data-stu-id="9c33a-105">Each installation package includes an .msi file, containing an installation database, a summary information stream, and data streams for various parts of the installation.</span></span> <span data-ttu-id="9c33a-106">.Msi 檔案也可以包含一或多個轉換、內部原始程式檔，以及安裝所需的外部原始程式檔或封包檔。</span><span class="sxs-lookup"><span data-stu-id="9c33a-106">The .msi file can also contain one or more transforms, internal source files, and external source files or cabinet files required by the installation.</span></span>

<span data-ttu-id="9c33a-107">應用程式開發人員必須撰寫安裝以使用安裝程式。</span><span class="sxs-lookup"><span data-stu-id="9c33a-107">Application developers must author an installation to use the installer.</span></span> <span data-ttu-id="9c33a-108">因為安裝程式會根據 [元件和功能](components-and-features.md)的概念來組織安裝，並且將安裝的所有相關資訊儲存在關係資料庫中，所以撰寫安裝套件的程式會廣泛地牽涉到下列步驟：</span><span class="sxs-lookup"><span data-stu-id="9c33a-108">Because the installer organizes installations around the concept of [components and features](components-and-features.md), and stores all information about the installation in a relational database, the process of authoring an installation package broadly entails the following steps:</span></span>

-   <span data-ttu-id="9c33a-109">識別要呈現給使用者的功能。</span><span class="sxs-lookup"><span data-stu-id="9c33a-109">Identify the features to be presented to users.</span></span>
-   <span data-ttu-id="9c33a-110">將應用程式組織為元件。</span><span class="sxs-lookup"><span data-stu-id="9c33a-110">Organize the application into components.</span></span>
-   <span data-ttu-id="9c33a-111">填入安裝資料庫中的資訊。</span><span class="sxs-lookup"><span data-stu-id="9c33a-111">Populate the installation database with information.</span></span>
-   <span data-ttu-id="9c33a-112">驗證安裝套件。</span><span class="sxs-lookup"><span data-stu-id="9c33a-112">Validate the installation package.</span></span>

<span data-ttu-id="9c33a-113">下一節將討論安裝程式元件和功能。</span><span class="sxs-lookup"><span data-stu-id="9c33a-113">The next section discusses installer components and features.</span></span> <span data-ttu-id="9c33a-114">如需詳細資訊，請參閱 [元件和功能](components-and-features.md)。</span><span class="sxs-lookup"><span data-stu-id="9c33a-114">For more information, see [Components and Features](components-and-features.md).</span></span> <span data-ttu-id="9c33a-115">從使用者的觀點來看，應用程式的功能通常會決定功能的選擇。</span><span class="sxs-lookup"><span data-stu-id="9c33a-115">The choice of features is commonly determined by the application's functionality from the user's perspective.</span></span>

<span data-ttu-id="9c33a-116">建議開發人員使用標準程式來選擇元件。</span><span class="sxs-lookup"><span data-stu-id="9c33a-116">It is recommended that developers use a standard procedure for choosing components.</span></span> <span data-ttu-id="9c33a-117">如需詳細資訊，請參閱將 [應用程式組織成元件](organizing-applications-into-components.md)。</span><span class="sxs-lookup"><span data-stu-id="9c33a-117">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

<span data-ttu-id="9c33a-118">封裝作者可以使用協力廠商套件建立工具或資料表編輯器和 Windows Installer SDK 來填入安裝資料庫。</span><span class="sxs-lookup"><span data-stu-id="9c33a-118">Package authors can use third-party package creation tools, or a table editor and the Windows Installer SDK, to populate the installation database.</span></span> <span data-ttu-id="9c33a-119">所有安裝套件都必須經過驗證，才能進行內部一致性。</span><span class="sxs-lookup"><span data-stu-id="9c33a-119">All installation packages need to be validated for internal consistency.</span></span> <span data-ttu-id="9c33a-120">如需詳細資訊，請參閱 [封裝驗證](package-validation.md)。</span><span class="sxs-lookup"><span data-stu-id="9c33a-120">For more information, see [Package Validation](package-validation.md).</span></span>

 

 



