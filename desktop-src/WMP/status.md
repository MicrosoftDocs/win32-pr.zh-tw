---
title: '狀態 (Windows Media Player SDK) '
description: 狀態
ms.assetid: b8d6d026-819c-4889-a894-c82fe81ec922
keywords:
- Windows Media Player 行動外觀、狀態顯示
- 外觀，狀態顯示
- 外觀的參考、狀態顯示
- 狀態顯示在 [外觀]、[關於]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f1cd9e0df209d6a37ed880765fd607e939765
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024417"
---
# <a name="status-windows-media-player-sdk"></a><span data-ttu-id="ed225-107">狀態 (Windows Media Player SDK) </span><span class="sxs-lookup"><span data-stu-id="ed225-107">Status (Windows Media Player SDK)</span></span>

<span data-ttu-id="ed225-108">您可能會想要在您的面板中使用狀態顯示。</span><span class="sxs-lookup"><span data-stu-id="ed225-108">You may want to use a status display in your skin.</span></span> <span data-ttu-id="ed225-109">如果是，則狀態專案必須定義在面板定義檔中。</span><span class="sxs-lookup"><span data-stu-id="ed225-109">If so, the status element must be defined in the skin definition file.</span></span> <span data-ttu-id="ed225-110">或者，您也可以使用 Text 元素中的 Status 屬性來顯示這項資訊。</span><span class="sxs-lookup"><span data-stu-id="ed225-110">As an alternative, you may also display this information by using the Status attribute in the Text element.</span></span>

<span data-ttu-id="ed225-111">面板定義檔的 [狀態] 區段開頭為以下這一行：</span><span class="sxs-lookup"><span data-stu-id="ed225-111">The Status section of the skin definition file begins with this line:</span></span>


```C++
[ Status ]

```



<span data-ttu-id="ed225-112">然後，您必須新增一或多行，其中包含有關面板中狀態顯示的資訊。</span><span class="sxs-lookup"><span data-stu-id="ed225-112">You then must add one or more lines that contain information about the status display in your skin.</span></span>


```C++
    On           45,193,120,13    Left    Tahoma,8,B        0,255,  0

```



<span data-ttu-id="ed225-113">您可以使用下列範本作為面板定義檔的 [狀態] 區段：</span><span class="sxs-lookup"><span data-stu-id="ed225-113">You can use the following template for the Status section of your skin definition file:</span></span>


```C++
//  <Item>       <Location>     <Align>  <Font>          <Color>
//  ------       ----------     -------  ------          -------

```



<span data-ttu-id="ed225-114">您必須使用上述範本中顯示的順序，以取得 [狀態] 區段中每一行的狀態顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="ed225-114">You must use the order shown in the preceding template for status display information for each line in the Status section.</span></span> <span data-ttu-id="ed225-115">這一行的每個部分都是必要的。</span><span class="sxs-lookup"><span data-stu-id="ed225-115">Each part of the line is required.</span></span> <span data-ttu-id="ed225-116">下列各節將說明每個專案：</span><span class="sxs-lookup"><span data-stu-id="ed225-116">The following sections describe each item:</span></span>

-   [<span data-ttu-id="ed225-117">狀態項目</span><span class="sxs-lookup"><span data-stu-id="ed225-117">Status Item</span></span>](status-item.md)
-   [<span data-ttu-id="ed225-118">狀態位置</span><span class="sxs-lookup"><span data-stu-id="ed225-118">Status Location</span></span>](status-location.md)
-   [<span data-ttu-id="ed225-119">狀態對齊</span><span class="sxs-lookup"><span data-stu-id="ed225-119">Status Alignment</span></span>](status-alignment.md)
-   [<span data-ttu-id="ed225-120">狀態字型</span><span class="sxs-lookup"><span data-stu-id="ed225-120">Status Font</span></span>](status-font.md)
-   [<span data-ttu-id="ed225-121">狀態色彩</span><span class="sxs-lookup"><span data-stu-id="ed225-121">Status Color</span></span>](status-color.md)

<span data-ttu-id="ed225-122">如需狀態碼的範例，請參閱 [範例狀態一節](sample-status-section.md)。</span><span class="sxs-lookup"><span data-stu-id="ed225-122">For an example of Status code, see [Sample Status Section](sample-status-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed225-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed225-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed225-124">**外觀參考**</span><span class="sxs-lookup"><span data-stu-id="ed225-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




