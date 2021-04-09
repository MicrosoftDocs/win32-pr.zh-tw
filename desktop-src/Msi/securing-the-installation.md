---
description: 將 CustomUserAccounts 資料表中的所有密碼屬性加入至屬性工作表中的 MsiHiddenProperties 屬性。
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: 保護安裝的安全
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add5211327508dbbf6531c48c3d2ae40f095375d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945416"
---
# <a name="securing-the-installation"></a><span data-ttu-id="e1e6c-103">保護安裝的安全</span><span class="sxs-lookup"><span data-stu-id="e1e6c-103">Securing the Installation</span></span>

<span data-ttu-id="e1e6c-104">將 CustomUserAccounts 資料表中的所有密碼屬性加入至 [屬性工作表](property-table.md)中的 [**MsiHiddenProperties**](msihiddenproperties.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="e1e6c-104">Add all of the Password properties from the CustomUserAccounts table to the [**MsiHiddenProperties**](msihiddenproperties.md) property in the [Property table](property-table.md).</span></span> <span data-ttu-id="e1e6c-105">將延遲自訂動作的名稱也加入至 **MsiHiddenProperties** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e1e6c-105">Add the names of the deferred custom actions to the **MsiHiddenProperties** property as well.</span></span> <span data-ttu-id="e1e6c-106">這可防止安裝程式將機密屬性值寫入 () 到記錄檔中的密碼，並確保當延遲的自訂動作使用這些值做為 CustomActionData 屬性時，不會記錄這些值。</span><span class="sxs-lookup"><span data-stu-id="e1e6c-106">This will prevent the installer from writing the sensitive property values (the passwords) into the log and will ensure these values are not logged when the deferred custom actions use the values as the CustomActionData property.</span></span>

<span data-ttu-id="e1e6c-107">若要讓使用者的密碼可在 Windows Installer 服務中使用，必須將 password 屬性新增至 [**SecureCustomProperties**](securecustomproperties.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="e1e6c-107">For the user's password to be available in the Windows Installer service, the password property must be added to the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

[<span data-ttu-id="e1e6c-108">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="e1e6c-108">Property Table</span></span>](property-table.md)



| <span data-ttu-id="e1e6c-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e1e6c-109">Property</span></span>                                                 | <span data-ttu-id="e1e6c-110">值</span><span class="sxs-lookup"><span data-stu-id="e1e6c-110">Value</span></span>                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="e1e6c-111">**MsiHiddenProperties**</span><span class="sxs-lookup"><span data-stu-id="e1e6c-111">**MsiHiddenProperties**</span></span>](msihiddenproperties.md)       | <span data-ttu-id="e1e6c-112">TESTUSERPASSWORD;CreateAccount;RemoveAccount;RollbackAccount</span><span class="sxs-lookup"><span data-stu-id="e1e6c-112">TESTUSERPASSWORD;CreateAccount;RemoveAccount;RollbackAccount</span></span> |
| [<span data-ttu-id="e1e6c-113">**SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="e1e6c-113">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="e1e6c-114">TESTUSERPASSWORD</span><span class="sxs-lookup"><span data-stu-id="e1e6c-114">TESTUSERPASSWORD</span></span>                                             |



 

<span data-ttu-id="e1e6c-115">這會結束範例。</span><span class="sxs-lookup"><span data-stu-id="e1e6c-115">This concludes the sample.</span></span>

 

 



