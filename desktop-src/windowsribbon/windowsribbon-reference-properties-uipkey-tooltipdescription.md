---
title: UI_PKEY_TooltipDescription
description: 識別 UI \_ PKEY \_ TooltipDescription 屬性。
ms.assetid: 658e798a-f41e-4538-94ac-38a9cb20dd74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 900610c1302d3cc904dcde2d7c86801982fd4d10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968867"
---
# <a name="ui_pkey_tooltipdescription"></a><span data-ttu-id="2af90-103">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="2af90-103">UI\_PKEY\_TooltipDescription</span></span>

<span data-ttu-id="2af90-104">識別 UI \_ PKEY \_ TooltipDescription 屬性。</span><span class="sxs-lookup"><span data-stu-id="2af90-104">Identifies the UI\_PKEY\_TooltipDescription property.</span></span>

```
propertyDescription
   name = UI_PKEY_TooltipDescription
   shellPKey = UI_PKEY_TooltipDescription
   formatID = 00000005-7363-696e-8441798acf5aebb7
   propID = 5
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="2af90-105">備註</span><span class="sxs-lookup"><span data-stu-id="2af90-105">Remarks</span></span>

<span data-ttu-id="2af90-106">\_ \_ 應用程式會使用 ui PKEY TooltipDescription 來查詢與[UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)相關聯的描述。</span><span class="sxs-lookup"><span data-stu-id="2af90-106">UI\_PKEY\_TooltipDescription is used by an application to query the description associated with a [UI\_PKEY\_TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md).</span></span>

<span data-ttu-id="2af90-107">屬性值是限制為任何字元序列（包括空白字元和分行符號字元）的字串。</span><span class="sxs-lookup"><span data-stu-id="2af90-107">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="2af90-108">使用通用字元集 (UCS) XML 字元參考 `&#xA;` 來指定分行符號。</span><span class="sxs-lookup"><span data-stu-id="2af90-108">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="2af90-109">UI PKEY TooltipDescription 的最大長度未系結 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="2af90-109">The maximum length of UI\_PKEY\_TooltipDescription is unbounded.</span></span>

<span data-ttu-id="2af90-110">不支援靠右對齊。</span><span class="sxs-lookup"><span data-stu-id="2af90-110">Right alignment is not supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2af90-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="2af90-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2af90-112">資源屬性</span><span class="sxs-lookup"><span data-stu-id="2af90-112">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="2af90-113">**TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="2af90-113">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)
</dt> <dt>

[<span data-ttu-id="2af90-114">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="2af90-114">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 




