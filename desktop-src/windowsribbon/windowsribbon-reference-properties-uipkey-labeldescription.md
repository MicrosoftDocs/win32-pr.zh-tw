---
title: UI_PKEY_LabelDescription
description: 識別 UI \_ PKEY \_ LabelDescription 屬性。
ms.assetid: e7dfbe7e-c9c9-44fe-9e2d-39e20f5f7062
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb81e723d5f55dcfd63f1bb89bff4741b4e088e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840299"
---
# <a name="ui_pkey_labeldescription"></a><span data-ttu-id="fa484-103">UI \_ PKEY \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="fa484-103">UI\_PKEY\_LabelDescription</span></span>

<span data-ttu-id="fa484-104">識別 UI \_ PKEY \_ LabelDescription 屬性。</span><span class="sxs-lookup"><span data-stu-id="fa484-104">Identifies the UI\_PKEY\_LabelDescription property.</span></span>

```
propertyDescription
   name = UI_PKEY_LabelDescription
   shellPKey = UI_PKEY_LabelDescription
   formatID = 00000002-7363-696e-8441798acf5aebb7
   propID = 2
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="fa484-105">備註</span><span class="sxs-lookup"><span data-stu-id="fa484-105">Remarks</span></span>

<span data-ttu-id="fa484-106">\_ \_ 應用程式會使用 ui PKEY LabelDescription 來查詢與[UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)相關聯的描述。</span><span class="sxs-lookup"><span data-stu-id="fa484-106">UI\_PKEY\_LabelDescription is used by an application to query the description associated with a [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span>

<span data-ttu-id="fa484-107">屬性值是限制為任何字元序列（包括空白字元和分行符號字元）的字串。</span><span class="sxs-lookup"><span data-stu-id="fa484-107">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="fa484-108">使用通用字元集 (UCS) XML 字元參考 `&#xA;` 來指定分行符號。</span><span class="sxs-lookup"><span data-stu-id="fa484-108">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="fa484-109">長度上限為未系結。</span><span class="sxs-lookup"><span data-stu-id="fa484-109">The maximum length is unbounded.</span></span>

<span data-ttu-id="fa484-110">不支援靠右對齊。</span><span class="sxs-lookup"><span data-stu-id="fa484-110">Right alignment is not supported.</span></span>

<span data-ttu-id="fa484-111">下列螢幕擷取畫面說明如何在應用程式功能表中使用標籤和相關聯的標籤描述。</span><span class="sxs-lookup"><span data-stu-id="fa484-111">The following screen shot illustrates the use of a label and an associated label description in an Application Menu.</span></span>

![螢幕擷取畫面：顯示應用程式功能表中的標籤和相關聯的標籤描述。](images/properties/ui-pkey-labeldescription.png)

## <a name="related-topics"></a><span data-ttu-id="fa484-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa484-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa484-114">資源屬性</span><span class="sxs-lookup"><span data-stu-id="fa484-114">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="fa484-115">**LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="fa484-115">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)
</dt> <dt>

[<span data-ttu-id="fa484-116">UI \_ PKEY \_ 標籤</span><span class="sxs-lookup"><span data-stu-id="fa484-116">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 




