---
title: UI_PKEY_FontProperties_DeltaSize
description: 識別 UI \_ PKEY \_ FontProperties \_ DeltaSize 屬性。
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67778a710de8f69e0aea1134c12fb9ee3ebe0133
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444389"
---
# <a name="ui_pkey_fontproperties_deltasize"></a><span data-ttu-id="dfabd-103">UI \_ PKEY \_ FontProperties \_ DeltaSize</span><span class="sxs-lookup"><span data-stu-id="dfabd-103">UI\_PKEY\_FontProperties\_DeltaSize</span></span>

<span data-ttu-id="dfabd-104">識別 UI \_ PKEY \_ FontProperties \_ DeltaSize 屬性。</span><span class="sxs-lookup"><span data-stu-id="dfabd-104">Identifies the UI\_PKEY\_FontProperties\_DeltaSize property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a><span data-ttu-id="dfabd-105">備註</span><span class="sxs-lookup"><span data-stu-id="dfabd-105">Remarks</span></span>

<span data-ttu-id="dfabd-106">\_ \_ \_ 如果應用程式無法指定 **字型大小** 值（例如選取了 [執行 heterogeneously 大小的文字]），應用程式就會使用 UI PKEY FontProperties DeltaSize。</span><span class="sxs-lookup"><span data-stu-id="dfabd-106">UI\_PKEY\_FontProperties\_DeltaSize is used by an application in cases where it is not possible for the application to specify a value for **Font size**, such as when a run of heterogeneously sized text is selected.</span></span> <span data-ttu-id="dfabd-107">**字型大小** 控制項設為空白，而 UI \_ PKEY \_ FontProperties \_ DeltaSize 用來捕捉使用者與 **字型成長** 和 **字型壓縮** 按鈕的互動。</span><span class="sxs-lookup"><span data-stu-id="dfabd-107">The **Font size** control is set to blank and UI\_PKEY\_FontProperties\_DeltaSize is used to capture user interaction with the **Font grow** and **Font shrink** buttons.</span></span>

<span data-ttu-id="dfabd-108">Ui \_ PKEY \_ FontProperties \_ DeltaSize 包含在 [ui \_ PKEY \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md)中。</span><span class="sxs-lookup"><span data-stu-id="dfabd-108">UI\_PKEY\_FontProperties\_DeltaSize is included in [UI\_PKEY\_FontProperties\_ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span></span>

<span data-ttu-id="dfabd-109">下列螢幕擷取畫面顯示功能區 [**FontControl**](windowsribbon-element-fontcontrol.md)的 **字型成長** 和 **字型壓縮** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="dfabd-109">The following screen shot shows the **Font grow** and **Font shrink** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![fontcontrol 上字型成長和字型壓縮按鈕的螢幕擷取畫面。](images/markup/fontcontrol-incdec.png)

<span data-ttu-id="dfabd-111">下表描述屬性值。</span><span class="sxs-lookup"><span data-stu-id="dfabd-111">The following table describes the property values.</span></span>



|     <span data-ttu-id="dfabd-112">值</span><span class="sxs-lookup"><span data-stu-id="dfabd-112">Value</span></span>                 |  <span data-ttu-id="dfabd-113">描述</span><span class="sxs-lookup"><span data-stu-id="dfabd-113">Description</span></span>                    |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | <span data-ttu-id="dfabd-114">已按下 [**放大] 字型** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="dfabd-114">**Grow font** button clicked.</span></span>   |
| `UI_FONTDELTASIZE_SHRINK` | <span data-ttu-id="dfabd-115">按一下 [**縮小字型**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="dfabd-115">**Shrink font** button clicked.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="dfabd-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="dfabd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfabd-117">字型控制項屬性</span><span class="sxs-lookup"><span data-stu-id="dfabd-117">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="dfabd-118">**UI \_ FONTDELTASIZE**</span><span class="sxs-lookup"><span data-stu-id="dfabd-118">**UI\_FONTDELTASIZE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[<span data-ttu-id="dfabd-119">字型控制項</span><span class="sxs-lookup"><span data-stu-id="dfabd-119">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 