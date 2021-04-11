---
title: 外觀定義檔案 XML 結構
description: 外觀定義檔案 XML 結構
ms.assetid: 93325b94-667a-42a6-92f8-78288d36da81
keywords:
- 建立外觀、面板定義檔
- 面板定義檔 Windows Media Player 的外觀
- 外觀、面板定義檔
- 面板的檔案、外觀定義
- 外觀定義檔案，XML 結構
- 外觀定義檔案的 XML 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8508f1a458930bc2b60d564a45ef08a9f9f5a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021714"
---
# <a name="skin-definition-file-xml-structure"></a><span data-ttu-id="070e9-109">外觀定義檔案 XML 結構</span><span class="sxs-lookup"><span data-stu-id="070e9-109">Skin Definition File XML Structure</span></span>

<span data-ttu-id="070e9-110">面板定義檔是以 XML 撰寫的。</span><span class="sxs-lookup"><span data-stu-id="070e9-110">The skin definition file is written in XML.</span></span> <span data-ttu-id="070e9-111">XML 的其中一個重要功能是完整結構化，而且類似于大綱。</span><span class="sxs-lookup"><span data-stu-id="070e9-111">One of the important features of XML is that it is completely structured, and is similar to an outline.</span></span> <span data-ttu-id="070e9-112">XML 程式碼只是一系列的元素，例如 **VIEW** 和 **BUTTONGROUP**。</span><span class="sxs-lookup"><span data-stu-id="070e9-112">The XML code is simply a series of elements such as **VIEW** and **BUTTONGROUP**.</span></span> <span data-ttu-id="070e9-113">您將從元素開始，然後使用屬性來定義它們。</span><span class="sxs-lookup"><span data-stu-id="070e9-113">You will start with the elements and then define them with attributes.</span></span> <span data-ttu-id="070e9-114">本教學課程的其餘部分將提供屬性的詳細資料，但以下是將使用的元素大綱：</span><span class="sxs-lookup"><span data-stu-id="070e9-114">The rest of this tutorial will give you details on the attributes, but here is the outline of the elements that will be used:</span></span>


```C++
<THEME>
    <VIEW>
        <BUTTONGROUP>
            <BUTTONELEMENT/>
            <BUTTONELEMENT/>
        </BUTTONGROUP>
    </VIEW>
<THEME>

```



<span data-ttu-id="070e9-115">請記住專案的簡單結構，讓每個專案都能成為唯一的屬性。</span><span class="sxs-lookup"><span data-stu-id="070e9-115">By keeping in mind the simple structure of the elements, you can make sense of the attributes that make each element unique.</span></span> <span data-ttu-id="070e9-116">本節的其餘主題將涵蓋每個元素的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="070e9-116">Details of each element will be covered in the remaining topics of this section.</span></span> <span data-ttu-id="070e9-117">如需有關元素和屬性的詳細資訊，請參閱面板程式 [設計參考](skin-programming-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="070e9-117">For more information about elements and attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="070e9-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="070e9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="070e9-119">**建立外觀定義檔**</span><span class="sxs-lookup"><span data-stu-id="070e9-119">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




