---
description: 產品代碼是 GUID，也就是應用程式或產品的主體識別。
ms.assetid: 6fbad59b-27b7-4ac1-bad5-8a608c7b270f
title: 產品代碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edca03d54dcd14068e89b2314b729e672b0c631c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194212"
---
# <a name="product-codes"></a><span data-ttu-id="2046c-103">產品代碼</span><span class="sxs-lookup"><span data-stu-id="2046c-103">Product Codes</span></span>

<span data-ttu-id="2046c-104">產品代碼是 GUID，也就是應用程式或產品的主體識別。</span><span class="sxs-lookup"><span data-stu-id="2046c-104">The product code is a GUID that is the principal identification of an application or product.</span></span> <span data-ttu-id="2046c-105">如需詳細資訊，請參閱 [ [**ProductCode**](productcode.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="2046c-105">For more information, see the [**ProductCode**](productcode.md) property.</span></span> <span data-ttu-id="2046c-106">如果對產品進行重大變更，則產品代碼也應該變更以反映這一點。</span><span class="sxs-lookup"><span data-stu-id="2046c-106">If significant changes are made to a product then the product code should also be changed to reflect this.</span></span> <span data-ttu-id="2046c-107">但是，如果產品的變更相對較小，則不需要變更產品程式碼。</span><span class="sxs-lookup"><span data-stu-id="2046c-107">It is not however a requirement that the product code be changed if the changes to the product are relatively minor.</span></span>

<span data-ttu-id="2046c-108">應用程式套件的32位和64位版本必須有不同的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="2046c-108">The 32-bit and 64-bit versions of an application's package must have different product codes.</span></span> <span data-ttu-id="2046c-109">如果應用程式的任何32位元件重新編譯成64位元件，則必須指派新的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="2046c-109">If any 32-bit component of an application is recompiled into a 64-bit component, a new product code must be assigned.</span></span>

<span data-ttu-id="2046c-110">如果 [PublishComponent 資料表](publishcomponent-table.md) 中公開的伺服器是從32位重新編譯為64位，則可能也需要變更此資料表中的 GUID，讓32位和64位用戶端可以識別適當的限定元件類別。</span><span class="sxs-lookup"><span data-stu-id="2046c-110">If a server exposed in the [PublishComponent Table](publishcomponent-table.md) is recompiled from 32-bits to 64-bits, the GUID in this table may also need to be changed so that 32-bit and 64-bit clients can identify the appropriate qualified component category.</span></span> <span data-ttu-id="2046c-111">在此情況下，產品代碼也必須變更。</span><span class="sxs-lookup"><span data-stu-id="2046c-111">In this case, the product code must also be changed.</span></span>

<span data-ttu-id="2046c-112">請注意，產品程式碼 Guid 中的字母必須為大寫。</span><span class="sxs-lookup"><span data-stu-id="2046c-112">Note that letters in product code GUIDs must be uppercase.</span></span> <span data-ttu-id="2046c-113">GUIDGEN 之類的公用程式會產生包含小寫字母的 Guid。</span><span class="sxs-lookup"><span data-stu-id="2046c-113">Utilities such as GUIDGEN generate GUIDs containing lowercase letters.</span></span> <span data-ttu-id="2046c-114">這些 Guid 中的小寫字母必須變更為大寫，才能當做產品代碼或封裝程式碼使用。</span><span class="sxs-lookup"><span data-stu-id="2046c-114">The lowercase letters in these GUIDs must be changed to uppercase to be used as a product code or package code.</span></span> <span data-ttu-id="2046c-115">如需詳細資訊，請參閱 [變更產品代碼](changing-the-product-code.md)。</span><span class="sxs-lookup"><span data-stu-id="2046c-115">For more information, see [Changing the Product Code](changing-the-product-code.md).</span></span>

<span data-ttu-id="2046c-116">封裝程式碼是識別特定 Windows Installer [*套件*](p-gly.md)的 GUID。</span><span class="sxs-lookup"><span data-stu-id="2046c-116">The package code is a GUID identifying a particular Windows Installer [*package*](p-gly.md).</span></span> <span data-ttu-id="2046c-117">封裝程式碼會將 .msi 檔案與應用程式或產品產生關聯，也可以用於驗證來源。</span><span class="sxs-lookup"><span data-stu-id="2046c-117">The package code associates an .msi file with an application or product and can also be used for the verification of sources.</span></span> <span data-ttu-id="2046c-118">產品和套件代碼不可互換。</span><span class="sxs-lookup"><span data-stu-id="2046c-118">The product and package codes are not interchangeable.</span></span> <span data-ttu-id="2046c-119">沒有兩個 nonidentical .msi 檔案應該要有相同的套件程式碼。</span><span class="sxs-lookup"><span data-stu-id="2046c-119">No two nonidentical .msi files should ever have the same package code.</span></span> <span data-ttu-id="2046c-120">雖然傳送具有相同封裝程式碼和產品程式碼的應用程式很常見，但在更新應用程式時，這兩個值可能會分離出來。</span><span class="sxs-lookup"><span data-stu-id="2046c-120">Although it is common to ship an application that has the same package code and product code, the two values can diverge as the application is updated.</span></span> <span data-ttu-id="2046c-121">如需詳細資訊，請參閱 [封裝程式碼](package-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="2046c-121">For more information, see [Package Codes](package-codes.md).</span></span>

 

 



