---
title: UI_PKEY_FontProperties_Italic
description: 識別 UI \_ PKEY \_ FontProperties \_ 斜體屬性。
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00825807c57632b1bbea69c47bc9b90d705efa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375597"
---
# <a name="ui_pkey_fontproperties_italic"></a><span data-ttu-id="977dd-103">UI \_ PKEY \_ FontProperties \_ 斜體</span><span class="sxs-lookup"><span data-stu-id="977dd-103">UI\_PKEY\_FontProperties\_Italic</span></span>

<span data-ttu-id="977dd-104">識別 UI \_ PKEY \_ FontProperties \_ 斜體屬性。</span><span class="sxs-lookup"><span data-stu-id="977dd-104">Identifies the UI\_PKEY\_FontProperties\_Italic property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="977dd-105">備註</span><span class="sxs-lookup"><span data-stu-id="977dd-105">Remarks</span></span>

<span data-ttu-id="977dd-106">UI \_ PKEY \_ FontProperties \_ 斜體是由應用程式用來查詢 **斜體** 按鈕的狀態。</span><span class="sxs-lookup"><span data-stu-id="977dd-106">UI\_PKEY\_FontProperties\_Italic is used by an application to query the state of the **Italic** button.</span></span>

<span data-ttu-id="977dd-107">屬性值來自 [**UI \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) 列舉。</span><span class="sxs-lookup"><span data-stu-id="977dd-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="977dd-108">預設值是 `UI_FONTPROPERTIES_NOTSET`。</span><span class="sxs-lookup"><span data-stu-id="977dd-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="977dd-109">下表描述屬性和 UI 結果。</span><span class="sxs-lookup"><span data-stu-id="977dd-109">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="977dd-110">**斜體** 按鈕已停用，而且只能由應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="977dd-110">**Italic** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="977dd-111">未選取 [**斜體**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="977dd-111">**Italic** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="977dd-112">已選取 [**斜體**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="977dd-112">**Italic** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="977dd-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="977dd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="977dd-114">字型控制項屬性</span><span class="sxs-lookup"><span data-stu-id="977dd-114">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="977dd-115">**UI \_ FONTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="977dd-115">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="977dd-116">字型控制項</span><span class="sxs-lookup"><span data-stu-id="977dd-116">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 