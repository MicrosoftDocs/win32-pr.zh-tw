---
description: 當您建立安全物件時，可以將安全描述項指派給新的物件。
ms.assetid: 5b276d27-31a4-4a83-83b0-c4044a427097
title: 新物件的安全描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3f9af674c83e4fc42448635bc54dfc0bb51b42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983329"
---
# <a name="security-descriptors-for-new-objects"></a><span data-ttu-id="7bb24-103">新物件的安全描述項</span><span class="sxs-lookup"><span data-stu-id="7bb24-103">Security Descriptors for New Objects</span></span>

<span data-ttu-id="7bb24-104">當您建立安全物件時，可以將 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 指派給新的物件。</span><span class="sxs-lookup"><span data-stu-id="7bb24-104">When you create a securable object, you can assign a [*security descriptor*](/windows/desktop/SecGloss/s-gly) to the new object.</span></span> <span data-ttu-id="7bb24-105">建立安全物件（例如 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 或 [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)）的函式有一個參數，指向可包含新物件安全描述項之指標的 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="7bb24-105">The functions for creating securable objects, such as [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) or [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa), have a parameter that points to the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure that can contain a pointer to the new object's security descriptor.</span></span> <span data-ttu-id="7bb24-106">如需建立安全描述項的範例程式碼，然後呼叫 **RegCreateKeyEx** 將安全描述項指派給新的登錄機碼，請參閱 [在 c + + 中建立新物件的安全描述項](creating-a-security-descriptor-for-a-new-object-in-c--.md)。</span><span class="sxs-lookup"><span data-stu-id="7bb24-106">For sample code that builds a security descriptor and then calls **RegCreateKeyEx** to assign the security descriptor to a new registry key, see [Creating a Security Descriptor for a New Object in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).</span></span>

<span data-ttu-id="7bb24-107">管理物件的系統元件或伺服器可以儲存指定的或預設安全描述項，使其成為物件的持續性屬性。</span><span class="sxs-lookup"><span data-stu-id="7bb24-107">The system component or server that manages the object can store the specified or default security descriptor to make it a persistent attribute of the object.</span></span> <span data-ttu-id="7bb24-108">如果物件的建立者未指定安全描述項，系統會使用繼承的或預設的安全性資訊來建立安全描述項。</span><span class="sxs-lookup"><span data-stu-id="7bb24-108">If an object's creator does not specify a security descriptor, the system uses inherited or default security information to create a security descriptor.</span></span> <span data-ttu-id="7bb24-109">您可以使用函數來變更物件安全描述項中的資訊。</span><span class="sxs-lookup"><span data-stu-id="7bb24-109">You can use functions to change the information in an object's security descriptor.</span></span>

<span data-ttu-id="7bb24-110">目錄服務物件、檔案、目錄、登錄機碼和桌上型電腦是可以有父物件的安全物件。</span><span class="sxs-lookup"><span data-stu-id="7bb24-110">Directory service objects, files, directories, registry keys, and desktops are securable objects that can have a parent object.</span></span> <span data-ttu-id="7bb24-111">當您建立這些物件的其中一個時，系統會檢查父物件之安全描述項中的可繼承 Ace。</span><span class="sxs-lookup"><span data-stu-id="7bb24-111">When you create one of these objects, the system checks for inheritable ACEs in the security descriptor of the parent object.</span></span> <span data-ttu-id="7bb24-112">系統通常會將任何可繼承的 Ace 合併到新物件安全描述項的 Acl 中。</span><span class="sxs-lookup"><span data-stu-id="7bb24-112">The system typically merges any inheritable ACEs into the ACLs of the new object's security descriptor.</span></span> <span data-ttu-id="7bb24-113">您可以藉由在 \_ \_ \_ \_ 安全描述項的控制位中設定 SE dacl protected 或 se 受保護的位，來防止 DACL 或 SACL 繼承 ace。</span><span class="sxs-lookup"><span data-stu-id="7bb24-113">You can prevent a DACL or SACL from inheriting ACEs by setting the SE\_DACL\_PROTECTED or SE\_SACL\_PROTECTED bits in the security descriptor's control bits.</span></span> <span data-ttu-id="7bb24-114">如需詳細資訊，請參閱 [ACE 繼承](ace-inheritance.md)。</span><span class="sxs-lookup"><span data-stu-id="7bb24-114">For more information, see [ACE inheritance](ace-inheritance.md).</span></span>

 

 
