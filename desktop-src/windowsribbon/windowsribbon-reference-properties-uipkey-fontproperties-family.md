---
title: UI_PKEY_FontProperties_Family
description: 識別 UI \_ PKEY \_ FontProperties \_ 系列屬性。
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7183e51105a397f14154639512ca11f7c03d44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969519"
---
# <a name="ui_pkey_fontproperties_family"></a><span data-ttu-id="8e0ca-103">UI \_ PKEY \_ FontProperties \_ 系列</span><span class="sxs-lookup"><span data-stu-id="8e0ca-103">UI\_PKEY\_FontProperties\_Family</span></span>

<span data-ttu-id="8e0ca-104">識別 UI \_ PKEY \_ FontProperties \_ 系列屬性。</span><span class="sxs-lookup"><span data-stu-id="8e0ca-104">Identifies the UI\_PKEY\_FontProperties\_Family property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Family
   shellPKey = UI_PKEY_FontProperties_Family
   formatID = 00000301-7363-696e-8441798acf5aebb7
   propID = 301
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="8e0ca-105">備註</span><span class="sxs-lookup"><span data-stu-id="8e0ca-105">Remarks</span></span>

<span data-ttu-id="8e0ca-106">\_ \_ \_ 應用程式會使用 UI PKEY FontProperties 系列來查詢 [**字型家族**] 下拉式清單庫的值。</span><span class="sxs-lookup"><span data-stu-id="8e0ca-106">UI\_PKEY\_FontProperties\_Family is used by an application to query the value of the **Font family** drop-down gallery.</span></span>

<span data-ttu-id="8e0ca-107">UI \_ PKEY \_ FontProperties 系列的值 \_ 符合以[>enumfontfamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa)函式或[ENUMFONTFAMILIESEX](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)函式取出的[Windows GDI 字型系列](../gdi/font-families.md)名稱。</span><span class="sxs-lookup"><span data-stu-id="8e0ca-107">The value of UI\_PKEY\_FontProperties\_Family matches a [Windows GDI Font Families](../gdi/font-families.md) name retrieved with the [EnumFontFamilies function](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) or [EnumFontFamiliesEx function](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).</span></span>

<span data-ttu-id="8e0ca-108">預設值為空字串。</span><span class="sxs-lookup"><span data-stu-id="8e0ca-108">The default value is an empty string.</span></span>

<span data-ttu-id="8e0ca-109">如果為 UI PKEY FontProperties 系列的值提供空字串 \_ \_ ，則 \_ 會清除字型選取範圍。</span><span class="sxs-lookup"><span data-stu-id="8e0ca-109">If an empty string is supplied for the value for UI\_PKEY\_FontProperties\_Family, then the font selection is cleared.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e0ca-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="8e0ca-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e0ca-111">字型控制項屬性</span><span class="sxs-lookup"><span data-stu-id="8e0ca-111">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="8e0ca-112">字型控制項</span><span class="sxs-lookup"><span data-stu-id="8e0ca-112">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 