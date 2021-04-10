---
description: 物件是由標準標頭和物件特有的屬性所組成。 因為所有物件都有相同的結構，所以 Windows 中會有一個維護所有物件的物件管理員。
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: 物件管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a74581650828a77c6423825d3c557a13075a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944739"
---
# <a name="object-manager"></a><span data-ttu-id="57788-104">物件管理員</span><span class="sxs-lookup"><span data-stu-id="57788-104">Object Manager</span></span>

<span data-ttu-id="57788-105">物件是由標準標頭和物件特有的屬性所組成。</span><span class="sxs-lookup"><span data-stu-id="57788-105">An object consists of a standard header and object-specific attributes.</span></span> <span data-ttu-id="57788-106">因為所有物件都有相同的結構，所以 Windows 中會有一個維護所有物件的物件管理員。</span><span class="sxs-lookup"><span data-stu-id="57788-106">Because all objects have the same structure, there is a single object manager in Windows that maintains all objects.</span></span>

<span data-ttu-id="57788-107">物件標頭包含物件名稱之類的專案，讓其他進程可以依名稱參考物件，並提供安全描述項，讓物件管理員可以控制哪些進程存取系統資源。</span><span class="sxs-lookup"><span data-stu-id="57788-107">The object header includes items such as the object name, so that other processes can reference the object by name, and a security descriptor, so that the object manager can control which processes access the system resource.</span></span>

<span data-ttu-id="57788-108">物件管理員執行的工作包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="57788-108">The tasks that the object manager performs include the following:</span></span>

-   <span data-ttu-id="57788-109">建立物件</span><span class="sxs-lookup"><span data-stu-id="57788-109">Creating objects</span></span>
-   <span data-ttu-id="57788-110">確認處理常式具有使用物件的許可權</span><span class="sxs-lookup"><span data-stu-id="57788-110">Verifying that a process has the right to use the object</span></span>
-   <span data-ttu-id="57788-111">建立物件控制碼，並將其傳回給呼叫者</span><span class="sxs-lookup"><span data-stu-id="57788-111">Creating object handles and returning them to the caller</span></span>
-   <span data-ttu-id="57788-112">維護資源配額</span><span class="sxs-lookup"><span data-stu-id="57788-112">Maintaining resource quotas</span></span>
-   <span data-ttu-id="57788-113">建立重複的控制碼</span><span class="sxs-lookup"><span data-stu-id="57788-113">Creating duplicate handles</span></span>
-   <span data-ttu-id="57788-114">關閉物件的控制碼</span><span class="sxs-lookup"><span data-stu-id="57788-114">Closing handles to objects</span></span>

 

 



