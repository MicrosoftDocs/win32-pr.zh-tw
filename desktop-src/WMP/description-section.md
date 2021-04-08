---
title: 描述區段
description: 描述區段
ms.assetid: 280a9a4d-935f-440d-a606-94aeba0007db
keywords:
- Windows Media Player 行動外觀、描述區段
- 外觀，描述區段
- 建立外觀，描述區段
- 撰寫面板的程式碼，描述區段
- 外觀中的描述區段
- 外觀定義檔，描述區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9518b6b1de128457dc3e6b3738ddab9be2a873
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840680"
---
# <a name="description-section"></a><span data-ttu-id="3a0e7-109">描述區段</span><span class="sxs-lookup"><span data-stu-id="3a0e7-109">Description Section</span></span>

<span data-ttu-id="3a0e7-110">接下來，您必須在建立適用于 Windows Mobile 2003 和更新版本的 Windows Media Player 9 系列面板時，提供描述面板大小和方向的區段：</span><span class="sxs-lookup"><span data-stu-id="3a0e7-110">Next, you must provide a section that describes the size and orientation of the skin when creating a skin for Windows Media Player 9 Series for Windows Mobile 2003 and later versions:</span></span>


```C++
[ Description ]
//              <X,Y>       <DPI>
//              ------      -----
    Dimensions  240, 320    96

//    <Orientation>
//    -------------
    Orientation Portrait

```



<span data-ttu-id="3a0e7-111">[描述] 區段的開頭必須是以括弧括住的單字描述，然後再包含指定面板之尺寸和顯示解析度的行。</span><span class="sxs-lookup"><span data-stu-id="3a0e7-111">The Description section must begin with the word Description in brackets, and then include a line that specifies the dimensions and display resolution for the skin.</span></span>

<span data-ttu-id="3a0e7-112">開頭為兩個正斜線的行不會經過處理，而且可以用於批註或（如先前的程式碼所示），以協助您記住一節中的內容。</span><span class="sxs-lookup"><span data-stu-id="3a0e7-112">Lines beginning with two forward slashes are not processed, and can be used for comments or, as shown in the previous code, a template to help you remember what goes in a section.</span></span> <span data-ttu-id="3a0e7-113">您也可以使用範本來協助將所有專案對齊資料行。</span><span class="sxs-lookup"><span data-stu-id="3a0e7-113">You can also use templates to help align everything into columns.</span></span>

<span data-ttu-id="3a0e7-114">如需 [描述] 區段的詳細資訊，請參閱面板參考中的 [描述](description.md) 。</span><span class="sxs-lookup"><span data-stu-id="3a0e7-114">For more information about the Description section, see [Description](description.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a0e7-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a0e7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a0e7-116">**撰寫程式碼**</span><span class="sxs-lookup"><span data-stu-id="3a0e7-116">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




