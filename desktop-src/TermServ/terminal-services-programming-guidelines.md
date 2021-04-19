---
title: 遠端桌面服務程式設計指導方針
description: 本主題提供在遠端桌面服務環境中開發應用程式的指導方針。
ms.assetid: e0cd52c5-40d7-4a48-9d10-fdbcea46a5a0
ms.tgt_platform: multiple
keywords:
- 遠端桌面服務遠端桌面服務，程式設計指導方針
- 程式設計指導方針遠端桌面服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e767740a2f279c90ce4f0eb37c49919749465ad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968705"
---
# <a name="remote-desktop-services-programming-guidelines"></a><span data-ttu-id="abae3-105">遠端桌面服務程式設計指導方針</span><span class="sxs-lookup"><span data-stu-id="abae3-105">Remote Desktop Services programming guidelines</span></span>

<span data-ttu-id="abae3-106">大部分現有的32位或64位 Windows 架構應用程式會在先前稱為終端機服務) 環境的遠端桌面服務 (中以相同的方式執行。</span><span class="sxs-lookup"><span data-stu-id="abae3-106">Most existing 32-bit or 64-bit Windows-based applications run "as is" in a Remote Desktop Services (formerly known as Terminal Services) environment.</span></span> <span data-ttu-id="abae3-107">不過，有些應用程式在遠端桌面服務環境中正常運作並正常運作，而有些則沒有。</span><span class="sxs-lookup"><span data-stu-id="abae3-107">However, some applications function correctly and perform well in a Remote Desktop Services environment, while others do not.</span></span> <span data-ttu-id="abae3-108">下列主題提供在遠端桌面服務環境中開發應用程式的指導方針。</span><span class="sxs-lookup"><span data-stu-id="abae3-108">The following topics provide guidelines for developing applications in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="abae3-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="abae3-109">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="abae3-110">多使用者指導方針</span><span class="sxs-lookup"><span data-stu-id="abae3-110">Multiple-user guidelines</span></span>](multiple-user-guidelines.md)
</dt> <dd>

<span data-ttu-id="abae3-111">在遠端桌面服務環境中為多個使用者開發應用程式的指導方針。</span><span class="sxs-lookup"><span data-stu-id="abae3-111">Guidelines for developing applications for multiple users in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="abae3-112">效能指導方針</span><span class="sxs-lookup"><span data-stu-id="abae3-112">Performance guidelines</span></span>](performance-guidelines.md)
</dt> <dd>

<span data-ttu-id="abae3-113">開發在遠端桌面服務環境中順利執行之應用程式的指導方針。</span><span class="sxs-lookup"><span data-stu-id="abae3-113">Guidelines for developing applications that perform well in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="abae3-114">一般程式設計指導方針</span><span class="sxs-lookup"><span data-stu-id="abae3-114">General programming guidelines</span></span>](general-programming-guidelines.md)
</dt> <dd>

<span data-ttu-id="abae3-115">在遠端桌面服務環境中開發應用程式的指導方針。</span><span class="sxs-lookup"><span data-stu-id="abae3-115">Guidelines for developing applications in a Remote Desktop Services environment.</span></span>

</dd> </dl>

<span data-ttu-id="abae3-116">其中許多指導方針都是良好的程式設計實務，可受益于在任何 Windows 環境中執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="abae3-116">Many of these guidelines are good programming practices that will benefit applications running in any Windows environment.</span></span> <span data-ttu-id="abae3-117">不過，某些建議的優化（例如限制圖形效果）是優化，只有在您的應用程式在遠端桌面服務下執行時，才會想要優化。</span><span class="sxs-lookup"><span data-stu-id="abae3-117">However, some recommended optimizations, such as limiting graphic effects, are optimizations that you would want only when your application is running under Remote Desktop Services.</span></span> <span data-ttu-id="abae3-118">如需說明如何偵測遠端桌面服務環境的程式碼範例，請參閱偵測 [遠端桌面服務環境](detecting-the-terminal-services-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="abae3-118">For a code example that shows how to detect a Remote Desktop Services environment, see [Detecting the Remote Desktop Services Environment](detecting-the-terminal-services-environment.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="abae3-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="abae3-119">Related topics</span></span>

<dl> <span data-ttu-id="abae3-120"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="abae3-120"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="abae3-121">終端機服務現在遠端桌面服務</span><span class="sxs-lookup"><span data-stu-id="abae3-121">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[<span data-ttu-id="abae3-122">系統管理範本檔案格式</span><span class="sxs-lookup"><span data-stu-id="abae3-122">Administrative Template File Format</span></span>](/previous-versions/windows/desktop/Policy/administrative-template-file-format)
</dt> <dt>

[<span data-ttu-id="abae3-123">登錄機碼安全性與存取權限</span><span class="sxs-lookup"><span data-stu-id="abae3-123">Registry Key Security and Access Rights</span></span>](/windows/desktop/SysInfo/registry-key-security-and-access-rights)
</dt> <dt>

[<span data-ttu-id="abae3-124">登錄 hive</span><span class="sxs-lookup"><span data-stu-id="abae3-124">Registry Hives</span></span>](/windows/desktop/SysInfo/registry-hives)
</dt> <dt>

[<span data-ttu-id="abae3-125">安全性描述項</span><span class="sxs-lookup"><span data-stu-id="abae3-125">Security Descriptors</span></span>](/windows/desktop/SecAuthZ/security-descriptors)
</dt> <dt>

[<span data-ttu-id="abae3-126">標準存取權限</span><span class="sxs-lookup"><span data-stu-id="abae3-126">Standard Access Rights</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[<span data-ttu-id="abae3-127">存取控制模型</span><span class="sxs-lookup"><span data-stu-id="abae3-127">Access Control Model</span></span>](/windows/desktop/SecAuthZ/access-control-model)
</dt> </dl>

 

 