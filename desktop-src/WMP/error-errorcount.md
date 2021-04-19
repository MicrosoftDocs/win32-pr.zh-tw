---
title: 錯誤。 errorCount
description: ErrorCount 屬性會捕獲錯誤佇列中的錯誤數目。
ms.assetid: 64d9bb0a-fcc4-401b-a7bd-529e1a517f3b
keywords:
- 錯誤。 errorCount Windows Media Player
topic_type:
- apiref
api_name:
- Error.errorCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94848023d2cd331545f97d3bea6d92f2fcd4b49c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985959"
---
# <a name="errorerrorcount"></a><span data-ttu-id="5afd7-104">錯誤。 errorCount</span><span class="sxs-lookup"><span data-stu-id="5afd7-104">Error.errorCount</span></span>

<span data-ttu-id="5afd7-105">**ErrorCount** 屬性會捕獲錯誤佇列中的錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="5afd7-105">The **errorCount** property retrieves the number of errors in the error queue.</span></span>

``` syntax
player.error.errorCount
      
```

## <a name="possible-values"></a><span data-ttu-id="5afd7-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="5afd7-106">Possible Values</span></span>

<span data-ttu-id="5afd7-107">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="5afd7-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="5afd7-108">備註</span><span class="sxs-lookup"><span data-stu-id="5afd7-108">Remarks</span></span>

<span data-ttu-id="5afd7-109">您 *應該設定設定。* 如果您選擇顯示自訂錯誤訊息，請 **enableErrorDialogs** 為 false。</span><span class="sxs-lookup"><span data-stu-id="5afd7-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="5afd7-110">範例</span><span class="sxs-lookup"><span data-stu-id="5afd7-110">Examples</span></span>

<span data-ttu-id="5afd7-111">下列 JScript 範例使用 *錯誤*。在事件處理常式中 **errorCount** ，以警示使用者錯誤佇列中的最新錯誤。</span><span class="sxs-lookup"><span data-stu-id="5afd7-111">The following JScript example uses *Error*.**errorCount** in an event handler to alert the user about the most recent error in the error queue.</span></span> <span data-ttu-id="5afd7-112">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="5afd7-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount;

// Get the description of the last error. Error items start at zero,
// so the item index will always be one less than the error count.
var errDesc = Player.error.item(max-1).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="5afd7-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5afd7-113">Requirements</span></span>



| <span data-ttu-id="5afd7-114">需求</span><span class="sxs-lookup"><span data-stu-id="5afd7-114">Requirement</span></span> | <span data-ttu-id="5afd7-115">值</span><span class="sxs-lookup"><span data-stu-id="5afd7-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5afd7-116">版本</span><span class="sxs-lookup"><span data-stu-id="5afd7-116">Version</span></span><br/> | <span data-ttu-id="5afd7-117">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="5afd7-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5afd7-118">DLL</span><span class="sxs-lookup"><span data-stu-id="5afd7-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="5afd7-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5afd7-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5afd7-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5afd7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5afd7-121">**Error 物件**</span><span class="sxs-lookup"><span data-stu-id="5afd7-121">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





