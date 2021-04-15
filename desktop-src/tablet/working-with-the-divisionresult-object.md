---
description: DivisionResult 物件代表分割物件所包含之筆觸的版面配置分析快照。 它包含來自版面配置分析的筆劃分類和群組資訊。
ms.assetid: 2bcf5223-7bf4-420c-8f04-a972f04f262d
title: 使用 DivisionResult 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0b9874f4a9d2e6bc4390d98803c2344308fc3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511920"
---
# <a name="working-with-the-divisionresult-object"></a><span data-ttu-id="09eeb-104">使用 DivisionResult 物件</span><span class="sxs-lookup"><span data-stu-id="09eeb-104">Working with the DivisionResult Object</span></span>

<span data-ttu-id="09eeb-105">**DivisionResult** 物件代表 **分割** 物件所包含之筆觸的版面配置分析快照。</span><span class="sxs-lookup"><span data-stu-id="09eeb-105">The **DivisionResult** object represents a snapshot of the layout analysis of the strokes contained by the **Divider** object.</span></span> <span data-ttu-id="09eeb-106">它包含來自版面配置分析的筆劃分類和群組資訊。</span><span class="sxs-lookup"><span data-stu-id="09eeb-106">It contains the stroke classification and grouping information from the layout analysis.</span></span>

<span data-ttu-id="09eeb-107">您可以透過結構化元素類型（例如繪圖或手寫線）從 **DivisionResult** 物件取得資訊。</span><span class="sxs-lookup"><span data-stu-id="09eeb-107">You can get information from the **DivisionResult** object by structural element type, such as drawing or lines of handwriting.</span></span> <span data-ttu-id="09eeb-108">**DivisionResult** 物件可以在 **分割** 物件終結之後保存。</span><span class="sxs-lookup"><span data-stu-id="09eeb-108">The **DivisionResult** object can persist after the **Divider** object is destroyed.</span></span> <span data-ttu-id="09eeb-109">在自動化中，此物件稱為 [**IInkDivisionResult 介面**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) 物件。</span><span class="sxs-lookup"><span data-stu-id="09eeb-109">In Automation, this object is called the [**IInkDivisionResult Interface**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

<span data-ttu-id="09eeb-110">**DivisionResult** 物件的 [[**筆觸**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)] 屬性包含在建立 **DivisionResult** 物件時，**分割** 物件中的 **筆劃** 集合副本。</span><span class="sxs-lookup"><span data-stu-id="09eeb-110">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property of the **DivisionResult** object contains a copy of the **Strokes** collection in the **Divider** object at the time the **DivisionResult** object was created.</span></span>

<span data-ttu-id="09eeb-111">[**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype)列舉會定義版面配置分析可辨識的結構化元素類型。</span><span class="sxs-lookup"><span data-stu-id="09eeb-111">The [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) enumeration defines the structural element types that the layout analysis recognizes.</span></span>

<span data-ttu-id="09eeb-112">**DivisionResult** 物件的 [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype)方法會傳回 **DivisionUnits** 集合，其中包含指定型別的所有結構化元素。</span><span class="sxs-lookup"><span data-stu-id="09eeb-112">The [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) method of the **DivisionResult** object returns a **DivisionUnits** collection that contains all structural elements of a given type.</span></span> <span data-ttu-id="09eeb-113">個別的結構元素是由 **DivisionUnit** 物件表示。</span><span class="sxs-lookup"><span data-stu-id="09eeb-113">An individual structural element is represented by a **DivisionUnit** object.</span></span> <span data-ttu-id="09eeb-114">每次呼叫 **ResultByType** 方法時， **DivisionResult** 物件都會建立 **DivisionUnits** 集合。</span><span class="sxs-lookup"><span data-stu-id="09eeb-114">Each time you call the **ResultByType** method, the **DivisionResult** object creates a **DivisionUnits** collection.</span></span> <span data-ttu-id="09eeb-115">如需 **DivisionUnit** 物件的詳細資訊，請參閱 [使用 DivisionUnit 物件](working-with-the-divisionunit-object.md)。</span><span class="sxs-lookup"><span data-stu-id="09eeb-115">For more information about the **DivisionUnit** object, see [Working with the DivisionUnit Object](working-with-the-divisionunit-object.md).</span></span>

 

 
