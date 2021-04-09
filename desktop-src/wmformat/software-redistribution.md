---
title: 軟體轉散發
description: 軟體轉散發
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- Windows Media Format SDK，軟體轉散發
- Advanced Systems Format (ASF) 、軟體轉散發
- ASF (Advanced Systems Format) ，軟體轉散發
- Windows Media Format SDK，轉散發
- Advanced Systems Format (ASF) ，轉散發
- ASF (Advanced Systems Format) ，轉散發
- 軟體轉散發，關於
- 轉散發，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d51f332f5b0e038293a1dbe1dbf59015931d67e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672516"
---
# <a name="software-redistribution"></a><span data-ttu-id="d2e5d-111">軟體轉散發</span><span class="sxs-lookup"><span data-stu-id="d2e5d-111">Software Redistribution</span></span>

<span data-ttu-id="d2e5d-112">在應用程式安裝程式中包含 Windows Media Format 軟體稱為「轉散發」。</span><span class="sxs-lookup"><span data-stu-id="d2e5d-112">The inclusion of Windows Media Format software in an application setup is known as redistribution.</span></span> <span data-ttu-id="d2e5d-113">Windows Media Format SDK 包含可在應用程式安裝程式中包含的安裝套件。</span><span class="sxs-lookup"><span data-stu-id="d2e5d-113">The Windows Media Format SDK includes an installation package which can be included with your application setup.</span></span> <span data-ttu-id="d2e5d-114">安裝套件是名為 wmfdist95.exe 的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="d2e5d-114">The installation package is an executable file named wmfdist95.exe.</span></span> <span data-ttu-id="d2e5d-115">當您安裝 Windows Media Format SDK 時，安裝套件會複製到安裝目錄的可轉散發套件 \\ 資料夾 (c： \\ wmsdk \\ wmfsdk 預設為) 。</span><span class="sxs-lookup"><span data-stu-id="d2e5d-115">When you install the Windows Media Format SDK, the installation package is copied to the \\Redist folder of the install directory (c:\\wmsdk\\wmfsdk by default).</span></span>

<span data-ttu-id="d2e5d-116">下列各節提供軟體轉散發設定的程式和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="d2e5d-116">The following sections provide procedures and other information for software redistribution setup.</span></span>



| <span data-ttu-id="d2e5d-117">區段</span><span class="sxs-lookup"><span data-stu-id="d2e5d-117">Section</span></span>                                                                            | <span data-ttu-id="d2e5d-118">描述</span><span class="sxs-lookup"><span data-stu-id="d2e5d-118">Description</span></span>                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e5d-119">若要建立轉散發設定</span><span class="sxs-lookup"><span data-stu-id="d2e5d-119">To Create a Redistribution Setup</span></span>](to-create-a-redistribution-setup.md)           | <span data-ttu-id="d2e5d-120">說明建立應用程式安裝程式的程式。</span><span class="sxs-lookup"><span data-stu-id="d2e5d-120">Describes the procedure for creating an application setup.</span></span>                                                                                                                       |
| [<span data-ttu-id="d2e5d-121">偵測安裝狀態</span><span class="sxs-lookup"><span data-stu-id="d2e5d-121">Detecting Setup Status</span></span>](detecting-setup-status.md)                               | <span data-ttu-id="d2e5d-122">提供的範例程式碼會檢查登錄中的安裝狀態，以判斷是否需要安裝轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="d2e5d-122">Provides example code that checks the registry for installation status to determine whether the redistribution package needs to be installed.</span></span>                                    |
| [<span data-ttu-id="d2e5d-123">轉散發設定的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="d2e5d-123">Example Code for Redistribution Setup</span></span>](example-code-for-redistribution-setup.md) | <span data-ttu-id="d2e5d-124">提供範例程式碼，可在您的安裝程式常式中用來以無訊息模式執行轉散發套件，並在電腦必須重新開機時通知您的設定常式。</span><span class="sxs-lookup"><span data-stu-id="d2e5d-124">Provides example code that can be used in your setup routine to run the redistribution packages in quiet mode and notify your setup routine when the computer must be restarted.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d2e5d-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2e5d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2e5d-126">**專案考慮**</span><span class="sxs-lookup"><span data-stu-id="d2e5d-126">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




