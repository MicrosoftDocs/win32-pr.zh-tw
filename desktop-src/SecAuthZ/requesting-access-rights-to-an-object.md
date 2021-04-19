---
description: 當您開啟物件的控制碼時，傳回的控制碼會有物件的存取權限組合。
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: 要求存取物件的存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb2e13bd5f5e51ed194b60c6ab63d1eda8eddfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970644"
---
# <a name="requesting-access-rights-to-an-object"></a><span data-ttu-id="40ba5-103">要求存取物件的存取權限</span><span class="sxs-lookup"><span data-stu-id="40ba5-103">Requesting Access Rights to an Object</span></span>

<span data-ttu-id="40ba5-104">當您開啟物件的控制碼時，傳回的控制碼會有物件的存取權限組合。</span><span class="sxs-lookup"><span data-stu-id="40ba5-104">When you open a handle to an object, the returned handle has some combination of access rights to the object.</span></span> <span data-ttu-id="40ba5-105">某些功能（例如 [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea)）不需要一組特定的要求存取權限。</span><span class="sxs-lookup"><span data-stu-id="40ba5-105">Some functions, such as [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), do not require a specific set of requested access rights.</span></span> <span data-ttu-id="40ba5-106">這些函式一律會嘗試開啟控制碼來取得完整存取權。</span><span class="sxs-lookup"><span data-stu-id="40ba5-106">These functions always try to open the handle for full access.</span></span> <span data-ttu-id="40ba5-107">其他功能（例如 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 和 [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess)）可讓您指定所需的存取權限集。</span><span class="sxs-lookup"><span data-stu-id="40ba5-107">Other functions, such as [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) and [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), allow you to specify the set of access rights that you want.</span></span> <span data-ttu-id="40ba5-108">您只應要求所需的存取權限，而不是開啟完整存取的控制碼。</span><span class="sxs-lookup"><span data-stu-id="40ba5-108">You should request only the access rights that you need, rather than opening a handle for full access.</span></span> <span data-ttu-id="40ba5-109">這可防止以非預期的方式使用控制碼，而且如果物件的 DACL 只允許有限存取，則會提高存取要求成功的機率。</span><span class="sxs-lookup"><span data-stu-id="40ba5-109">This prevents using the handle in an unintended way, and increases the chances that the access request will succeed if the object's DACL only allows limited access.</span></span>

<span data-ttu-id="40ba5-110">使用 [一般存取權限](generic-access-rights.md) 來指定開啟物件的控制碼時所需的存取類型。</span><span class="sxs-lookup"><span data-stu-id="40ba5-110">Use [generic access rights](generic-access-rights.md) to specify the type of access needed when opening a handle to an object.</span></span> <span data-ttu-id="40ba5-111">這通常比指定所有對應的標準和特定許可權來得簡單。</span><span class="sxs-lookup"><span data-stu-id="40ba5-111">This is typically simpler than specifying all the corresponding standard and specific rights.</span></span> <span data-ttu-id="40ba5-112">或者，使用允許的最大常數，要求以對 \_ 呼叫端有效的所有存取權限開啟物件。</span><span class="sxs-lookup"><span data-stu-id="40ba5-112">Alternatively, use the MAXIMUM\_ALLOWED constant to request that the object be opened with all the access rights that are valid for the caller.</span></span>

> [!Note]  
> <span data-ttu-id="40ba5-113">最大 \_ 允許的常數不能用在 ACE 中。</span><span class="sxs-lookup"><span data-stu-id="40ba5-113">The MAXIMUM\_ALLOWED constant cannot be used in an ACE.</span></span>

 

<span data-ttu-id="40ba5-114">若要取得或設定物件 [*安全描述項*](/windows/desktop/SecGloss/s-gly)中的 SACL，請在開啟物件的控制碼時，要求 [存取 \_ 系統 \_ 安全性訪問](sacl-access-right.md) 許可權。</span><span class="sxs-lookup"><span data-stu-id="40ba5-114">To get or set the SACL in an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly), request the [ACCESS\_SYSTEM\_SECURITY access right](sacl-access-right.md) when opening a handle to the object.</span></span>

 

 
