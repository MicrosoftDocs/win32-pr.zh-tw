---
description: 列出並說明私用資料物件的存取權限。
ms.assetid: 82be57d0-487c-4eb7-83d5-0dd2d53a452b
title: 私用資料物件存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142aecfe133a9c04237aacf58413e026c4cb3164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468876"
---
# <a name="private-data-object-access-rights"></a><span data-ttu-id="9b374-103">私用資料物件存取權限</span><span class="sxs-lookup"><span data-stu-id="9b374-103">Private Data Object Access Rights</span></span>

<span data-ttu-id="9b374-104">此物件類型的存取類型為：</span><span class="sxs-lookup"><span data-stu-id="9b374-104">The access types of this object type are:</span></span>



| <span data-ttu-id="9b374-105">存取類型</span><span class="sxs-lookup"><span data-stu-id="9b374-105">Access type</span></span>          | <span data-ttu-id="9b374-106">Description</span><span class="sxs-lookup"><span data-stu-id="9b374-106">Description</span></span>                                      |
|----------------------|--------------------------------------------------|
| <span data-ttu-id="9b374-107">秘密 \_ 查詢 \_ 值</span><span class="sxs-lookup"><span data-stu-id="9b374-107">SECRET\_QUERY\_VALUE</span></span> | <span data-ttu-id="9b374-108">需要此存取類型才能取得秘密。</span><span class="sxs-lookup"><span data-stu-id="9b374-108">This access type is needed to retrieve a secret.</span></span> |
| <span data-ttu-id="9b374-109">密碼 \_ 集 \_ 值</span><span class="sxs-lookup"><span data-stu-id="9b374-109">SECRET\_SET\_VALUE</span></span>   | <span data-ttu-id="9b374-110">需要此存取類型才能修改秘密。</span><span class="sxs-lookup"><span data-stu-id="9b374-110">This access type is needed to modify a secret.</span></span>   |



 

## <a name="generic-access-masks"></a><span data-ttu-id="9b374-111">一般存取遮罩</span><span class="sxs-lookup"><span data-stu-id="9b374-111">Generic Access Masks</span></span>

<span data-ttu-id="9b374-112">此物件類型具有下列一般存取對應：</span><span class="sxs-lookup"><span data-stu-id="9b374-112">This object type has the following generic access mappings:</span></span>

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    SECRET_QUERY_VALUE

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    SECRET_SET_VALUE

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a><span data-ttu-id="9b374-113">標準存取類型：</span><span class="sxs-lookup"><span data-stu-id="9b374-113">Standard Access Types:</span></span>

<span data-ttu-id="9b374-114">此物件不支援 (選擇性) 同步處理標準存取類型。</span><span class="sxs-lookup"><span data-stu-id="9b374-114">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="9b374-115">支援所有必要的存取類型。</span><span class="sxs-lookup"><span data-stu-id="9b374-115">All required access types are supported.</span></span> <span data-ttu-id="9b374-116">此物件類型所有支援之存取類型的遮罩為：</span><span class="sxs-lookup"><span data-stu-id="9b374-116">The mask of all supported access types for this object type is:</span></span>

``` syntax
    SECRET_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    SECRET_QUERY_VALUE |
                    SECRET_SET_VALUE
```

 

 



