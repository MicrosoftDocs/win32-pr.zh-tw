---
title: ErrorItem. errorDescription
description: ErrorDescription 屬性會捕獲錯誤的描述。
ms.assetid: 7fd16c3d-1460-41b5-81ca-2636d7a1d0d1
keywords:
- ErrorItem. errorDescription Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorDescription
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0de19bb67a5846a82e87d091f95a18cd12c5c2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985969"
---
# <a name="erroritemerrordescription"></a><span data-ttu-id="9b25b-104">ErrorItem. errorDescription</span><span class="sxs-lookup"><span data-stu-id="9b25b-104">ErrorItem.errorDescription</span></span>

<span data-ttu-id="9b25b-105">**ErrorDescription** 屬性會捕獲錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="9b25b-105">The **errorDescription** property retrieves a description of the error.</span></span>

``` syntax
player.error.item(
        index
        ).errorDescription
```

## <a name="possible-values"></a><span data-ttu-id="9b25b-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="9b25b-106">Possible Values</span></span>

<span data-ttu-id="9b25b-107">這個屬性是唯讀 **字串**。</span><span class="sxs-lookup"><span data-stu-id="9b25b-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b25b-108">備註</span><span class="sxs-lookup"><span data-stu-id="9b25b-108">Remarks</span></span>

<span data-ttu-id="9b25b-109">您 *應該設定設定。* 如果您選擇顯示自訂錯誤訊息，請 **enableErrorDialogs** 為 false。</span><span class="sxs-lookup"><span data-stu-id="9b25b-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="9b25b-110">範例</span><span class="sxs-lookup"><span data-stu-id="9b25b-110">Examples</span></span>

<span data-ttu-id="9b25b-111">下列 JScript 範例會使用 *ErrorItem*。**errorDescription** 事件處理常式，以向使用者顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="9b25b-111">The following JScript example uses *ErrorItem*.**errorDescription** in an event handler to display the error message to the user.</span></span> <span data-ttu-id="9b25b-112">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="9b25b-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error description for the first error item.
errDesc = Player.error.item(0).errorDescription;

// Display the error code.
var message = "Error: " + errDesc";
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="9b25b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b25b-113">Requirements</span></span>



| <span data-ttu-id="9b25b-114">需求</span><span class="sxs-lookup"><span data-stu-id="9b25b-114">Requirement</span></span> | <span data-ttu-id="9b25b-115">值</span><span class="sxs-lookup"><span data-stu-id="9b25b-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b25b-116">版本</span><span class="sxs-lookup"><span data-stu-id="9b25b-116">Version</span></span><br/> | <span data-ttu-id="9b25b-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="9b25b-117">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="9b25b-118">DLL</span><span class="sxs-lookup"><span data-stu-id="9b25b-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="9b25b-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b25b-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b25b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b25b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b25b-121">**ErrorItem 物件**</span><span class="sxs-lookup"><span data-stu-id="9b25b-121">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





