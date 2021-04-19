---
title: CurrentPosition
description: CurrentPosition 屬性會指定或抓取媒體專案中的目前位置（以秒為單位）。
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- CurrentPosition Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPosition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c690c102bb95c1a58785f18d727ffdae2a82c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993225"
---
# <a name="controlscurrentposition"></a><span data-ttu-id="ad0ab-104">CurrentPosition</span><span class="sxs-lookup"><span data-stu-id="ad0ab-104">Controls.currentPosition</span></span>

<span data-ttu-id="ad0ab-105">**CurrentPosition** 屬性會指定或抓取媒體專案中的目前位置（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ad0ab-105">The **currentPosition** property specifies or retrieves the current position in the media item in seconds from the beginning.</span></span>

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a><span data-ttu-id="ad0ab-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="ad0ab-106">Possible Values</span></span>

<span data-ttu-id="ad0ab-107">這個屬性是 (**雙**) 的讀/寫 **號碼**。</span><span class="sxs-lookup"><span data-stu-id="ad0ab-107">This property is a read/write **Number** (**double**).</span></span>

## <a name="examples"></a><span data-ttu-id="ad0ab-108">範例</span><span class="sxs-lookup"><span data-stu-id="ad0ab-108">Examples</span></span>

<span data-ttu-id="ad0ab-109">下列範例會使用 **currentPosition** 來搜尋使用者提供的位置。</span><span class="sxs-lookup"><span data-stu-id="ad0ab-109">The following example uses **currentPosition** to seek to a position provided by the user.</span></span> <span data-ttu-id="ad0ab-110">系統會建立 HTML 按鈕元素來執行 JScript 程式碼。</span><span class="sxs-lookup"><span data-stu-id="ad0ab-110">An HTML BUTTON element is created to execute the JScript code.</span></span> <span data-ttu-id="ad0ab-111">系統會建立名為 setPosition 的 HTML 文字輸入元素，以從使用者接受值（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ad0ab-111">An HTML TEXT input element, named setPosition, was created to accept a value, in seconds, from the user.</span></span> <span data-ttu-id="ad0ab-112">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="ad0ab-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "Set"  NAME = "Set"  VALUE = "Set Position"

    /* Check to be sure the TEXT element contains a valid value. */
    if (!isNaN(setPosition.value) && (setPosition.value != '))

    /* Set the current position when the user clicks the button. */
    onClick = "Player.controls.currentPosition = setPosition.value;
">
```



## <a name="requirements"></a><span data-ttu-id="ad0ab-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad0ab-113">Requirements</span></span>



| <span data-ttu-id="ad0ab-114">需求</span><span class="sxs-lookup"><span data-stu-id="ad0ab-114">Requirement</span></span> | <span data-ttu-id="ad0ab-115">值</span><span class="sxs-lookup"><span data-stu-id="ad0ab-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad0ab-116">版本</span><span class="sxs-lookup"><span data-stu-id="ad0ab-116">Version</span></span><br/> | <span data-ttu-id="ad0ab-117">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="ad0ab-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ad0ab-118">DLL</span><span class="sxs-lookup"><span data-stu-id="ad0ab-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="ad0ab-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad0ab-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad0ab-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad0ab-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad0ab-121">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="ad0ab-121">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





