---
title: 伺服器指導方針
description: 若要讓 Microsoft Active Accessibility 依照設計的方式運作，伺服器必須提供協助工具資訊給用戶端。
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344721428c94e2ea3d9e9ff78e194851ba9304db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371953"
---
# <a name="server-guidelines"></a><span data-ttu-id="86137-103">伺服器指導方針</span><span class="sxs-lookup"><span data-stu-id="86137-103">Server Guidelines</span></span>

<span data-ttu-id="86137-104">若要讓 Microsoft Active Accessibility 依照設計的方式運作，伺服器必須提供協助工具資訊給用戶端。</span><span class="sxs-lookup"><span data-stu-id="86137-104">For Microsoft Active Accessibility to work as designed, servers must provide accessibility information to clients.</span></span>

<span data-ttu-id="86137-105">若要執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)，伺服器開發人員必須遵循此基本流程。</span><span class="sxs-lookup"><span data-stu-id="86137-105">To implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), server developers must follow this basic process.</span></span>

1.  <span data-ttu-id="86137-106">為您的自訂使用者介面專案和應用程式的用戶端，執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法，以建立可存取的物件。</span><span class="sxs-lookup"><span data-stu-id="86137-106">Create accessible objects by implementing the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods for your custom user interface elements and for your application's client.</span></span> <span data-ttu-id="86137-107">請務必提供同時支援 **IAccessible** 和 [**IDispatch**](idispatch-interface.md) 的雙重介面，讓以 Microsoft Visual Basic 撰寫的用戶端和各種指令碼語言可以取得物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="86137-107">Be sure to provide a dual interface that supports both **IAccessible** and [**IDispatch**](idispatch-interface.md) so that clients written in Microsoft Visual Basic and various scripting languages can get information about the objects.</span></span>
2.  <span data-ttu-id="86137-108">呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 以通知用戶端變更您的自訂使用者介面元素。</span><span class="sxs-lookup"><span data-stu-id="86137-108">Call [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) to notify clients of changes to your custom user interface elements.</span></span>
3.  <span data-ttu-id="86137-109">處理 [**WM \_ GETOBJECT**](wm-getobject.md) 以提供存取權給您的可存取物件。</span><span class="sxs-lookup"><span data-stu-id="86137-109">Handle [**WM\_GETOBJECT**](wm-getobject.md) to provide access to your accessible objects.</span></span>

<span data-ttu-id="86137-110">如需設計可存取物件的建議和指導方針，請參閱 [Active Accessibility 伺服器的開發人員指南](developer-s-guide-for-active-accessibility-servers.md)。</span><span class="sxs-lookup"><span data-stu-id="86137-110">For suggestions and guidelines for designing accessible objects, see [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="86137-111">本節內容</span><span class="sxs-lookup"><span data-stu-id="86137-111">In this section</span></span>

-   [<span data-ttu-id="86137-112">伺服器如何執行子系識別碼</span><span class="sxs-lookup"><span data-stu-id="86137-112">How Servers Implement Child IDs</span></span>](how-servers-implement-child-ids.md)

 

 




