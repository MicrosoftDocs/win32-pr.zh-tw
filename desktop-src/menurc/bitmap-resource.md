---
title: 點陣圖資源
description: 定義應用程式在其螢幕顯示中使用的點陣圖，或為功能表或控制項中的專案。
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- 點陣圖資源功能表與其他資源
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5bed33fb66d9deb85e1f25165f3f7a0f664961
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375104"
---
# <a name="bitmap-resource"></a><span data-ttu-id="0f52c-104">點陣圖資源</span><span class="sxs-lookup"><span data-stu-id="0f52c-104">BITMAP resource</span></span>

<span data-ttu-id="0f52c-105">定義應用程式在其螢幕顯示中使用的點陣圖，或為功能表或控制項中的專案。</span><span class="sxs-lookup"><span data-stu-id="0f52c-105">Defines a bitmap that an application uses in its screen display or as an item in a menu or control.</span></span>

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a><span data-ttu-id="0f52c-106">參數</span><span class="sxs-lookup"><span data-stu-id="0f52c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f52c-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="0f52c-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="0f52c-108">識別資源的唯一名稱或16位不帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="0f52c-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="0f52c-109"><span id="filename"></span><span id="FILENAME"></span>*檔案名*</span><span class="sxs-lookup"><span data-stu-id="0f52c-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="0f52c-110">包含資源的檔案名。</span><span class="sxs-lookup"><span data-stu-id="0f52c-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="0f52c-111">名稱必須是有效的檔案名;如果檔案不在目前的工作目錄中，它必須是完整路徑。</span><span class="sxs-lookup"><span data-stu-id="0f52c-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="0f52c-112">路徑應該是加上引號的字串。</span><span class="sxs-lookup"><span data-stu-id="0f52c-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="0f52c-113">此外，也支援某些屬性以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="0f52c-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="0f52c-114">如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="0f52c-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0f52c-115">範例</span><span class="sxs-lookup"><span data-stu-id="0f52c-115">Examples</span></span>

<span data-ttu-id="0f52c-116">下列範例會定義兩個位圖資源：</span><span class="sxs-lookup"><span data-stu-id="0f52c-116">The following example defines two bitmap resources:</span></span>

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a><span data-ttu-id="0f52c-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f52c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f52c-118">使用點陣圖</span><span class="sxs-lookup"><span data-stu-id="0f52c-118">Using Bitmaps</span></span>](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[<span data-ttu-id="0f52c-119">**LoadBitmap**</span><span class="sxs-lookup"><span data-stu-id="0f52c-119">**LoadBitmap**</span></span>](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[<span data-ttu-id="0f52c-120">**LoadImage**</span><span class="sxs-lookup"><span data-stu-id="0f52c-120">**LoadImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 