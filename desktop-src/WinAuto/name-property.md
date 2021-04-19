---
title: Name 屬性
description: Name 屬性是用戶端用來為使用者識別、尋找或宣告物件的字串。 所有物件都支援 Name 屬性。
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e93d8b90190f81179d681600f4b1bfacf4665e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106996556"
---
# <a name="name-property"></a><span data-ttu-id="124df-104">Name 屬性</span><span class="sxs-lookup"><span data-stu-id="124df-104">Name Property</span></span>

<span data-ttu-id="124df-105">**Name** 屬性是用戶端用來為使用者識別、尋找或宣告物件的字串。</span><span class="sxs-lookup"><span data-stu-id="124df-105">The **Name** property is a string used by clients to identify, find, or announce an object for the user.</span></span> <span data-ttu-id="124df-106">所有物件都支援 **Name** 屬性。</span><span class="sxs-lookup"><span data-stu-id="124df-106">All objects support the **Name** property.</span></span>

<span data-ttu-id="124df-107">例如，按鈕控制項上的文字是其名稱，而清單方塊或編輯控制項的名稱則是在控制項的定位順序中緊接在控制項前面的靜態文字。</span><span class="sxs-lookup"><span data-stu-id="124df-107">For example, the text on a button control is its name, while the name for a list box or edit control is the static text that immediately precedes the control in the tabbing order.</span></span> <span data-ttu-id="124df-108">即使是未顯示名稱的繪圖物件，在查詢 **name** 屬性時也會提供文字。</span><span class="sxs-lookup"><span data-stu-id="124df-108">Even graphic objects that do not display a name provide text when queried for the **Name** property.</span></span>

<span data-ttu-id="124df-109">藉由呼叫 [**IAccessible：： get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)，即可取出 **Name** 屬性。</span><span class="sxs-lookup"><span data-stu-id="124df-109">The **Name** property is retrieved by calling [**IAccessible::get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).</span></span>

## <a name="selecting-names"></a><span data-ttu-id="124df-110">選取名稱</span><span class="sxs-lookup"><span data-stu-id="124df-110">Selecting Names</span></span>

<span data-ttu-id="124df-111">物件的名稱應該是直覺的，讓使用者瞭解物件的意義或用途。</span><span class="sxs-lookup"><span data-stu-id="124df-111">An object's name should be intuitive so that users understand the object's meaning or purpose.</span></span> <span data-ttu-id="124df-112">此外，[ **名稱** ] 屬性應該是唯一的，相對於父系中的任何同級物件。</span><span class="sxs-lookup"><span data-stu-id="124df-112">Also, the **Name** property should be unique relative to any sibling objects in the parent.</span></span>

<span data-ttu-id="124df-113">資料表內的導覽會對某些使用者造成特別困難的問題。</span><span class="sxs-lookup"><span data-stu-id="124df-113">Navigation within tables presents especially difficult problems for some users.</span></span> <span data-ttu-id="124df-114">因此，伺服器開發人員應該盡可能使資料表單元格名稱成為描述性。</span><span class="sxs-lookup"><span data-stu-id="124df-114">Therefore, server developers should make table cell names as descriptive as possible.</span></span> <span data-ttu-id="124df-115">例如，您可以藉由結合所佔用的資料列和資料行的名稱（例如 "A1"）來建立資料格名稱。</span><span class="sxs-lookup"><span data-stu-id="124df-115">For example, you could create a cell name by combining the names of the row and column it occupies, such as "A1."</span></span> <span data-ttu-id="124df-116">不過，通常最好使用更具描述性的名稱，例如 "南，二月"，其中 "南" 是目前的資料列，而 "二月" 是目前的資料行。</span><span class="sxs-lookup"><span data-stu-id="124df-116">However, it is generally better to use more descriptive names, such as "Nancy, February" where "Nancy" is the current row and "February" is the current column.</span></span>

## <a name="delegating-requests"></a><span data-ttu-id="124df-117">委派要求</span><span class="sxs-lookup"><span data-stu-id="124df-117">Delegating Requests</span></span>

<span data-ttu-id="124df-118">如果物件沒有其 **Name** 屬性的存取權，它就會將要求委派給其父系，並依其子識別碼進行識別。</span><span class="sxs-lookup"><span data-stu-id="124df-118">If an object does not have access to its **Name** property, it delegates requests to its parent, identifying itself by its child ID.</span></span> <span data-ttu-id="124df-119">例如，如果用戶端呼叫編輯控制項的 [ **名稱** ] 屬性，則編輯控制項會將查詢委派給其父系，以傳回標記編輯控制項的靜態文字控制項值。</span><span class="sxs-lookup"><span data-stu-id="124df-119">For example, if a client calls an edit control's **Name** property, the edit control delegates the query to its parent, which returns the value of the static text control that labels the edit control.</span></span>

 

 




