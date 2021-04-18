---
description: Firstrun.cmd 對話方塊序列會收集使用者名稱、公司名稱和產品識別碼資訊。 此安裝程式會在此對話方塊中驗證產品識別碼。
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Firstrun.cmd 對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2024683d7a10395340a18ddd2015b94e1207bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191868"
---
# <a name="firstrun-dialog"></a><span data-ttu-id="11c72-104">Firstrun.cmd 對話方塊</span><span class="sxs-lookup"><span data-stu-id="11c72-104">FirstRun Dialog</span></span>

<span data-ttu-id="11c72-105">Firstrun.cmd 對話方塊序列會收集使用者名稱、公司名稱和產品識別碼資訊。</span><span class="sxs-lookup"><span data-stu-id="11c72-105">A FirstRun dialog box sequence collects user name, company name, and product ID information.</span></span> <span data-ttu-id="11c72-106">此安裝程式會在此對話方塊中驗證產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="11c72-106">The installer verifies the product ID during this dialog.</span></span>

<span data-ttu-id="11c72-107">Firstrun.cmd 對話方塊序列通常不是動作順序的一部分，而是在第一次執行產品時由 [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) 函數呼叫。</span><span class="sxs-lookup"><span data-stu-id="11c72-107">A FirstRun dialog box sequence is usually not a part of the action sequence and is instead called by the [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) function on the first run of the product.</span></span>

<span data-ttu-id="11c72-108">安裝程式套件的作者可能會使用範本對話順序或建立不同的順序。</span><span class="sxs-lookup"><span data-stu-id="11c72-108">An author of an installer package may use the template dialog sequence or create a different sequence.</span></span> <span data-ttu-id="11c72-109">不過，對話順序必須讓使用者設定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="11c72-109">The dialog sequence however needs to have the user set the following properties:</span></span>

-   <span data-ttu-id="11c72-110">[**USERNAME**](username.md) 屬性</span><span class="sxs-lookup"><span data-stu-id="11c72-110">[**USERNAME**](username.md) property</span></span>
-   <span data-ttu-id="11c72-111">[**公司名稱**](companyname.md) 屬性</span><span class="sxs-lookup"><span data-stu-id="11c72-111">[**COMPANYNAME**](companyname.md) property</span></span>
-   <span data-ttu-id="11c72-112">[**PIDKEY**](pidkey.md) 屬性</span><span class="sxs-lookup"><span data-stu-id="11c72-112">[**PIDKEY**](pidkey.md) property</span></span>

<span data-ttu-id="11c72-113">在使用 [ValidateProductID 動作](validateproductid-action.md) 或 [ValidateProductID ControlEvent](validateproductid-controlevent.md)的對話期間，將會驗證產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="11c72-113">The product ID will be validated during the dialog using the [ValidateProductID action](validateproductid-action.md) or the [ValidateProductID ControlEvent](validateproductid-controlevent.md).</span></span>

<span data-ttu-id="11c72-114">如果在命令列上或透過轉換將產品識別碼設定為屬性，則必須讓使用者在第一次執行對話時重新輸入產品識別碼，才能使用 [**ProductID**](productid.md) 屬性來控制顯示。</span><span class="sxs-lookup"><span data-stu-id="11c72-114">If the product ID is set as a property on the command line, or by a transform, then the necessity of having the user reenter the product ID during the first-run dialog can be circumvented by controlling the display using the [**ProductID**](productid.md) property.</span></span> <span data-ttu-id="11c72-115">成功驗證產品識別碼之後， **ProductID** 屬性會設定為完整的有效產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="11c72-115">Following the successful validation of the product ID the **ProductID** property is set to the full, valid product ID.</span></span>

 

 



