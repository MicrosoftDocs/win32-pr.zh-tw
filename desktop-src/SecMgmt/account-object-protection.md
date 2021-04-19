---
description: 說明如何保護帳戶物件。
ms.assetid: a07ef46e-f4b6-4e21-bdd7-72d03e1c88b3
title: 帳戶物件保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f495a3dc943ef73eef5074e0edc73247ceb02d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997847"
---
# <a name="account-object-protection"></a><span data-ttu-id="1d288-103">帳戶物件保護</span><span class="sxs-lookup"><span data-stu-id="1d288-103">Account Object Protection</span></span>

<span data-ttu-id="1d288-104">[**帳戶**](account-object.md) 物件會以下列方式受到保護：</span><span class="sxs-lookup"><span data-stu-id="1d288-104">[**Account**](account-object.md) objects are protected in the following fashion:</span></span>

-   <span data-ttu-id="1d288-105">群組 **世界** 具有一般 \_ 執行。</span><span class="sxs-lookup"><span data-stu-id="1d288-105">The group **WORLD** has GENERIC\_EXECUTE.</span></span>
-   <span data-ttu-id="1d288-106">群組 **本機系統 \_ 管理員** 具有 DELETE、GENERIC \_ READ、generic \_ WRITE、generic \_ EXECUTE 和 WRITE \_ DACL 存取權。</span><span class="sxs-lookup"><span data-stu-id="1d288-106">The group **LOCAL\_ADMIN** has DELETE, GENERIC\_READ, GENERIC\_WRITE, GENERIC\_EXECUTE, and WRITE\_DACL access.</span></span>
-   <span data-ttu-id="1d288-107">群組 **本機系統 \_ 管理員** 會被指派為帳戶物件的擁有者和主要群組。</span><span class="sxs-lookup"><span data-stu-id="1d288-107">The group **LOCAL\_ADMIN** is assigned as owner and primary group of Account objects.</span></span>

 

 



