---
description: 由於有兩個主要原因，系統會使用物件和控制碼來管制系統資源的存取權。
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: 關於控制碼和物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7474c11298166cc8d63032c6e1d8f84e6db249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944349"
---
# <a name="about-handles-and-objects"></a><span data-ttu-id="64d72-103">關於控制碼和物件</span><span class="sxs-lookup"><span data-stu-id="64d72-103">About Handles and Objects</span></span>

<span data-ttu-id="64d72-104">由於有兩個主要原因，系統會使用物件和控制碼來管制系統資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="64d72-104">The system uses objects and handles to regulate access to system resources for two main reasons.</span></span> <span data-ttu-id="64d72-105">首先，使用物件可確保只要維持原始物件介面，Microsoft 就能更新系統功能。</span><span class="sxs-lookup"><span data-stu-id="64d72-105">First, the use of objects ensures that Microsoft can update system functionality, as long as the original object interface is maintained.</span></span> <span data-ttu-id="64d72-106">當系統的後續版本發行時，您可以使用已更新的物件，幾乎不需要額外的工作。</span><span class="sxs-lookup"><span data-stu-id="64d72-106">When subsequent versions of the system are released, you can use the updated object with little or no additional work.</span></span>

<span data-ttu-id="64d72-107">其次，使用物件可以讓您利用 Windows 安全性。</span><span class="sxs-lookup"><span data-stu-id="64d72-107">Secondly, the use of objects enables you to take advantage of Windows security.</span></span> <span data-ttu-id="64d72-108">每個物件都有自己的存取控制清單 (ACL) ，可指定進程可以在物件上執行的動作。</span><span class="sxs-lookup"><span data-stu-id="64d72-108">Each object has its own access-control list (ACL) that specifies the actions a process can perform on the object.</span></span> <span data-ttu-id="64d72-109">系統會在每次應用程式建立物件的控制碼時，檢查物件的 ACL。</span><span class="sxs-lookup"><span data-stu-id="64d72-109">The system examines an object's ACL each time an application creates a handle to the object.</span></span> <span data-ttu-id="64d72-110">如需詳細資訊，請參閱[存取控制](/windows/desktop/SecAuthZ/access-control)。</span><span class="sxs-lookup"><span data-stu-id="64d72-110">For more information, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

-   [<span data-ttu-id="64d72-111">物件管理員</span><span class="sxs-lookup"><span data-stu-id="64d72-111">Object Manager</span></span>](object-manager.md)
-   [<span data-ttu-id="64d72-112">物件介面</span><span class="sxs-lookup"><span data-stu-id="64d72-112">Object Interface</span></span>](object-interface.md)
-   [<span data-ttu-id="64d72-113">物件命名空間</span><span class="sxs-lookup"><span data-stu-id="64d72-113">Object Namespaces</span></span>](/windows/desktop/Sync/object-namespaces)
-   [<span data-ttu-id="64d72-114">控制碼限制</span><span class="sxs-lookup"><span data-stu-id="64d72-114">Handle Limitations</span></span>](handle-limitations.md)
-   [<span data-ttu-id="64d72-115">處理繼承</span><span class="sxs-lookup"><span data-stu-id="64d72-115">Handle Inheritance</span></span>](handle-inheritance.md)

 

 
