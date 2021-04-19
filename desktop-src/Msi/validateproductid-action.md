---
description: ValidateProductID 動作會將 [ProductID] 屬性設定為 [完整產品識別碼]。
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: ValidateProductID 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0f9f58641e8e24d73a1acae0b79cc0b875aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970229"
---
# <a name="validateproductid-action"></a><span data-ttu-id="7c5b7-103">ValidateProductID 動作</span><span class="sxs-lookup"><span data-stu-id="7c5b7-103">ValidateProductID Action</span></span>

<span data-ttu-id="7c5b7-104">ValidateProductID 動作會將 [ [**ProductID**](productid.md) ] 屬性設定為 [完整產品識別碼]。</span><span class="sxs-lookup"><span data-stu-id="7c5b7-104">The ValidateProductID action sets the [**ProductID**](productid.md) property to the full product identifier.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="7c5b7-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="7c5b7-105">Sequence Restrictions</span></span>

<span data-ttu-id="7c5b7-106">此動作必須在[InstallUISequence 資料表](installuisequence-table.md)中的使用者介面 wizard 之前，以及[InstallExecuteSequence 資料表](installexecutesequence-table.md)中的[RegisterUser 動作](registeruser-action.md)之前排序。</span><span class="sxs-lookup"><span data-stu-id="7c5b7-106">This action must be sequenced before the user interface wizard in the [InstallUISequence table](installuisequence-table.md) and before the [RegisterUser action](registeruser-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="7c5b7-107">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="7c5b7-107">ActionData Messages</span></span>

<span data-ttu-id="7c5b7-108">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="7c5b7-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c5b7-109">備註</span><span class="sxs-lookup"><span data-stu-id="7c5b7-109">Remarks</span></span>

<span data-ttu-id="7c5b7-110">安裝程式會檢查 [**ProductID**](productid.md) 屬性，檢查產品是否已成功驗證。</span><span class="sxs-lookup"><span data-stu-id="7c5b7-110">The installer checks whether a product has validated successfully by checking the [**ProductID**](productid.md) property.</span></span> <span data-ttu-id="7c5b7-111">在成功驗證之後，安裝程式會將 **ProductID** 屬性設定為完整產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="7c5b7-111">The installer sets the **ProductID** property to the full product identifier after a successful validation.</span></span> <span data-ttu-id="7c5b7-112">如果已成功驗證或由其他方法設定 **ProductID** 屬性，ValidateProductID 動作不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="7c5b7-112">The ValidateProductID action does nothing if the **ProductID** property has already been set by a successful validation or by another method.</span></span>

<span data-ttu-id="7c5b7-113">無論產品識別碼是否有效，ValidateProductID 動作一律會傳回成功，以便在第一次執行產品時，于命令列上輸入產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="7c5b7-113">The ValidateProductID action always returns a success, whether or not the product identifier is valid, so that the product identifier can be entered on the command line the first time the product is run.</span></span>

<span data-ttu-id="7c5b7-114">您可以在命令列上設定 [**PIDKEY**](pidkey.md) 屬性，或使用轉換，以驗證產品識別碼，而不需要讓使用者重新輸入這項資訊。</span><span class="sxs-lookup"><span data-stu-id="7c5b7-114">The product identifier can be validated without having the user reenter this information by setting the [**PIDKEY**](pidkey.md) property on the command line or by using a transform.</span></span> <span data-ttu-id="7c5b7-115">接著，您可以在 **PIDKEY** 屬性驗證時設定 [**ProductID**](productid.md)屬性的情況下，讓要求使用者輸入產品識別碼的對話方塊顯示成為條件式。</span><span class="sxs-lookup"><span data-stu-id="7c5b7-115">The display of the dialog box requesting the user to enter the product identifier can then be made conditional upon the presence of the [**ProductID**](productid.md) property, which is set when the **PIDKEY** property is validated.</span></span>

 

 



