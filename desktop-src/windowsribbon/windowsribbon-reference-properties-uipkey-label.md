---
title: UI_PKEY_Label
description: 識別 UI \_ PKEY \_ 標籤屬性。
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245ce8d239e1a0893c907a047aa9a48996cbf606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840300"
---
# <a name="ui_pkey_label"></a><span data-ttu-id="2c47b-103">UI \_ PKEY \_ 標籤</span><span class="sxs-lookup"><span data-stu-id="2c47b-103">UI\_PKEY\_Label</span></span>

<span data-ttu-id="2c47b-104">識別 UI \_ PKEY \_ 標籤屬性。</span><span class="sxs-lookup"><span data-stu-id="2c47b-104">Identifies the UI\_PKEY\_Label property.</span></span>

```
propertyDescription
   name = UI_PKEY_Label
   shellPKey = UI_PKEY_Label
   formatID = 00000004-7363-696e-8441798acf5aebb7
   propID = 4
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="2c47b-105">備註</span><span class="sxs-lookup"><span data-stu-id="2c47b-105">Remarks</span></span>

<span data-ttu-id="2c47b-106">UI \_ PKEY \_ 標籤是由應用程式用來查詢索引標籤、群組、按鈕、圖庫專案和其他功能區控制項的標籤文字。</span><span class="sxs-lookup"><span data-stu-id="2c47b-106">UI\_PKEY\_Label is used by an application to query the label text of tabs, groups, buttons, gallery items, and other Ribbon controls.</span></span>

> [!Note]  
> <span data-ttu-id="2c47b-107">Windows 8 和更新版本： [應用程式功能表](windowsribbon-controls-applicationmenu.md) 按鈕影像已變更為 Label： **File**。</span><span class="sxs-lookup"><span data-stu-id="2c47b-107">Windows 8 and newer: [Application Menu](windowsribbon-controls-applicationmenu.md) button image changed to label: **File**.</span></span> <span data-ttu-id="2c47b-108">建議您不要使用 [檔案] 作為任何您自己的索引標籤的標籤。</span><span class="sxs-lookup"><span data-stu-id="2c47b-108">We recommend that you do not use File as the label for any of your own tabs.</span></span>

 

<span data-ttu-id="2c47b-109">屬性值是限制為任何字元序列（包括空白字元和分行符號字元）的字串。</span><span class="sxs-lookup"><span data-stu-id="2c47b-109">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="2c47b-110">使用通用字元集 (UCS) XML 字元參考 `&#xA;` 來指定分行符號。</span><span class="sxs-lookup"><span data-stu-id="2c47b-110">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="2c47b-111">不支援靠右對齊。</span><span class="sxs-lookup"><span data-stu-id="2c47b-111">Right alignment is not supported.</span></span>

<span data-ttu-id="2c47b-112">UI PKEY 標籤的最大長度 \_ \_ 為未系結。</span><span class="sxs-lookup"><span data-stu-id="2c47b-112">The maximum length of UI\_PKEY\_Label is unbounded.</span></span>

<span data-ttu-id="2c47b-113">如果命令是透過功能表項目公開，而且 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 或 UI \_ PKEY \_ 標籤的值包含前面加上連字號的字母，如下列範例所示，則會將這個字母視為使用者介面的快速鍵，以及功能區架構的鍵盤對應鍵。</span><span class="sxs-lookup"><span data-stu-id="2c47b-113">If a Command is exposed through a menu item and the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or UI\_PKEY\_Label contains a letter preceded by an ampersand, as shown in the following example, this letter is treated as both a keytip and a keyboard accelerator for that Command by the Ribbon framework.</span></span>


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



<span data-ttu-id="2c47b-114">若要在標籤中顯示 & 符號，請將特殊字元指定換成雙符號 (`&&`) ，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="2c47b-114">To display an ampersand in a label, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a><span data-ttu-id="2c47b-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c47b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c47b-116">資源屬性</span><span class="sxs-lookup"><span data-stu-id="2c47b-116">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="2c47b-117">**LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="2c47b-117">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[<span data-ttu-id="2c47b-118">UI \_ PKEY \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="2c47b-118">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




