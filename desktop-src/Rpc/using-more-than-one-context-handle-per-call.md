---
title: 每次呼叫使用一個以上的內容控制碼
description: 在 Windows Vista 和更新版本的作業系統中，可以使用內容控制碼陣列做為參數的能力。
ms.assetid: 84f3036b-ff4d-485d-bf23-ad10a03076a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7b1c69dd182bee8f68e7068bcfcef60efd380a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840019"
---
# <a name="using-more-than-one-context-handle-per-call"></a><span data-ttu-id="cd638-103">每次呼叫使用一個以上的內容控制碼</span><span class="sxs-lookup"><span data-stu-id="cd638-103">Using More than One Context Handle per Call</span></span>

<span data-ttu-id="cd638-104">在 Windows Vista 和更新版本的作業系統中，可以使用內容控制碼陣列做為參數的能力。</span><span class="sxs-lookup"><span data-stu-id="cd638-104">The ability to use arrays of context handles as parameters is made available in Windows Vista and later operating systems.</span></span> <span data-ttu-id="cd638-105">不過，在應用程式中應該謹慎使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="cd638-105">However, this feature should be used carefully within an application.</span></span> <span data-ttu-id="cd638-106">例如，在多個呼叫中使用內容控制碼的情況下，會越來越難以追蹤其用途。</span><span class="sxs-lookup"><span data-stu-id="cd638-106">For example, in a situation where a context handle is being used in multiple calls it becomes increasingly difficult to keep track of its use.</span></span>

 

 




