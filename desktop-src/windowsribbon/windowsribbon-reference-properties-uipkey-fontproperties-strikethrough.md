---
title: UI_PKEY_FontProperties_Strikethrough
description: 識別 UI \_ PKEY \_ FontProperties \_ 刪除線屬性。
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07804a74671bb219b34b1c67580af083fd5c34c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382537"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a><span data-ttu-id="00327-103">UI \_ PKEY \_ FontProperties \_ 刪除線</span><span class="sxs-lookup"><span data-stu-id="00327-103">UI\_PKEY\_FontProperties\_Strikethrough</span></span>

<span data-ttu-id="00327-104">識別 UI \_ PKEY \_ FontProperties \_ 刪除線屬性。</span><span class="sxs-lookup"><span data-stu-id="00327-104">Identifies the UI\_PKEY\_FontProperties\_Strikethrough property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="00327-105">備註</span><span class="sxs-lookup"><span data-stu-id="00327-105">Remarks</span></span>

<span data-ttu-id="00327-106">\_ \_ \_ 應用程式會使用 UI PKEY FontProperties 刪除線來查詢 **刪除線** 按鈕的狀態。</span><span class="sxs-lookup"><span data-stu-id="00327-106">UI\_PKEY\_FontProperties\_Strikethrough is used by an application to query the state of the **Strikethrough** button.</span></span>

<span data-ttu-id="00327-107">屬性值來自 [**UI \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) 列舉。</span><span class="sxs-lookup"><span data-stu-id="00327-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="00327-108">預設值是 `UI_FONTPROPERTIES_NOTSET`。</span><span class="sxs-lookup"><span data-stu-id="00327-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="00327-109">下列螢幕擷取畫面顯示功能區 [**FontControl**](windowsribbon-element-fontcontrol.md)的 **刪除線** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="00327-109">The following screen shot shows the **Strikethrough** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![fontcontrol 專案的螢幕擷取畫面，其中 richfont 屬性設定為 true。](images/markup/fontcontrol-strikethrough.png)

<span data-ttu-id="00327-111">下表描述屬性和 UI 結果。</span><span class="sxs-lookup"><span data-stu-id="00327-111">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                              |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="00327-112">**刪除線** 按鈕已停用，而且只能由應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="00327-112">**Strikethrough** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="00327-113">未選取 **刪除線** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="00327-113">**Strikethrough** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="00327-114">已選取 **刪除線** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="00327-114">**Strikethrough** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="00327-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="00327-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00327-116">字型控制項屬性</span><span class="sxs-lookup"><span data-stu-id="00327-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="00327-117">**UI \_ FONTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="00327-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="00327-118">字型控制項</span><span class="sxs-lookup"><span data-stu-id="00327-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 