---
title: 圖示控制項
description: 定義圖示控制項。 此控制項是顯示在對話方塊中的圖示。
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- 圖示控制項功能表和其他資源
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2400136395a17f039d552373fa35cba0f3545a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462545"
---
# <a name="icon-control"></a><span data-ttu-id="88f77-105">圖示控制項</span><span class="sxs-lookup"><span data-stu-id="88f77-105">ICON control</span></span>

<span data-ttu-id="88f77-106">定義圖示控制項。</span><span class="sxs-lookup"><span data-stu-id="88f77-106">Defines an icon control.</span></span> <span data-ttu-id="88f77-107">此控制項是顯示在對話方塊中的圖示。</span><span class="sxs-lookup"><span data-stu-id="88f77-107">This control is an icon displayed in a dialog box.</span></span>

<span data-ttu-id="88f77-108">**Icon** 控制項語句（您只能在 [**DIALOGEX**](dialogex-resource.md)語句中使用）會定義控制項的圖示資源識別碼、圖示控制項識別碼、位置和屬性。</span><span class="sxs-lookup"><span data-stu-id="88f77-108">The **ICON** control statement, which you can use only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the icon-resource identifier, icon-control identifier, position, and attributes of a control.</span></span>

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="88f77-109"><span id="text"></span><span id="TEXT"></span>*文本*</span><span class="sxs-lookup"><span data-stu-id="88f77-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="88f77-110">圖示的名稱 (不是) 在資源檔中的其他位置定義的檔案名。</span><span class="sxs-lookup"><span data-stu-id="88f77-110">Name of an icon (not a file name) defined elsewhere in the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="88f77-111"><span id="width"></span><span id="WIDTH"></span>*寬度*</span><span class="sxs-lookup"><span data-stu-id="88f77-111"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="88f77-112">此值會被忽略，且應設定為零。</span><span class="sxs-lookup"><span data-stu-id="88f77-112">This value is ignored and should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="88f77-113"><span id="height"></span><span id="HEIGHT"></span>*高度*</span><span class="sxs-lookup"><span data-stu-id="88f77-113"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="88f77-114">此值會被忽略，且應設定為零。</span><span class="sxs-lookup"><span data-stu-id="88f77-114">This value is ignored and should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="88f77-115"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="88f77-115"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="88f77-116">控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="88f77-116">Control style.</span></span> <span data-ttu-id="88f77-117">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="88f77-117">This parameter is optional.</span></span> <span data-ttu-id="88f77-118">唯一可指定的值為 **SS \_ 圖示** 樣式。</span><span class="sxs-lookup"><span data-stu-id="88f77-118">The only value that can be specified is the **SS\_ICON** style.</span></span> <span data-ttu-id="88f77-119">這是指定是否指定這個參數的預設樣式。</span><span class="sxs-lookup"><span data-stu-id="88f77-119">This is the default style whether this parameter is specified or not.</span></span>

</dd> </dl>

<span data-ttu-id="88f77-120">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="88f77-120">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="88f77-121">範例</span><span class="sxs-lookup"><span data-stu-id="88f77-121">Examples</span></span>

<span data-ttu-id="88f77-122">這個範例會定義圖示控制項，其圖示識別碼為901，而其名稱為 myicon：</span><span class="sxs-lookup"><span data-stu-id="88f77-122">This example defines an icon control whose icon identifier is 901 and whose name is myicon:</span></span>

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a><span data-ttu-id="88f77-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88f77-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88f77-124">**圖示**</span><span class="sxs-lookup"><span data-stu-id="88f77-124">**ICON**</span></span>](icon-resource.md)
</dt> </dl>

 

 




