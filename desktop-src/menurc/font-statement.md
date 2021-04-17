---
title: 字型語句
description: 定義系統在對話方塊中用來繪製文字的字型。 字型必須先前已載入;例如，藉由呼叫 LoadResource 函數。
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- 字型語句功能表和其他資源
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b31b280a5a973301e8410f1f74340138af07ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463112"
---
# <a name="font-statement"></a><span data-ttu-id="b6647-105">字型語句</span><span class="sxs-lookup"><span data-stu-id="b6647-105">FONT statement</span></span>

<span data-ttu-id="b6647-106">定義系統在對話方塊中用來繪製文字的字型。</span><span class="sxs-lookup"><span data-stu-id="b6647-106">Defines the font with which the system will draw text in the dialog box.</span></span> <span data-ttu-id="b6647-107">字型必須先前已載入;例如，藉由呼叫 [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) 函數。</span><span class="sxs-lookup"><span data-stu-id="b6647-107">The font must have been previously loaded; for example, by calling the [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) function.</span></span>

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span data-ttu-id="b6647-108"><span id="pointsize"></span><span id="POINTSIZE"></span>*dialog*</span><span class="sxs-lookup"><span data-stu-id="b6647-108"><span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*</span></span>
</dt> <dd>

<span data-ttu-id="b6647-109">字型的大小（以點為單位）。</span><span class="sxs-lookup"><span data-stu-id="b6647-109">The size of the font, in points.</span></span>

</dd> <dt>

<span data-ttu-id="b6647-110"><span id="typeface"></span><span id="TYPEFACE"></span>*字體*</span><span class="sxs-lookup"><span data-stu-id="b6647-110"><span id="typeface"></span><span id="TYPEFACE"></span>*typeface*</span></span>
</dt> <dd>

<span data-ttu-id="b6647-111">字樣的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6647-111">The name of the typeface.</span></span> <span data-ttu-id="b6647-112">此參數必須以引號括住 ( ") 。</span><span class="sxs-lookup"><span data-stu-id="b6647-112">This parameter must be enclosed in quotes (").</span></span>

</dd> <dt>

<span data-ttu-id="b6647-113"><span id="weight"></span><span id="WEIGHT"></span>*重量*</span><span class="sxs-lookup"><span data-stu-id="b6647-113"><span id="weight"></span><span id="WEIGHT"></span>*weight*</span></span>
</dt> <dd>

<span data-ttu-id="b6647-114">範圍0到1000的字型粗細。</span><span class="sxs-lookup"><span data-stu-id="b6647-114">The weight of the font in the range 0 through 1000.</span></span> <span data-ttu-id="b6647-115">例如，400是正常的，700是粗體。</span><span class="sxs-lookup"><span data-stu-id="b6647-115">For example, 400 is normal and 700 is bold.</span></span> <span data-ttu-id="b6647-116">如果這個值為0，則會使用預設權數。</span><span class="sxs-lookup"><span data-stu-id="b6647-116">If this value is 0, the default weight is used.</span></span> <span data-ttu-id="b6647-117">如需預先定義的值清單，請參閱 WinGDI 中定義的 **FW \_ \*** 值。</span><span class="sxs-lookup"><span data-stu-id="b6647-117">For a list of predefined values, see the **FW\_\*** values defined in WinGDI.h.</span></span>

</dd> <dt>

<span data-ttu-id="b6647-118"><span id="italic"></span><span id="ITALIC"></span>*斜*</span><span class="sxs-lookup"><span data-stu-id="b6647-118"><span id="italic"></span><span id="ITALIC"></span>*italic*</span></span>
</dt> <dd>

<span data-ttu-id="b6647-119">如果設定為 TRUE，則表示斜體字型。</span><span class="sxs-lookup"><span data-stu-id="b6647-119">Indicates an italic font if set to TRUE.</span></span>

</dd> <dt>

<span data-ttu-id="b6647-120"><span id="charset"></span><span id="CHARSET"></span>*字元集*</span><span class="sxs-lookup"><span data-stu-id="b6647-120"><span id="charset"></span><span id="CHARSET"></span>*charset*</span></span>
</dt> <dd>

<span data-ttu-id="b6647-121">字元集。</span><span class="sxs-lookup"><span data-stu-id="b6647-121">The character set.</span></span> <span data-ttu-id="b6647-122">如需值的清單，請參閱 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的 **lfCharSet** 成員。</span><span class="sxs-lookup"><span data-stu-id="b6647-122">For a list of values, see the **lfCharSet** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b6647-123">範例</span><span class="sxs-lookup"><span data-stu-id="b6647-123">Examples</span></span>

<span data-ttu-id="b6647-124">下列範例示範 **字型** 語句的用法：</span><span class="sxs-lookup"><span data-stu-id="b6647-124">The following example demonstrates the use of the **FONT** statement:</span></span>

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a><span data-ttu-id="b6647-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6647-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6647-126">**LoadResource**</span><span class="sxs-lookup"><span data-stu-id="b6647-126">**LoadResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 