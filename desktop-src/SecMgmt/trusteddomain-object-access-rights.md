---
description: 列出並說明 TrustedDomain 物件的存取權限。
ms.assetid: eb82864c-7e69-4ed5-a55d-d6792670bcd1
title: TrustedDomain 物件存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f79dc44b54ff907cbe3d1f700cc673f75a40d57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972394"
---
# <a name="trusteddomain-object-access-rights"></a><span data-ttu-id="fcbbb-103">TrustedDomain 物件存取權限</span><span class="sxs-lookup"><span data-stu-id="fcbbb-103">TrustedDomain Object Access Rights</span></span>

<span data-ttu-id="fcbbb-104">[**TrustedDomain**](trusteddomain-object.md)物件類型具有下列存取類型：</span><span class="sxs-lookup"><span data-stu-id="fcbbb-104">The [**TrustedDomain**](trusteddomain-object.md) object type has the following access types:</span></span>



| <span data-ttu-id="fcbbb-105">存取類型</span><span class="sxs-lookup"><span data-stu-id="fcbbb-105">Access type</span></span>                  | <span data-ttu-id="fcbbb-106">Description</span><span class="sxs-lookup"><span data-stu-id="fcbbb-106">Description</span></span>                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fcbbb-107">受信任的 \_ 查詢 \_ 功能變數名稱 \_</span><span class="sxs-lookup"><span data-stu-id="fcbbb-107">TRUSTED\_QUERY\_DOMAIN\_NAME</span></span> | <span data-ttu-id="fcbbb-108">需要此存取類型才能查詢受信任網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcbbb-108">This access type is needed to query the name of the trusted domain.</span></span>              |
| <span data-ttu-id="fcbbb-109">信任的 \_ 設定 \_ 控制器</span><span class="sxs-lookup"><span data-stu-id="fcbbb-109">TRUSTED\_SET\_CONTROLLERS</span></span>    | <span data-ttu-id="fcbbb-110">需要此存取類型才能設定受信任網域的控制器清單。</span><span class="sxs-lookup"><span data-stu-id="fcbbb-110">This access type is needed to set the list of controllers of the trusted domain.</span></span> |
| <span data-ttu-id="fcbbb-111">信任的 \_ 查詢 \_ POSIX</span><span class="sxs-lookup"><span data-stu-id="fcbbb-111">TRUSTED\_QUERY\_POSIX</span></span>        | <span data-ttu-id="fcbbb-112">需要此存取類型才能取得受信任網域的 Posix 識別碼位移。</span><span class="sxs-lookup"><span data-stu-id="fcbbb-112">This access type is needed to retrieve the Posix ID offset of a trusted domain.</span></span>  |
| <span data-ttu-id="fcbbb-113">信任的 \_ 組 \_ POSIX</span><span class="sxs-lookup"><span data-stu-id="fcbbb-113">TRUSTED\_SET\_POSIX</span></span>          | <span data-ttu-id="fcbbb-114">需要此存取類型才能設定受信任網域的 Posix 識別碼位移。</span><span class="sxs-lookup"><span data-stu-id="fcbbb-114">This access type is needed to set the Posix ID offset of a trusted domain.</span></span>       |



 

## <a name="generic-access-masks"></a><span data-ttu-id="fcbbb-115">一般存取遮罩</span><span class="sxs-lookup"><span data-stu-id="fcbbb-115">Generic Access Masks</span></span>

<span data-ttu-id="fcbbb-116">此物件類型具有下列一般存取對應：</span><span class="sxs-lookup"><span data-stu-id="fcbbb-116">This object type has the following generic access mappings:</span></span>

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                    TRUSTED_QUERY_DOMAIN_NAME

    GENERIC_WRITE        STANDARD_RIGHTS_WRITE |
                    TRUSTED_SET_POSIX

    GENERIC_EXECUTE    STANDARD_RIGHTS_EXECUTE |
                    TRUSTED_QUERY_POSIX
```

## <a name="standard-access-types"></a><span data-ttu-id="fcbbb-117">標準存取類型</span><span class="sxs-lookup"><span data-stu-id="fcbbb-117">Standard Access Types</span></span>

<span data-ttu-id="fcbbb-118">此物件不支援 (選擇性) 同步處理標準存取類型。</span><span class="sxs-lookup"><span data-stu-id="fcbbb-118">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="fcbbb-119">支援所有必要的存取類型。</span><span class="sxs-lookup"><span data-stu-id="fcbbb-119">All required access types are supported.</span></span> <span data-ttu-id="fcbbb-120">此物件類型所有支援之存取類型的遮罩為：</span><span class="sxs-lookup"><span data-stu-id="fcbbb-120">The mask of all supported access types for this object type is:</span></span>

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



