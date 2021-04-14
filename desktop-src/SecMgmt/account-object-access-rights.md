---
description: 帳戶物件存取權限類型具有下列存取類型。
ms.assetid: 42fb22bb-8135-4a8f-bce6-e767d6c5aaea
title: 帳戶物件存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d69ba0939286564517c7293da136e88aa0367a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513760"
---
# <a name="account-object-access-rights"></a><span data-ttu-id="c555b-103">帳戶物件存取權限</span><span class="sxs-lookup"><span data-stu-id="c555b-103">Account Object Access Rights</span></span>

<span data-ttu-id="c555b-104">帳戶物件存取權限類型具有下列存取類型。</span><span class="sxs-lookup"><span data-stu-id="c555b-104">The Account Object Access Rights type has the following access types.</span></span>



| <span data-ttu-id="c555b-105">存取類型</span><span class="sxs-lookup"><span data-stu-id="c555b-105">Access type</span></span>                     | <span data-ttu-id="c555b-106">Description</span><span class="sxs-lookup"><span data-stu-id="c555b-106">Description</span></span>                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c555b-107">帳戶 \_ 視圖</span><span class="sxs-lookup"><span data-stu-id="c555b-107">ACCOUNT\_VIEW</span></span>                   | <span data-ttu-id="c555b-108">需要此存取類型才能讀取帳戶資訊。</span><span class="sxs-lookup"><span data-stu-id="c555b-108">This access type is required to read the account information.</span></span> <span data-ttu-id="c555b-109">這包括指派給帳戶的 [*許可權*](/windows/desktop/SecGloss/p-gly) 、指派的記憶體配額，以及授與的任何特殊存取類型。</span><span class="sxs-lookup"><span data-stu-id="c555b-109">This includes the [*privileges*](/windows/desktop/SecGloss/p-gly) assigned to the account, memory quotas assigned, and any special access types granted.</span></span> |
| <span data-ttu-id="c555b-110">帳戶 \_ 調整 \_ 許可權</span><span class="sxs-lookup"><span data-stu-id="c555b-110">ACCOUNT\_ADJUST\_PRIVILEGES</span></span>     | <span data-ttu-id="c555b-111">需要有此存取類型，才能將許可權指派給帳戶或從中移除許可權。</span><span class="sxs-lookup"><span data-stu-id="c555b-111">This access type is required to assign privileges to or remove privileges from an account.</span></span>                                                                                                                                                            |
| <span data-ttu-id="c555b-112">帳戶 \_ 調整 \_ 配額</span><span class="sxs-lookup"><span data-stu-id="c555b-112">ACCOUNT\_ADJUST\_QUOTAS</span></span>         | <span data-ttu-id="c555b-113">變更指派給帳戶的系統配額需要此存取類型。</span><span class="sxs-lookup"><span data-stu-id="c555b-113">This access type is required to change the system quotas assigned to an account.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="c555b-114">帳戶 \_ 調整 \_ 系統 \_ 存取</span><span class="sxs-lookup"><span data-stu-id="c555b-114">ACCOUNT\_ADJUST\_SYSTEM\_ACCESS</span></span> | <span data-ttu-id="c555b-115">需要此存取類型才能更新帳戶的系統存取旗標。</span><span class="sxs-lookup"><span data-stu-id="c555b-115">This access type is required to update the system access flags for the account.</span></span>                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a><span data-ttu-id="c555b-116">一般存取遮罩</span><span class="sxs-lookup"><span data-stu-id="c555b-116">Generic Access Masks</span></span>

<span data-ttu-id="c555b-117">[**Account**](account-object.md)物件會將下列從一般存取類型的對應發行至特定的存取類型。</span><span class="sxs-lookup"><span data-stu-id="c555b-117">The [**Account**](account-object.md) object publishes the following mappings from generic access types to specific access types.</span></span>

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                        ACCOUNT_VIEW 
            
    GENERIC_WRITE       STANDARD_RIGHTS_WRITE |
                        ACCOUNT_ADJUST_PRIVILEGES |
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS

    GENERIC_EXECUTE        STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a><span data-ttu-id="c555b-118">標準存取類型</span><span class="sxs-lookup"><span data-stu-id="c555b-118">Standard Access Types</span></span>

<span data-ttu-id="c555b-119">此物件不支援 (選擇性) 同步處理標準存取類型。</span><span class="sxs-lookup"><span data-stu-id="c555b-119">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="c555b-120">支援所有必要的存取類型。</span><span class="sxs-lookup"><span data-stu-id="c555b-120">All required access types are supported.</span></span> <span data-ttu-id="c555b-121">此物件類型所有支援之存取類型的遮罩如下所示。</span><span class="sxs-lookup"><span data-stu-id="c555b-121">The mask of all supported access types for this object type is as follows.</span></span>

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
