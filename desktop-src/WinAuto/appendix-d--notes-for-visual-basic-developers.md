---
title: Visual Basic 開發人員的附錄 D 附注
description: 本節提供 Microsoft Visual Basic 開發人員 Microsoft Active Accessibility 的相關資訊。
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc09c23a81b2f987a6f651a923dd10b0d16a2a27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932158"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a><span data-ttu-id="bdceb-103">附錄 D： Visual Basic 開發人員的注意事項</span><span class="sxs-lookup"><span data-stu-id="bdceb-103">Appendix D: Notes for Visual Basic Developers</span></span>

<span data-ttu-id="bdceb-104">本節提供 Microsoft Visual Basic 開發人員 Microsoft Active Accessibility 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bdceb-104">This section provides information about Microsoft Active Accessibility for Microsoft Visual Basic developers.</span></span>

<span data-ttu-id="bdceb-105">以 Visual Basic 撰寫的應用程式 Microsoft Active Accessibility 用戶端。</span><span class="sxs-lookup"><span data-stu-id="bdceb-105">Applications written in Visual Basic are Microsoft Active Accessibility clients.</span></span> <span data-ttu-id="bdceb-106">它們不會提供其自訂使用者介面專案的相關資訊，因為它們不會執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 或任何其他元件物件模型 (COM) 介面。</span><span class="sxs-lookup"><span data-stu-id="bdceb-106">They do not provide information about their custom user interface elements because they do not implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) or any other Component Object Model (COM) interface.</span></span>

<span data-ttu-id="bdceb-107">本檔使用 C/c + + 名稱作為 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性;不過，Visual Basic 名稱很類似。</span><span class="sxs-lookup"><span data-stu-id="bdceb-107">This documentation uses the C/C++ names for the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties; however, the Visual Basic names are similar.</span></span> <span data-ttu-id="bdceb-108">例如， [**IAccessible：： get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) 屬性在 Visual Basic 應用程式中會被稱為 **accName** 。</span><span class="sxs-lookup"><span data-stu-id="bdceb-108">For example, the [**IAccessible::get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) property would be called **accName** in a Visual Basic application.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bdceb-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="bdceb-109">In this section</span></span>

-   [<span data-ttu-id="bdceb-110">Visual Basic 方法附注： accName</span><span class="sxs-lookup"><span data-stu-id="bdceb-110">Visual Basic Method Notes: accName</span></span>](visual-basic-method-notes--accname.md)
-   [<span data-ttu-id="bdceb-111">Visual Basic 方法附注： accValue</span><span class="sxs-lookup"><span data-stu-id="bdceb-111">Visual Basic Method Notes: accValue</span></span>](visual-basic-method-notes--accvalue.md)
-   [<span data-ttu-id="bdceb-112">Visual Basic 範例程式</span><span class="sxs-lookup"><span data-stu-id="bdceb-112">Visual Basic Sample Programs</span></span>](visual-basic-sample-programs.md)

 

 




