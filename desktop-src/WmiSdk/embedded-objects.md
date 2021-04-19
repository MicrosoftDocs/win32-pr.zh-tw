---
description: 内嵌物件是類別的物件，存在於另一個類別的類別或實例宣告內。
ms.assetid: 11a4556b-f682-4850-aedc-793602c5745b
ms.tgt_platform: multiple
title: 在類別中內嵌物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b94296a6869dddca7fd3df08739615a4a0c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979965"
---
# <a name="embedding-objects-in-a-class"></a><span data-ttu-id="c575c-103">在類別中內嵌物件</span><span class="sxs-lookup"><span data-stu-id="c575c-103">Embedding Objects in a Class</span></span>

<span data-ttu-id="c575c-104">内嵌物件是類別的物件，存在於另一個類別的類別或實例宣告內。</span><span class="sxs-lookup"><span data-stu-id="c575c-104">An embedded object is an object of a class that exists within a class or instance declaration of another class.</span></span> <span data-ttu-id="c575c-105">例如， [**win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別包含 [**win32 \_ 受信任**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) 的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="c575c-105">For example, the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class contains [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) embedded objects.</span></span> <span data-ttu-id="c575c-106">每個 **win32 \_ 信任** 物件都包含一個 [**win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 物件。</span><span class="sxs-lookup"><span data-stu-id="c575c-106">Each of the **Win32\_Trustee** objects contains a [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) object.</span></span> <span data-ttu-id="c575c-107">WMI 不會限制類別可以有内嵌物件的深度。</span><span class="sxs-lookup"><span data-stu-id="c575c-107">WMI does not limit the depth to which a class can have embedded objects.</span></span> <span data-ttu-id="c575c-108">不過，使用另一個設計（例如建立關聯類別）可能會讓架構更容易管理。</span><span class="sxs-lookup"><span data-stu-id="c575c-108">However, using another design, such as creating an association class, may make a more manageable schema.</span></span>

<span data-ttu-id="c575c-109">如需有關内嵌物件的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="c575c-109">For more information about embedded objects, see the following topics:</span></span>

-   [<span data-ttu-id="c575c-110">建立内嵌物件</span><span class="sxs-lookup"><span data-stu-id="c575c-110">Creating Embedded Objects</span></span>](creating-embedded-objects.md)
-   [<span data-ttu-id="c575c-111">查詢内嵌物件</span><span class="sxs-lookup"><span data-stu-id="c575c-111">Querying Embedded Objects</span></span>](querying-embedded-objects.md)

## <a name="related-topics"></a><span data-ttu-id="c575c-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="c575c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c575c-113">設計受控物件格式 (MOF) 類別</span><span class="sxs-lookup"><span data-stu-id="c575c-113">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
