---
description: 安全物件使用存取遮罩格式，其中四個高序位位會指定一般存取權限。
ms.assetid: e18cede9-9bf7-4866-850b-5d7fa43a5b0f
title: 一般存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff14aa259222bc37096b8a94f30cffb5ab0876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694140"
---
# <a name="generic-access-rights"></a><span data-ttu-id="7700d-103">一般存取權限</span><span class="sxs-lookup"><span data-stu-id="7700d-103">Generic Access Rights</span></span>

<span data-ttu-id="7700d-104">安全物件使用 [存取遮罩格式](access-mask-format.md) ，其中四個高序位位會指定一般存取權限。</span><span class="sxs-lookup"><span data-stu-id="7700d-104">Securable objects use an [access mask format](access-mask-format.md) in which the four high-order bits specify generic access rights.</span></span> <span data-ttu-id="7700d-105">每一種安全物件類型都會將這些位對應到一組其標準和物件特定的存取權限。</span><span class="sxs-lookup"><span data-stu-id="7700d-105">Each type of securable object maps these bits to a set of its standard and object-specific access rights.</span></span> <span data-ttu-id="7700d-106">例如，Windows 檔案物件會將一般 \_ 讀取位對應到讀取 \_ 控制項，並同步處理標準存取權限和檔案讀取 \_ \_ 資料、檔案 \_ 讀取 \_ EA 和檔案 \_ 讀取 \_ 屬性物件特定存取權限。</span><span class="sxs-lookup"><span data-stu-id="7700d-106">For example, a Windows file object maps the GENERIC\_READ bit to the READ\_CONTROL and SYNCHRONIZE standard access rights and to the FILE\_READ\_DATA, FILE\_READ\_EA, and FILE\_READ\_ATTRIBUTES object-specific access rights.</span></span> <span data-ttu-id="7700d-107">其他類型的物件會將泛型 \_ 讀取位對應至任何一組適用于該類型物件的存取權限。</span><span class="sxs-lookup"><span data-stu-id="7700d-107">Other types of objects map the GENERIC\_READ bit to whatever set of access rights is appropriate for that type of object.</span></span>

<span data-ttu-id="7700d-108">當您開啟物件的控制碼時，您可以使用一般存取權限來指定所需的存取類型。</span><span class="sxs-lookup"><span data-stu-id="7700d-108">You can use generic access rights to specify the type of access you need when you are opening a handle to an object.</span></span> <span data-ttu-id="7700d-109">這通常比指定所有對應的標準和特定許可權來得簡單。</span><span class="sxs-lookup"><span data-stu-id="7700d-109">This is typically simpler than specifying all the corresponding standard and specific rights.</span></span>

<span data-ttu-id="7700d-110">下表顯示針對一般存取權限定義的常數。</span><span class="sxs-lookup"><span data-stu-id="7700d-110">The following table shows the constants defined for the generic access rights.</span></span>



| <span data-ttu-id="7700d-111">常數</span><span class="sxs-lookup"><span data-stu-id="7700d-111">Constant</span></span>         | <span data-ttu-id="7700d-112">泛型意義</span><span class="sxs-lookup"><span data-stu-id="7700d-112">Generic meaning</span></span>            |
|------------------|----------------------------|
| <span data-ttu-id="7700d-113">一般 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="7700d-113">GENERIC\_ALL</span></span>     | <span data-ttu-id="7700d-114">所有可能的存取權限</span><span class="sxs-lookup"><span data-stu-id="7700d-114">All possible access rights</span></span> |
| <span data-ttu-id="7700d-115">一般 \_ 執行</span><span class="sxs-lookup"><span data-stu-id="7700d-115">GENERIC\_EXECUTE</span></span> | <span data-ttu-id="7700d-116">執行存取</span><span class="sxs-lookup"><span data-stu-id="7700d-116">Execute access</span></span>             |
| <span data-ttu-id="7700d-117">一般 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="7700d-117">GENERIC\_READ</span></span>    | <span data-ttu-id="7700d-118">讀取存取權</span><span class="sxs-lookup"><span data-stu-id="7700d-118">Read access</span></span>                |
| <span data-ttu-id="7700d-119">一般 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="7700d-119">GENERIC\_WRITE</span></span>   | <span data-ttu-id="7700d-120">寫入存取權</span><span class="sxs-lookup"><span data-stu-id="7700d-120">Write access</span></span>               |



 

<span data-ttu-id="7700d-121">定義私用安全物件的應用程式也可以使用一般存取權限。</span><span class="sxs-lookup"><span data-stu-id="7700d-121">Applications that define private securable objects can also use the generic access rights.</span></span>

 

 



