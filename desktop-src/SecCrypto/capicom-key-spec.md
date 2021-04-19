---
description: CAPICOM \_ 金鑰 \_ 規格列舉會定義金鑰規格。
ms.assetid: e4aaaf69-ab28-4e8c-8a8a-6dc662299865
title: 'CAPICOM_KEY_SPEC 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_SPEC
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 153f0431d78ff595b4d568fd7a677abea0d28be7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990202"
---
# <a name="capicom_key_spec-enumeration"></a><span data-ttu-id="fcbbd-103">CAPICOM \_ 金鑰 \_ 規格列舉</span><span class="sxs-lookup"><span data-stu-id="fcbbd-103">CAPICOM\_KEY\_SPEC enumeration</span></span>

<span data-ttu-id="fcbbd-104">**CAPICOM \_ 金鑰 \_ 規格** 列舉會定義金鑰規格。</span><span class="sxs-lookup"><span data-stu-id="fcbbd-104">The **CAPICOM\_KEY\_SPEC** enumeration defines key specifications.</span></span>

## <a name="members"></a><span data-ttu-id="fcbbd-105">成員</span><span class="sxs-lookup"><span data-stu-id="fcbbd-105">Members</span></span>



| <span data-ttu-id="fcbbd-106">member</span><span class="sxs-lookup"><span data-stu-id="fcbbd-106">Member</span></span>                              | <span data-ttu-id="fcbbd-107">描述</span><span class="sxs-lookup"><span data-stu-id="fcbbd-107">Description</span></span>                                                | <span data-ttu-id="fcbbd-108">值</span><span class="sxs-lookup"><span data-stu-id="fcbbd-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|-------|
| <span data-ttu-id="fcbbd-109">**CAPICOM \_ 金鑰 \_ 規格 \_ KEYEXCHANGE**</span><span class="sxs-lookup"><span data-stu-id="fcbbd-109">**CAPICOM\_KEY\_SPEC\_KEYEXCHANGE**</span></span> | <span data-ttu-id="fcbbd-110">金鑰可用於加密和簽署。</span><span class="sxs-lookup"><span data-stu-id="fcbbd-110">The key can be used for encryption and signing.</span></span><br/> | <span data-ttu-id="fcbbd-111">1</span><span class="sxs-lookup"><span data-stu-id="fcbbd-111">1</span></span>     |
| <span data-ttu-id="fcbbd-112">**CAPICOM \_ 金鑰 \_ 規格簽章 \_**</span><span class="sxs-lookup"><span data-stu-id="fcbbd-112">**CAPICOM\_KEY\_SPEC\_SIGNATURE**</span></span>   | <span data-ttu-id="fcbbd-113">金鑰只能用於簽署。</span><span class="sxs-lookup"><span data-stu-id="fcbbd-113">The key can be used only for signing.</span></span><br/>           | <span data-ttu-id="fcbbd-114">2</span><span class="sxs-lookup"><span data-stu-id="fcbbd-114">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="fcbbd-115">備註</span><span class="sxs-lookup"><span data-stu-id="fcbbd-115">Remarks</span></span>

<span data-ttu-id="fcbbd-116">下列方法和屬性會使用 **CAPICOM \_ 金鑰 \_ 規格** 列舉：</span><span class="sxs-lookup"><span data-stu-id="fcbbd-116">The **CAPICOM\_KEY\_SPEC** enumeration is used by the following methods and properties:</span></span>

-   <span data-ttu-id="fcbbd-117">[**PrivateKey. KeySpec**](privatekey-keyspec.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="fcbbd-117">[**PrivateKey.KeySpec**](privatekey-keyspec.md) property.</span></span>
-   <span data-ttu-id="fcbbd-118">[**PrivateKey。 Open**](privatekey-open.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="fcbbd-118">[**PrivateKey.Open**](privatekey-open.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcbbd-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="fcbbd-119">Requirements</span></span>



| <span data-ttu-id="fcbbd-120">需求</span><span class="sxs-lookup"><span data-stu-id="fcbbd-120">Requirement</span></span> | <span data-ttu-id="fcbbd-121">值</span><span class="sxs-lookup"><span data-stu-id="fcbbd-121">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fcbbd-122">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="fcbbd-122">Redistributable</span></span><br/> | <span data-ttu-id="fcbbd-123">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="fcbbd-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="fcbbd-124">標頭</span><span class="sxs-lookup"><span data-stu-id="fcbbd-124">Header</span></span><br/>          | <dl> <span data-ttu-id="fcbbd-125"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="fcbbd-125"><dt>Capicom.h</dt></span></span> </dl> |



 

 




