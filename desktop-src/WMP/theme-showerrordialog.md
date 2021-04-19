---
title: ShowErrorDialog
description: ShowErrorDialog 方法會顯示 [標準錯誤] 對話方塊。
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- ShowErrorDialog Windows Media Player
topic_type:
- apiref
api_name:
- THEME.showErrorDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdc1f9df13ec460ce780507e1bde38a2996f915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977529"
---
# <a name="themeshowerrordialog"></a><span data-ttu-id="afb88-104">ShowErrorDialog</span><span class="sxs-lookup"><span data-stu-id="afb88-104">THEME.showErrorDialog</span></span>

<span data-ttu-id="afb88-105">**ShowErrorDialog** 方法會顯示 [標準錯誤] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="afb88-105">The **showErrorDialog** method displays the standard error dialog box.</span></span>

``` syntax
        theme.showErrorDialog()
```

## <a name="parameters"></a><span data-ttu-id="afb88-106">參數</span><span class="sxs-lookup"><span data-stu-id="afb88-106">Parameters</span></span>

<span data-ttu-id="afb88-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="afb88-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="afb88-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="afb88-108">Return Value</span></span>

<span data-ttu-id="afb88-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="afb88-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="afb88-110">備註</span><span class="sxs-lookup"><span data-stu-id="afb88-110">Remarks</span></span>

<span data-ttu-id="afb88-111">如果 **enableErrorDialogs** 為 false，則可以使用這個方法，以程式設計方式顯示錯誤對話方塊。</span><span class="sxs-lookup"><span data-stu-id="afb88-111">If **Settings.enableErrorDialogs** is false, this method can be used to programmatically display the error dialog.</span></span> <span data-ttu-id="afb88-112">如果錯誤佇列中沒有任何錯誤，則不會顯示 [錯誤] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="afb88-112">If there are no errors in the error queue, the error dialog box is not shown.</span></span>

<span data-ttu-id="afb88-113">若為 Windows Media Player 9 系列或更新版本，則必須從錯誤事件處理常式呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="afb88-113">For Windows Media Player 9 Series or later, this method must be called from the error event handler.</span></span> <span data-ttu-id="afb88-114">Windows Media Player 9 系列或更新版本會在引發錯誤事件之後，清除面板的錯誤佇列。</span><span class="sxs-lookup"><span data-stu-id="afb88-114">Windows Media Player 9 Series or later clears the error queue for skins after the error event has been fired.</span></span>

## <a name="requirements"></a><span data-ttu-id="afb88-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="afb88-115">Requirements</span></span>



| <span data-ttu-id="afb88-116">需求</span><span class="sxs-lookup"><span data-stu-id="afb88-116">Requirement</span></span> | <span data-ttu-id="afb88-117">值</span><span class="sxs-lookup"><span data-stu-id="afb88-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="afb88-118">版本</span><span class="sxs-lookup"><span data-stu-id="afb88-118">Version</span></span><br/> | <span data-ttu-id="afb88-119">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="afb88-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="afb88-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afb88-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afb88-121">**主題元素**</span><span class="sxs-lookup"><span data-stu-id="afb88-121">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="afb88-122">**設定. enableErrorDialogs**</span><span class="sxs-lookup"><span data-stu-id="afb88-122">**Settings.enableErrorDialogs**</span></span>](settings-enableerrordialogs.md)
</dt> </dl>

 

 





