---
title: ClosedCaption.SAMILang
description: SAMILang 屬性會指定或抓取隱藏式輔助字幕所顯示的語言。
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- ClosedCaption. SAMILang Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILang
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae99b9a164e29b4adeb2fd7b23a1b79945dcb26e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977664"
---
# <a name="closedcaptionsamilang"></a><span data-ttu-id="35ea9-104">ClosedCaption.SAMILang</span><span class="sxs-lookup"><span data-stu-id="35ea9-104">ClosedCaption.SAMILang</span></span>

<span data-ttu-id="35ea9-105">**SAMILang** 屬性會指定或抓取隱藏式輔助字幕所顯示的語言。</span><span class="sxs-lookup"><span data-stu-id="35ea9-105">The **SAMILang** property specifies or retrieves the language displayed for closed captioning.</span></span>

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a><span data-ttu-id="35ea9-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="35ea9-106">Possible Values</span></span>

<span data-ttu-id="35ea9-107">這個屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="35ea9-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="35ea9-108">備註</span><span class="sxs-lookup"><span data-stu-id="35ea9-108">Remarks</span></span>

<span data-ttu-id="35ea9-109">薩米文檔案可以包含一或多個語言的文字。</span><span class="sxs-lookup"><span data-stu-id="35ea9-109">A SAMI file can contain text for one or many languages.</span></span> <span data-ttu-id="35ea9-110">隱藏式字幕的可用語言會定義于薩米文檔案的 <STYLE> 和 </STYLE> 標記之間。</span><span class="sxs-lookup"><span data-stu-id="35ea9-110">The languages available for closed captioning are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="35ea9-111">語言識別項是使用唯一的英數位元字串所指定，該字串前面會加上句點 (。 ) 。</span><span class="sxs-lookup"><span data-stu-id="35ea9-111">A language identifier is specified with a unique alphanumeric string that is preceded by a period (.).</span></span> <span data-ttu-id="35ea9-112">針對語言指定的名稱可以是任何字串。</span><span class="sxs-lookup"><span data-stu-id="35ea9-112">The name specified for a language can be any string.</span></span> <span data-ttu-id="35ea9-113">例如，下列程式可用來定義美式英文：</span><span class="sxs-lookup"><span data-stu-id="35ea9-113">For example, the following could be used to define US English:</span></span>


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



<span data-ttu-id="35ea9-114">如果未指定薩米文語言，預設會使用薩米文檔案中定義的第一種語言。</span><span class="sxs-lookup"><span data-stu-id="35ea9-114">If no SAMI language is specified, the first language defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="35ea9-115">您使用 *ClosedCaption* 傳遞的值。**SAMILang** 必須符合語言規範中的 **Name** 屬性。</span><span class="sxs-lookup"><span data-stu-id="35ea9-115">The value you pass using *ClosedCaption*.**SAMILang** must match the **Name** attribute in the language specifier.</span></span>

<span data-ttu-id="35ea9-116">**Windows Media Player 10** 行動裝置版：這個屬性是唯讀的，而且一律會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="35ea9-116">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="35ea9-117">範例</span><span class="sxs-lookup"><span data-stu-id="35ea9-117">Examples</span></span>

<span data-ttu-id="35ea9-118">下列 JScript 範例會使用 *ClosedCaption*。在 HTML SELECT 元素中 **SAMILang** ，以指定隱藏式輔助字幕語言。</span><span class="sxs-lookup"><span data-stu-id="35ea9-118">The following JScript example uses *ClosedCaption*.**SAMILang** in an HTML SELECT element to specify the closed caption language.</span></span> <span data-ttu-id="35ea9-119">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="35ea9-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCLANG  NAME = "CCLANG"  LANGUAGE = "JScript"

     /* Set the closed caption language when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMILang = CCLANG.value;
        ">

        /* Fill in the SELECT element options. */
           <OPTION VALUE = "'Spanish Captions'">Spanish
           <OPTION VALUE = "'Japanese Captions'">Japanese
           <OPTION VALUE = "'English Captions'">English
           <OPTION VALUE = "'French Captions'">French
           <OPTION VALUE = "'German Captions'" SELECTED>German
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="35ea9-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="35ea9-120">Requirements</span></span>



| <span data-ttu-id="35ea9-121">需求</span><span class="sxs-lookup"><span data-stu-id="35ea9-121">Requirement</span></span> | <span data-ttu-id="35ea9-122">值</span><span class="sxs-lookup"><span data-stu-id="35ea9-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35ea9-123">版本</span><span class="sxs-lookup"><span data-stu-id="35ea9-123">Version</span></span><br/> | <span data-ttu-id="35ea9-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="35ea9-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="35ea9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="35ea9-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="35ea9-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35ea9-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ea9-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35ea9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ea9-128">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="35ea9-128">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="35ea9-129">**ClosedCaption 物件**</span><span class="sxs-lookup"><span data-stu-id="35ea9-129">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





