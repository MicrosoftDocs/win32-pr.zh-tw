---
title: Error。 item 方法
description: Item 方法會從錯誤佇列中取出 ErrorItem 物件。
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- item 方法 Windows Media Player
- item 方法 Windows Media Player，Error 類別
- Error 類別 Windows Media Player，item 方法
topic_type:
- apiref
api_name:
- Error.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5545df50fce05ff5a10a5f870d1ec07648434fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997667"
---
# <a name="erroritem-method"></a><span data-ttu-id="2f8a5-106">Error。 item 方法</span><span class="sxs-lookup"><span data-stu-id="2f8a5-106">Error.item method</span></span>

<span data-ttu-id="2f8a5-107">**Item** 方法會從錯誤佇列中取出 **ErrorItem** 物件。</span><span class="sxs-lookup"><span data-stu-id="2f8a5-107">The **item** method retrieves an **ErrorItem** object from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f8a5-108">語法</span><span class="sxs-lookup"><span data-stu-id="2f8a5-108">Syntax</span></span>


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="2f8a5-109">參數</span><span class="sxs-lookup"><span data-stu-id="2f8a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f8a5-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f8a5-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f8a5-111">**Number** (**Long**) ，其中包含要抓取之 **ErrorItem** 物件的索引。</span><span class="sxs-lookup"><span data-stu-id="2f8a5-111">**Number** (**long**) containing the index of the **ErrorItem** object to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f8a5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f8a5-112">Return value</span></span>

<span data-ttu-id="2f8a5-113">這個方法會傳回 **ErrorItem** 物件。</span><span class="sxs-lookup"><span data-stu-id="2f8a5-113">This method returns an **ErrorItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f8a5-114">備註</span><span class="sxs-lookup"><span data-stu-id="2f8a5-114">Remarks</span></span>

<span data-ttu-id="2f8a5-115">Windows Media Player 可能會產生一些錯誤，以回應錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="2f8a5-115">Windows Media Player can generate a number of errors in response to an error condition.</span></span> <span data-ttu-id="2f8a5-116">這個方法可讓您使用索引編號來抓取佇列中的特定錯誤。</span><span class="sxs-lookup"><span data-stu-id="2f8a5-116">This method allows the retrieval of a specific error in the queue by using an index number.</span></span> <span data-ttu-id="2f8a5-117">錯誤佇列的索引編號開頭為零。</span><span class="sxs-lookup"><span data-stu-id="2f8a5-117">The index numbers for the error queue begin with zero.</span></span>

<span data-ttu-id="2f8a5-118">您 *應該設定設定。* 如果您選擇顯示自訂錯誤訊息，請 **enableErrorDialogs** 為 false。</span><span class="sxs-lookup"><span data-stu-id="2f8a5-118">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="2f8a5-119">範例</span><span class="sxs-lookup"><span data-stu-id="2f8a5-119">Examples</span></span>

<span data-ttu-id="2f8a5-120">下列 JScript 範例會使用 *錯誤*。事件處理常式中的 **專案** 物件，警示使用者最新的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2f8a5-120">The following JScript example uses the *Error*.**item** object in an event handler to alert the user to the most recent error.</span></span> <span data-ttu-id="2f8a5-121">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="2f8a5-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE="JScript"  FOR=Player EVENT=error()>

// Store the most recent error item number.
var max = Player.error.errorCount - 1 

// Store the most recent error in an error item object.
var errItem = Player.error.item(max);

// Use the error item object to store the error info.
errDesc = errItem.errorDescription;
errNum = errItem.errorCode;

// Display the error info.
alert(errNum + "\n" + errDesc);

</SCRIPT> 

```



## <a name="requirements"></a><span data-ttu-id="2f8a5-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f8a5-122">Requirements</span></span>



| <span data-ttu-id="2f8a5-123">需求</span><span class="sxs-lookup"><span data-stu-id="2f8a5-123">Requirement</span></span> | <span data-ttu-id="2f8a5-124">值</span><span class="sxs-lookup"><span data-stu-id="2f8a5-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f8a5-125">版本</span><span class="sxs-lookup"><span data-stu-id="2f8a5-125">Version</span></span><br/> | <span data-ttu-id="2f8a5-126">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="2f8a5-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2f8a5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2f8a5-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="2f8a5-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f8a5-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f8a5-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f8a5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f8a5-130">**Error 物件**</span><span class="sxs-lookup"><span data-stu-id="2f8a5-130">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="2f8a5-131">**ErrorItem 物件**</span><span class="sxs-lookup"><span data-stu-id="2f8a5-131">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





