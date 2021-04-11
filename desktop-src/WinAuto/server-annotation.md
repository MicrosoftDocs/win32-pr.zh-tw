---
title: 伺服器注釋
description: 本節提供使用伺服器批註的相關資訊。
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe1b8fba9849b25a29c50ea1f55507e61eb69f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021058"
---
# <a name="server-annotation"></a><span data-ttu-id="efab4-103">伺服器注釋</span><span class="sxs-lookup"><span data-stu-id="efab4-103">Server Annotation</span></span>

<span data-ttu-id="efab4-104">本節提供使用伺服器批註的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="efab4-104">This section provides information about using server annotation.</span></span>

## <a name="summary"></a><span data-ttu-id="efab4-105">總結</span><span class="sxs-lookup"><span data-stu-id="efab4-105">Summary</span></span>

<span data-ttu-id="efab4-106">您可以定義可執行 [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver)的類別、建立其實例，以及告訴系統您希望它覆寫特定 UI 元素上的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="efab4-106">You define a class that implements [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), create an instance of it, and tell the system that you want it to override specific properties on specific UI elements.</span></span> <span data-ttu-id="efab4-107">當用戶端向其中一個 UI 元素要求其中一個屬性時，系統會呼叫您的物件，並提供一個值給您。</span><span class="sxs-lookup"><span data-stu-id="efab4-107">When a client requests one of the properties from one of the UI elements, your object is called and given an opportunity to provide a value.</span></span> <span data-ttu-id="efab4-108">如果您的物件傳回值，則該值會傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="efab4-108">If your object returns a value, that value is passed back to the client.</span></span> <span data-ttu-id="efab4-109">如果您的物件不會傳回值，則會將該 UI 元素的預設值傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="efab4-109">If your object does not return a value, the default value for that UI element is returned to the client.</span></span>

## <a name="when-to-use-this-technique"></a><span data-ttu-id="efab4-110">使用這項技術的時機</span><span class="sxs-lookup"><span data-stu-id="efab4-110">When to Use This Technique</span></span>

<span data-ttu-id="efab4-111">當您想要覆寫物件的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性時，請使用這項技術。</span><span class="sxs-lookup"><span data-stu-id="efab4-111">Use this technique when you want to override the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties for an object.</span></span> <span data-ttu-id="efab4-112">這項技術比先前的 **IAccessible** 技巧簡單許多。</span><span class="sxs-lookup"><span data-stu-id="efab4-112">This technique is much simpler than previous **IAccessible** techniques.</span></span> <span data-ttu-id="efab4-113">如需詳細資訊，請參閱 [動態注釋的替代方案](alternatives-to-dynamic-annotation.md)。</span><span class="sxs-lookup"><span data-stu-id="efab4-113">For more information, see [Alternatives to Dynamic Annotation](alternatives-to-dynamic-annotation.md).</span></span>

<span data-ttu-id="efab4-114">您無法使用伺服器注釋來改變公開的物件結構。</span><span class="sxs-lookup"><span data-stu-id="efab4-114">You cannot use server annotation to alter the exposed object structure.</span></span> <span data-ttu-id="efab4-115">若要變更物件的結構，您必須執行完整的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="efab4-115">To change the structure of an object, you must implement a full [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>

<span data-ttu-id="efab4-116">如需有關伺服器批註的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="efab4-116">For more information on server annotation, see the following topics:</span></span>

-   [<span data-ttu-id="efab4-117">使用伺服器注釋</span><span class="sxs-lookup"><span data-stu-id="efab4-117">Using Server Annotation</span></span>](using-server-annotation.md)
-   [<span data-ttu-id="efab4-118">伺服器批註範例</span><span class="sxs-lookup"><span data-stu-id="efab4-118">Server Annotation Sample</span></span>](server-annotation-sample.md)

 

 




