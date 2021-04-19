---
title: ClearErrorQueue 方法
description: ClearErrorQueue 方法會清除錯誤佇列中的錯誤。 |ClearErrorQueue 方法
ms.assetid: 306f0700-88b1-4433-8abb-7d225e82060a
keywords:
- clearErrorQueue 方法 Windows Media Player
- clearErrorQueue 方法 Windows Media Player，Error 類別
- Error 類別 Windows Media Player，clearErrorQueue 方法
topic_type:
- apiref
api_name:
- Error.clearErrorQueue
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b756708b8f0643f86489c26dd921e87c408be8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999208"
---
# <a name="errorclearerrorqueue-method"></a><span data-ttu-id="8caa7-107">ClearErrorQueue 方法</span><span class="sxs-lookup"><span data-stu-id="8caa7-107">Error.clearErrorQueue method</span></span>

<span data-ttu-id="8caa7-108">**ClearErrorQueue** 方法會清除錯誤佇列中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8caa7-108">The **clearErrorQueue** method clears the errors from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="8caa7-109">語法</span><span class="sxs-lookup"><span data-stu-id="8caa7-109">Syntax</span></span>


```JScript
Error.clearErrorQueue()
```



## <a name="parameters"></a><span data-ttu-id="8caa7-110">參數</span><span class="sxs-lookup"><span data-stu-id="8caa7-110">Parameters</span></span>

<span data-ttu-id="8caa7-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8caa7-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8caa7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8caa7-112">Return value</span></span>

<span data-ttu-id="8caa7-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8caa7-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8caa7-114">備註</span><span class="sxs-lookup"><span data-stu-id="8caa7-114">Remarks</span></span>

<span data-ttu-id="8caa7-115">在處理一系列的錯誤之後，這個方法會很有用來清除錯誤佇列。</span><span class="sxs-lookup"><span data-stu-id="8caa7-115">This method is useful to clear the error queue after a series of errors has been processed.</span></span>

<span data-ttu-id="8caa7-116">您 *應該設定設定。* 如果您選擇顯示自訂錯誤訊息，請 **enableErrorDialogs** 為 false。</span><span class="sxs-lookup"><span data-stu-id="8caa7-116">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="8caa7-117">範例</span><span class="sxs-lookup"><span data-stu-id="8caa7-117">Examples</span></span>

<span data-ttu-id="8caa7-118">下列 JScript 範例使用 *錯誤*。**clearErrorQueue** 事件處理常式，在顯示所有錯誤描述之後清空錯誤佇列。</span><span class="sxs-lookup"><span data-stu-id="8caa7-118">The following JScript example uses *Error*.**clearErrorQueue** in an event handler to empty the error queue after all error descriptions are displayed.</span></span> <span data-ttu-id="8caa7-119">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="8caa7-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount 

// Loop through the list of errors.
for (var i = 0; i < max; i++){
    // Get the error description for this item.
    var errDesc = Player.error.item(i).errorDescription;
    
    // Display the error message.
    alert(errDesc);
}

// Clear the error queue to prepare for the next group of errors.
Player.error.clearErrorQueue();

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="8caa7-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="8caa7-120">Requirements</span></span>



| <span data-ttu-id="8caa7-121">需求</span><span class="sxs-lookup"><span data-stu-id="8caa7-121">Requirement</span></span> | <span data-ttu-id="8caa7-122">值</span><span class="sxs-lookup"><span data-stu-id="8caa7-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8caa7-123">版本</span><span class="sxs-lookup"><span data-stu-id="8caa7-123">Version</span></span><br/> | <span data-ttu-id="8caa7-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8caa7-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8caa7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8caa7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="8caa7-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8caa7-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8caa7-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8caa7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8caa7-128">**Error 物件**</span><span class="sxs-lookup"><span data-stu-id="8caa7-128">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





