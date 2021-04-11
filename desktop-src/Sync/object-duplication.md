---
description: DuplicateHandle 函式會建立一個重複的控制碼，以供另一個指定的進程使用。
ms.assetid: b79d2b8f-931e-4cab-9bbe-9ead1b102132
title: 物件重複
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f8e0948ce55f5d25d7567346ecdec97f04b24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027082"
---
# <a name="object-duplication"></a><span data-ttu-id="887a1-103">物件重複</span><span class="sxs-lookup"><span data-stu-id="887a1-103">Object Duplication</span></span>

<span data-ttu-id="887a1-104">[**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)函式會建立一個重複的控制碼，以供另一個指定的進程使用。</span><span class="sxs-lookup"><span data-stu-id="887a1-104">The [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function creates a duplicate handle that can be used by another specified process.</span></span> <span data-ttu-id="887a1-105">這個共用物件控制碼的方法比使用命名物件或繼承更為複雜。</span><span class="sxs-lookup"><span data-stu-id="887a1-105">This method of sharing object handles is more complex than using named objects or inheritance.</span></span> <span data-ttu-id="887a1-106">它需要建立進程和控制碼重複的進程之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="887a1-106">It requires communication between the creating process and the process into which the handle is duplicated.</span></span> <span data-ttu-id="887a1-107"> (控制碼值和處理序識別碼) 所需的資訊，可由任何進程間的通訊方法（例如具名管道或命名的共用記憶體）進行通訊。</span><span class="sxs-lookup"><span data-stu-id="887a1-107">The necessary information (the handle value and process identifier) can be communicated by any of the interprocess communication methods, such as named pipes or named shared memory.</span></span>

 

 
