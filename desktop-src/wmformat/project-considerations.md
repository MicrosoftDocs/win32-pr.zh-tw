---
title: 專案考慮
description: 專案考慮
ms.assetid: aebe2886-0af0-443a-a5be-651f11936639
keywords:
- Windows Media Format SDK，專案考慮
- Advanced Systems Format (ASF) 、專案考慮
- ASF (Advanced Systems Format) ，專案考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1682e8008569c9b230b2c2f53f394326669d022
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184059"
---
# <a name="project-considerations"></a><span data-ttu-id="8764f-106">專案考慮</span><span class="sxs-lookup"><span data-stu-id="8764f-106">Project Considerations</span></span>

<span data-ttu-id="8764f-107">您必須確保終端使用者可以正確地執行您使用 Windows Media Format SDK 建立的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8764f-107">You must ensure that the end user can properly run applications that you create with the Windows Media Format SDK.</span></span> <span data-ttu-id="8764f-108">本節說明散發應用程式、副檔名和軟體轉散發時，必須考慮的兩件事。</span><span class="sxs-lookup"><span data-stu-id="8764f-108">This section describes two things you must consider when distributing applications, file name extensions and software redistribution.</span></span>

<span data-ttu-id="8764f-109">您必須針對使用您的應用程式所建立的任何檔案，使用正確的副檔名。</span><span class="sxs-lookup"><span data-stu-id="8764f-109">You must use the correct file name extensions for any files created with your applications.</span></span> <span data-ttu-id="8764f-110">使用適當的副檔名，讓使用者更容易辨識 ASF 檔案，並在解碼檔案時防止混淆。</span><span class="sxs-lookup"><span data-stu-id="8764f-110">Using proper file name extensions makes it easier for end users to recognize ASF files and prevents confusion when decoding files.</span></span>

<span data-ttu-id="8764f-111">您必須提供執行應用程式所需的任何可轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="8764f-111">You must provide any redistributables that are required to run your applications.</span></span> <span data-ttu-id="8764f-112">如果沒有正確的可轉散發套件，使用者將無法使用您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8764f-112">Without the correct redistributables, users will not be able to use your applications.</span></span>

<span data-ttu-id="8764f-113">下列各節詳細說明副檔名和軟體重新發佈。</span><span class="sxs-lookup"><span data-stu-id="8764f-113">The following sections describe file name extensions and software redistribution in detail.</span></span>



| <span data-ttu-id="8764f-114">區段</span><span class="sxs-lookup"><span data-stu-id="8764f-114">Section</span></span>                                                                      | <span data-ttu-id="8764f-115">描述</span><span class="sxs-lookup"><span data-stu-id="8764f-115">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8764f-116">檔案名延伸指導方針</span><span class="sxs-lookup"><span data-stu-id="8764f-116">File Name Extension Guidelines</span></span>](file-name-extension-guidelines.md)         | <span data-ttu-id="8764f-117">提供有關您的程式所建立之 ASF 檔案所應使用之副檔名的資訊。</span><span class="sxs-lookup"><span data-stu-id="8764f-117">Provides information about the file name extensions you should use for ASF files that your program creates.</span></span>     |
| [<span data-ttu-id="8764f-118">軟體轉散發</span><span class="sxs-lookup"><span data-stu-id="8764f-118">Software Redistribution</span></span>](software-redistribution.md)                       | <span data-ttu-id="8764f-119">說明 Windows Media Format SDK 的可轉散發套件，以及如何將它們包含在您的應用程式中。</span><span class="sxs-lookup"><span data-stu-id="8764f-119">Describes the redistributables for the Windows Media Format SDK and how to include them with your applications.</span></span> |
| [<span data-ttu-id="8764f-120">註冊應用程式相依性</span><span class="sxs-lookup"><span data-stu-id="8764f-120">Registering Application Dependency</span></span>](registering-application-dependency.md) | <span data-ttu-id="8764f-121">說明如何註冊您的應用程式，使其相依于 Windows Media Format SDK 執行時間。</span><span class="sxs-lookup"><span data-stu-id="8764f-121">Describes how to register your application as being dependent on the Windows Media Format SDK runtime.</span></span>          |



 

 

 




