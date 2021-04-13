---
description: 如何註冊 DirectShow 篩選器
ms.assetid: 2b6304c0-4b67-4723-94a0-7b1fff534f91
title: 如何註冊 DirectShow 篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301f26884115526e25e8875867f7cc2bdc628698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385681"
---
# <a name="how-to-register-directshow-filters"></a><span data-ttu-id="00034-103">如何註冊 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="00034-103">How to Register DirectShow Filters</span></span>

<span data-ttu-id="00034-104">本文說明如何讓 Microsoft DirectShow 篩選器自行註冊。</span><span class="sxs-lookup"><span data-stu-id="00034-104">This article describes how to make a Microsoft DirectShow filter self-registering.</span></span> <span data-ttu-id="00034-105">它包含下列區段：</span><span class="sxs-lookup"><span data-stu-id="00034-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="00034-106">登錄機碼的版面配置</span><span class="sxs-lookup"><span data-stu-id="00034-106">Layout of the Registry Keys</span></span>](layout-of-the-registry-keys.md)
-   [<span data-ttu-id="00034-107">宣告篩選資訊</span><span class="sxs-lookup"><span data-stu-id="00034-107">Declaring Filter Information</span></span>](declaring-filter-information.md)
-   [<span data-ttu-id="00034-108">宣告 Factory 範本</span><span class="sxs-lookup"><span data-stu-id="00034-108">Declaring the Factory Template</span></span>](declaring-the-factory-template.md)
-   [<span data-ttu-id="00034-109">執行 DllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="00034-109">Implementing DllRegisterServer</span></span>](implementing-dllregisterserver.md)
-   [<span data-ttu-id="00034-110">註冊篩選準則的指導方針</span><span class="sxs-lookup"><span data-stu-id="00034-110">Guidelines for Registering Filters</span></span>](guidelines-for-registering-filters.md)
-   [<span data-ttu-id="00034-111">取消註冊篩選</span><span class="sxs-lookup"><span data-stu-id="00034-111">Unregistering a Filter</span></span>](unregistering-a-filter.md)

<span data-ttu-id="00034-112">本文不會說明如何建立 DirectShow 篩選器的 DLL。</span><span class="sxs-lookup"><span data-stu-id="00034-112">This article does not describe how to create a DLL for a DirectShow filter.</span></span> <span data-ttu-id="00034-113">如需建立 Dll 的詳細資訊，請參閱 [如何建立 DirectShow 篩選 DLL](how-to-create-a-dll.md)。</span><span class="sxs-lookup"><span data-stu-id="00034-113">For information on creating DLLs, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00034-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="00034-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00034-115">DirectShow 和 COM</span><span class="sxs-lookup"><span data-stu-id="00034-115">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



