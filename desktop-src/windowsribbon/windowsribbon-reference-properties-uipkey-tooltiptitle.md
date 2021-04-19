---
title: UI_PKEY_TooltipTitle
description: 識別 UI \_ PKEY \_ TooltipTitle 屬性。
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e62fe9ebdb6418f5790e0073e32e81d7f7aba75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969664"
---
# <a name="ui_pkey_tooltiptitle"></a><span data-ttu-id="d7725-103">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="d7725-103">UI\_PKEY\_TooltipTitle</span></span>

<span data-ttu-id="d7725-104">識別 UI \_ PKEY \_ TooltipTitle 屬性。</span><span class="sxs-lookup"><span data-stu-id="d7725-104">Identifies the UI\_PKEY\_TooltipTitle property.</span></span>

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="d7725-105">備註</span><span class="sxs-lookup"><span data-stu-id="d7725-105">Remarks</span></span>

<span data-ttu-id="d7725-106">\_ \_ 應用程式會使用 [UI PKEY TooltipTitle] 來查詢索引標籤、群組、按鈕、圖庫專案和其他功能區控制項的工具提示。</span><span class="sxs-lookup"><span data-stu-id="d7725-106">UI\_PKEY\_TooltipTitle is used by an application to query the tooltip of tabs, groups, buttons, gallery items, and other Ribbon controls.</span></span>

<span data-ttu-id="d7725-107">屬性值是限制為任何字元序列（包括空白字元和分行符號字元）的字串。</span><span class="sxs-lookup"><span data-stu-id="d7725-107">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="d7725-108">使用通用字元集 (UCS) XML 字元參考 `&#xA;` 來指定分行符號。</span><span class="sxs-lookup"><span data-stu-id="d7725-108">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="d7725-109">不支援靠右對齊。</span><span class="sxs-lookup"><span data-stu-id="d7725-109">Right alignment is not supported.</span></span>

<span data-ttu-id="d7725-110">UI PKEY TooltipTitle 的最大長度未系結 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d7725-110">The maximum length of UI\_PKEY\_TooltipTitle is unbounded.</span></span>

<span data-ttu-id="d7725-111">若要在工具提示中顯示 & 符號，請將特殊字元指定以雙字元符號 (`&&`) ，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="d7725-111">To display an ampersand in a tooltip, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a><span data-ttu-id="d7725-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7725-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7725-113">資源屬性</span><span class="sxs-lookup"><span data-stu-id="d7725-113">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="d7725-114">**TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="d7725-114">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[<span data-ttu-id="d7725-115">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="d7725-115">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




