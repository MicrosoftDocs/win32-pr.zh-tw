---
title: 圖示資源
description: 定義點陣圖，以定義要用於指定應用程式或動畫圖標的圖示形狀。
ms.assetid: a8e3205e-e17a-4daf-a599-4dc89cb1e640
keywords:
- 圖示資源功能表與其他資源
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f762c4f4b459d51a0243a9cdbd7367deda7b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507879"
---
# <a name="icon-resource"></a><span data-ttu-id="28771-104">圖示資源</span><span class="sxs-lookup"><span data-stu-id="28771-104">ICON resource</span></span>

<span data-ttu-id="28771-105">定義點陣圖，以定義要用於指定應用程式或動畫圖標的圖示形狀。</span><span class="sxs-lookup"><span data-stu-id="28771-105">Defines a bitmap that defines the shape of the icon to be used for a given application or an animated icon.</span></span>

``` syntax
nameID ICON filename
```

## <a name="parameters"></a><span data-ttu-id="28771-106">參數</span><span class="sxs-lookup"><span data-stu-id="28771-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28771-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="28771-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="28771-108">識別資源的唯一名稱或16位不帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="28771-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="28771-109"><span id="filename"></span><span id="FILENAME"></span>*檔案名*</span><span class="sxs-lookup"><span data-stu-id="28771-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="28771-110">包含資源的檔案名。</span><span class="sxs-lookup"><span data-stu-id="28771-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="28771-111">名稱必須是有效的檔案名;如果檔案不在目前的工作目錄中，它必須是完整路徑。</span><span class="sxs-lookup"><span data-stu-id="28771-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="28771-112">路徑應該是加上引號的字串。</span><span class="sxs-lookup"><span data-stu-id="28771-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="28771-113">此外，也支援某些屬性以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="28771-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="28771-114">如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="28771-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="28771-115">備註</span><span class="sxs-lookup"><span data-stu-id="28771-115">Remarks</span></span>

<span data-ttu-id="28771-116">圖示和游標資源可以包含一個以上的影像。</span><span class="sxs-lookup"><span data-stu-id="28771-116">Icon and cursor resources can contain more than one image.</span></span>

## <a name="examples"></a><span data-ttu-id="28771-117">範例</span><span class="sxs-lookup"><span data-stu-id="28771-117">Examples</span></span>

<span data-ttu-id="28771-118">下列範例會定義兩個圖示資源：</span><span class="sxs-lookup"><span data-stu-id="28771-118">The following example defines two icon resources:</span></span>

``` syntax
desk1   ICON "desk.ico"
11      ICON "custom.ico"
```

## <a name="see-also"></a><span data-ttu-id="28771-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28771-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28771-120">使用圖示</span><span class="sxs-lookup"><span data-stu-id="28771-120">Using Icons</span></span>](./using-icons.md)
</dt> </dl>

 

 