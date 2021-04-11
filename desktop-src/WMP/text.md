---
title: " (Windows Media Player SDK) 的文字"
description: Text
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Windows Media Player 行動外觀、文字
- 外觀，文字
- 外觀的參考、文字
- 外觀中的文字，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801d93698bc7a17eea34df71514dd88b485f0d9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103843012"
---
# <a name="text-windows-media-player-sdk"></a><span data-ttu-id="26da1-107"> (Windows Media Player SDK) 的文字</span><span class="sxs-lookup"><span data-stu-id="26da1-107">Text (Windows Media Player SDK)</span></span>

<span data-ttu-id="26da1-108">您可能會想要在面板中使用一或多個文字顯示方塊。</span><span class="sxs-lookup"><span data-stu-id="26da1-108">You may want to use one or more text display boxes in your skin.</span></span> <span data-ttu-id="26da1-109">您使用的每個文字顯示方塊都必須定義在外觀定義檔中。</span><span class="sxs-lookup"><span data-stu-id="26da1-109">Each text display box you use must be defined in the skin definition file.</span></span> <span data-ttu-id="26da1-110">如果您未在此區段中定義文字顯示框，您的面板將無法使用它。</span><span class="sxs-lookup"><span data-stu-id="26da1-110">If you do not define a text display box in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="26da1-111">面板定義檔的文字區段開頭為以下這一行：</span><span class="sxs-lookup"><span data-stu-id="26da1-111">The Text section of the skin definition file begins with this line:</span></span>


```C++
[ Text ]

```



<span data-ttu-id="26da1-112">然後，您必須新增一或多行，其中包含面板中每個文字顯示方塊的相關資訊</span><span class="sxs-lookup"><span data-stu-id="26da1-112">You then must add one or more lines that contain information about each of the text display boxes in your skin</span></span>


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



<span data-ttu-id="26da1-113">您可以使用下列範本作為面板定義檔的文字區段：</span><span class="sxs-lookup"><span data-stu-id="26da1-113">You can use the following template for the Text section of your skin definition file:</span></span>


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



<span data-ttu-id="26da1-114">您必須使用上述範本中所示的順序，來顯示文字區段中每一行的文字顯示框資訊。</span><span class="sxs-lookup"><span data-stu-id="26da1-114">You must use the order shown in the preceding template for text display box information for each line in the Text section.</span></span> <span data-ttu-id="26da1-115">這一行的每個部分都是必要的。</span><span class="sxs-lookup"><span data-stu-id="26da1-115">Each part of the line is required.</span></span> <span data-ttu-id="26da1-116">下列各節將詳細說明每個專案。</span><span class="sxs-lookup"><span data-stu-id="26da1-116">The following sections describe each item in detail.</span></span>

1.  [<span data-ttu-id="26da1-117">文字類型</span><span class="sxs-lookup"><span data-stu-id="26da1-117">Text Type</span></span>](text-type.md)
2.  [<span data-ttu-id="26da1-118">文字位置</span><span class="sxs-lookup"><span data-stu-id="26da1-118">Text Location</span></span>](text-location.md)
3.  [<span data-ttu-id="26da1-119">文字對齊</span><span class="sxs-lookup"><span data-stu-id="26da1-119">Text Alignment</span></span>](text-alignment.md)
4.  [<span data-ttu-id="26da1-120">文字字型</span><span class="sxs-lookup"><span data-stu-id="26da1-120">Text Font</span></span>](text-font.md)
5.  [<span data-ttu-id="26da1-121">文字色彩</span><span class="sxs-lookup"><span data-stu-id="26da1-121">Text Color</span></span>](text-color.md)

<span data-ttu-id="26da1-122">如需文字程式碼的範例，請參閱 [範例文字一節](sample-text-section.md)。</span><span class="sxs-lookup"><span data-stu-id="26da1-122">For an example of Text code, see [Sample Text Section](sample-text-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="26da1-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="26da1-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26da1-124">**外觀參考**</span><span class="sxs-lookup"><span data-stu-id="26da1-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




