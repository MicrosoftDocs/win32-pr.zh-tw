---
description: Windows UI 可讓使用者存取執行應用程式和管理作業系統所需的各種物件。
title: Shell 開發人員指南
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1be17ca90b7138294be3e1b34fa3fcb4dcb4227a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991150"
---
# <a name="shell-developers-guide"></a><span data-ttu-id="cb9fc-103">Shell 開發人員指南</span><span class="sxs-lookup"><span data-stu-id="cb9fc-103">Shell Developer's Guide</span></span>

<span data-ttu-id="cb9fc-104">Windows UI 可讓使用者存取執行應用程式和管理作業系統所需的各種物件。</span><span class="sxs-lookup"><span data-stu-id="cb9fc-104">The Windows UI provides users with access to a wide variety of objects necessary to run applications and manage the operating system.</span></span> <span data-ttu-id="cb9fc-105">這些物件最多與熟悉的是位於電腦磁片磁碟機上的資料夾和檔案。</span><span class="sxs-lookup"><span data-stu-id="cb9fc-105">The most numerous and familiar of these objects are the folders and files that reside on computer disk drives.</span></span> <span data-ttu-id="cb9fc-106">另外還有一些虛擬物件，可讓使用者進行工作，例如將檔案傳送至遠端印表機或存取資源回收筒。</span><span class="sxs-lookup"><span data-stu-id="cb9fc-106">There are also a number of virtual objects that allow the user to do tasks such as sending files to remote printers or accessing the Recycle Bin.</span></span> <span data-ttu-id="cb9fc-107">Shell 會將這些物件組織成階層命名空間，並為使用者和應用程式提供一致且有效率的方式來存取和管理物件。</span><span class="sxs-lookup"><span data-stu-id="cb9fc-107">The Shell organizes these objects into a hierarchical namespace, and provides users and applications with a consistent and efficient way to access and manage objects.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cb9fc-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="cb9fc-108">In this section</span></span>

-   [<span data-ttu-id="cb9fc-109">安全性考慮： Microsoft Windows Shell</span><span class="sxs-lookup"><span data-stu-id="cb9fc-109">Security Considerations: Microsoft Windows Shell</span></span>](sec-shell.md)
-   [<span data-ttu-id="cb9fc-110">執行擴充功能的指引 In-Process</span><span class="sxs-lookup"><span data-stu-id="cb9fc-110">Guidance for Implementing In-Process Extensions</span></span>](shell-and-managed-code.md)
-   [<span data-ttu-id="cb9fc-111">Shell 和通用控制項版本</span><span class="sxs-lookup"><span data-stu-id="cb9fc-111">Shell and Common Controls Versions</span></span>](versions.md)
-   [<span data-ttu-id="cb9fc-112">執行基本資料夾物件介面</span><span class="sxs-lookup"><span data-stu-id="cb9fc-112">Implementing the Basic Folder Object Interfaces</span></span>](nse-implement.md)
-   [<span data-ttu-id="cb9fc-113">執行自訂檔案格式</span><span class="sxs-lookup"><span data-stu-id="cb9fc-113">Implementing a Custom File Format</span></span>](customizing-file-types-bumper.md)
-   [<span data-ttu-id="cb9fc-114">Shell 擴充性 (建立資料來源) </span><span class="sxs-lookup"><span data-stu-id="cb9fc-114">Shell Extensibility (Creating a Data Source)</span></span>](shell-extensibility-bumper.md)
-   [<span data-ttu-id="cb9fc-115">執行主控台專案</span><span class="sxs-lookup"><span data-stu-id="cb9fc-115">Implementing Control Panel Items</span></span>](control-panel-applications.md)
-   [<span data-ttu-id="cb9fc-116">支援 Shell 應用程式</span><span class="sxs-lookup"><span data-stu-id="cb9fc-116">Supporting Shell Applications</span></span>](application-support-bumper.md)
-   [<span data-ttu-id="cb9fc-117">舊版 Shell 主題</span><span class="sxs-lookup"><span data-stu-id="cb9fc-117">Legacy Shell Topics</span></span>](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a><span data-ttu-id="cb9fc-118">文件慣例</span><span class="sxs-lookup"><span data-stu-id="cb9fc-118">Document Conventions</span></span>

<span data-ttu-id="cb9fc-119">Shell 開發人員指南遵循一般 Windows 軟體開發套件 (SDK) 檔慣例。</span><span class="sxs-lookup"><span data-stu-id="cb9fc-119">The Shell Developers's Guide follows the usual Windows Software Development Kit (SDK) document conventions.</span></span> <span data-ttu-id="cb9fc-120">請特別注意兩個慣例：</span><span class="sxs-lookup"><span data-stu-id="cb9fc-120">Two conventions in particular should be noted:</span></span>

-   <span data-ttu-id="cb9fc-121">範例程式碼會省略正常的錯誤修正程式碼。</span><span class="sxs-lookup"><span data-stu-id="cb9fc-121">Sample code omits normal error-correction code.</span></span> <span data-ttu-id="cb9fc-122">這段程式碼已移除，使程式碼更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="cb9fc-122">This code has been removed only to make the code more readable.</span></span> <span data-ttu-id="cb9fc-123">您應該在自己的應用程式中包含所有適當的錯誤修正程式碼。</span><span class="sxs-lookup"><span data-stu-id="cb9fc-123">You should include all appropriate error-correction code in your own applications.</span></span>
-   <span data-ttu-id="cb9fc-124">若要清除範例登錄專案，請使用標準字型來顯示機碼、子機碼和專案名稱以及值。</span><span class="sxs-lookup"><span data-stu-id="cb9fc-124">To make sample registry entries clear, key, subkey, and entry names as well as values are displayed with a standard font.</span></span> <span data-ttu-id="cb9fc-125">使用者或應用程式定義的專案名稱為斜體。</span><span class="sxs-lookup"><span data-stu-id="cb9fc-125">User or application-defined item names are italicized.</span></span>

 

 



