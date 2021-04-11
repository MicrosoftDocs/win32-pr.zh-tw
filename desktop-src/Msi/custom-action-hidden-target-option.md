---
description: 使用下列選項旗標，指定安裝程式不會將輸入的值寫入至 CustomAction 資料表的目標欄位中。 若要設定選項，請將此資料表中的值加入至 CustomAction 資料表之 [類型] 欄位中的值。
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: 自訂動作隱藏目標選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acca69e4c3efc2b43302bf926a56bc53b2bf5e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026887"
---
# <a name="custom-action-hidden-target-option"></a><span data-ttu-id="53972-104">自訂動作隱藏目標選項</span><span class="sxs-lookup"><span data-stu-id="53972-104">Custom Action Hidden Target Option</span></span>

<span data-ttu-id="53972-105">使用下列選項旗標，指定安裝程式不會將輸入的值寫入至 [CustomAction 資料表](customaction-table.md) 的目標欄位中。</span><span class="sxs-lookup"><span data-stu-id="53972-105">Use the following option flags to specify that the installer not write the value entered into the Target field of the [CustomAction table](customaction-table.md) into the log.</span></span> <span data-ttu-id="53972-106">若要設定選項，請將此資料表中的值加入至 CustomAction 資料表之 [類型] 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="53972-106">To set the option add the value in this table to the value in the Type field of the CustomAction table.</span></span>



| <span data-ttu-id="53972-107">常數</span><span class="sxs-lookup"><span data-stu-id="53972-107">Constant</span></span>                            | <span data-ttu-id="53972-108">十六進位</span><span class="sxs-lookup"><span data-stu-id="53972-108">Hexadecimal</span></span> | <span data-ttu-id="53972-109">Decimal</span><span class="sxs-lookup"><span data-stu-id="53972-109">Decimal</span></span> | <span data-ttu-id="53972-110">Description</span><span class="sxs-lookup"><span data-stu-id="53972-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53972-111">(無)</span><span class="sxs-lookup"><span data-stu-id="53972-111">(none)</span></span>                              | <span data-ttu-id="53972-112">0x0000</span><span class="sxs-lookup"><span data-stu-id="53972-112">0x0000</span></span>      | <span data-ttu-id="53972-113">0</span><span class="sxs-lookup"><span data-stu-id="53972-113">0</span></span>       | <span data-ttu-id="53972-114">安裝程式可能會將 CustomAction 資料表的目標資料行中的值寫入記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="53972-114">The installer may write the value in the Target column of the CustomAction table into the log file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="53972-115">**msidbCustomActionTypeHideTarget**</span><span class="sxs-lookup"><span data-stu-id="53972-115">**msidbCustomActionTypeHideTarget**</span></span> | <span data-ttu-id="53972-116">0x2000</span><span class="sxs-lookup"><span data-stu-id="53972-116">0x2000</span></span>      | <span data-ttu-id="53972-117">8192</span><span class="sxs-lookup"><span data-stu-id="53972-117">8192</span></span>    | <span data-ttu-id="53972-118">安裝程式無法將 [CustomAction 資料表](customaction-table.md) 的目標資料行中的值寫入記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="53972-118">The installer is prevented from writing the value in the Target column of the [CustomAction table](customaction-table.md) into the log file.</span></span> <span data-ttu-id="53972-119">當安裝程式執行自訂動作時，也不會記錄 CustomActionData 屬性。</span><span class="sxs-lookup"><span data-stu-id="53972-119">The CustomActionData property is also not logged when the installer executes the custom action.</span></span><br/> <span data-ttu-id="53972-120">因為安裝程式會從與自訂動作相同名稱的屬性中設定 CustomActionData 的值，所以該屬性必須列在 [**MsiHiddenProperties**](msihiddenproperties.md) 屬性中，以防止其值出現在記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="53972-120">Because the installer sets the value of CustomActionData from a property with the same name as the custom action, that property must be listed in the [**MsiHiddenProperties**](msihiddenproperties.md) Property to prevent its value from appearing in the log.</span></span><br/> |



 

<span data-ttu-id="53972-121">如需詳細資訊，請參閱[防止機密資訊寫入記錄](preventing-confidential-information-from-being-written-into-the-log-file.md)檔</span><span class="sxs-lookup"><span data-stu-id="53972-121">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="53972-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="53972-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53972-123">自訂動作參考</span><span class="sxs-lookup"><span data-stu-id="53972-123">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="53972-124">關於自訂動作</span><span class="sxs-lookup"><span data-stu-id="53972-124">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="53972-125">使用自訂動作</span><span class="sxs-lookup"><span data-stu-id="53972-125">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 




