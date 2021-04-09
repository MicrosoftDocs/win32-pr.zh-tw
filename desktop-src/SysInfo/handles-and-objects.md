---
description: 物件是代表系統資源的資料結構，例如檔案、執行緒或圖形影像。
ms.assetid: 26aaad09-c1e1-46e8-9cd3-7d795a10d900
title: 控制碼和物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b5a35d55571a01f2f186f4e756401582474949f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852051"
---
# <a name="handles-and-objects"></a><span data-ttu-id="ff65f-103">控制碼和物件</span><span class="sxs-lookup"><span data-stu-id="ff65f-103">Handles and Objects</span></span>

<span data-ttu-id="ff65f-104">*物件* 是代表系統資源的資料結構，例如檔案、執行緒或圖形影像。</span><span class="sxs-lookup"><span data-stu-id="ff65f-104">An *object* is a data structure that represents a system resource, such as a file, thread, or graphic image.</span></span> <span data-ttu-id="ff65f-105">應用程式無法直接存取物件資料或物件所代表的系統資源。</span><span class="sxs-lookup"><span data-stu-id="ff65f-105">An application cannot directly access object data or the system resource that an object represents.</span></span> <span data-ttu-id="ff65f-106">相反地，應用程式必須取得物件 *控制碼*，它可以用來檢查或修改系統資源。</span><span class="sxs-lookup"><span data-stu-id="ff65f-106">Instead, an application must obtain an object *handle*, which it can use to examine or modify the system resource.</span></span> <span data-ttu-id="ff65f-107">每個控制碼在內部維護的資料表中都有一個專案。</span><span class="sxs-lookup"><span data-stu-id="ff65f-107">Each handle has an entry in an internally maintained table.</span></span> <span data-ttu-id="ff65f-108">這些專案包含資源的位址，以及用來識別資源類型的方法。</span><span class="sxs-lookup"><span data-stu-id="ff65f-108">These entries contain the addresses of the resources and the means to identify the resource type.</span></span>

-   [<span data-ttu-id="ff65f-109">關於控制碼和物件</span><span class="sxs-lookup"><span data-stu-id="ff65f-109">About Handles and Objects</span></span>](about-handles-and-objects.md)
-   [<span data-ttu-id="ff65f-110">物件類別</span><span class="sxs-lookup"><span data-stu-id="ff65f-110">Object Categories</span></span>](object-categories.md)
-   [<span data-ttu-id="ff65f-111">控制碼和物件參考</span><span class="sxs-lookup"><span data-stu-id="ff65f-111">Handle and Object Reference</span></span>](handle-and-object-reference.md)

 

 



