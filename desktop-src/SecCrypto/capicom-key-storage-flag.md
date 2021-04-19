---
description: CAPICOM \_ 金鑰 \_ 儲存 \_ 旗標列舉會定義金鑰儲存體旗標。
ms.assetid: 326cef75-24a5-4dc9-a7e9-a63dd3d8de54
title: 'CAPICOM_KEY_STORAGE_FLAG 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_STORAGE_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 9edbc3a5ac3396e528ebbb5390c4b07c24770e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987103"
---
# <a name="capicom_key_storage_flag-enumeration"></a><span data-ttu-id="b8c39-103">CAPICOM \_ 金鑰 \_ 儲存 \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="b8c39-103">CAPICOM\_KEY\_STORAGE\_FLAG enumeration</span></span>

<span data-ttu-id="b8c39-104">**CAPICOM \_ 金鑰 \_ 儲存 \_ 旗** 標列舉會定義金鑰儲存體旗標。</span><span class="sxs-lookup"><span data-stu-id="b8c39-104">The **CAPICOM\_KEY\_STORAGE\_FLAG** enumeration defines key storage flags.</span></span>

## <a name="members"></a><span data-ttu-id="b8c39-105">成員</span><span class="sxs-lookup"><span data-stu-id="b8c39-105">Members</span></span>



| <span data-ttu-id="b8c39-106">member</span><span class="sxs-lookup"><span data-stu-id="b8c39-106">Member</span></span>                                     | <span data-ttu-id="b8c39-107">描述</span><span class="sxs-lookup"><span data-stu-id="b8c39-107">Description</span></span>                           | <span data-ttu-id="b8c39-108">值</span><span class="sxs-lookup"><span data-stu-id="b8c39-108">Value</span></span> |
|--------------------------------------------|---------------------------------------|-------|
| <span data-ttu-id="b8c39-109">**CAPICOM \_ 金鑰 \_ 儲存 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="b8c39-109">**CAPICOM\_KEY\_STORAGE\_DEFAULT**</span></span>         | <span data-ttu-id="b8c39-110">預設金鑰存放區。</span><span class="sxs-lookup"><span data-stu-id="b8c39-110">Default key storage.</span></span><br/>       | <span data-ttu-id="b8c39-111">0</span><span class="sxs-lookup"><span data-stu-id="b8c39-111">0</span></span>     |
| <span data-ttu-id="b8c39-112">**可 \_ 匯出的 CAPICOM 金鑰 \_ 儲存體 \_**</span><span class="sxs-lookup"><span data-stu-id="b8c39-112">**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</span></span>      | <span data-ttu-id="b8c39-113">金鑰可以匯出。</span><span class="sxs-lookup"><span data-stu-id="b8c39-113">The key is exportable.</span></span><br/>     | <span data-ttu-id="b8c39-114">1</span><span class="sxs-lookup"><span data-stu-id="b8c39-114">1</span></span>     |
| <span data-ttu-id="b8c39-115">**已 \_ 保護的 CAPICOM 金鑰 \_ 儲存區 \_ 使用者 \_**</span><span class="sxs-lookup"><span data-stu-id="b8c39-115">**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</span></span> | <span data-ttu-id="b8c39-116">金鑰是由使用者保護。</span><span class="sxs-lookup"><span data-stu-id="b8c39-116">The key is user protected.</span></span><br/> | <span data-ttu-id="b8c39-117">2</span><span class="sxs-lookup"><span data-stu-id="b8c39-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="b8c39-118">備註</span><span class="sxs-lookup"><span data-stu-id="b8c39-118">Remarks</span></span>

<span data-ttu-id="b8c39-119">下列方法會使用這個列舉：</span><span class="sxs-lookup"><span data-stu-id="b8c39-119">This enumeration is used by the following method:</span></span>

-   [<span data-ttu-id="b8c39-120">**Certificate。 Load**</span><span class="sxs-lookup"><span data-stu-id="b8c39-120">**Certificate.Load**</span></span>](certificate-load.md)
-   [<span data-ttu-id="b8c39-121">**存放區載入**</span><span class="sxs-lookup"><span data-stu-id="b8c39-121">**Store.Load**</span></span>](store-load.md)

## <a name="requirements"></a><span data-ttu-id="b8c39-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8c39-122">Requirements</span></span>



| <span data-ttu-id="b8c39-123">需求</span><span class="sxs-lookup"><span data-stu-id="b8c39-123">Requirement</span></span> | <span data-ttu-id="b8c39-124">值</span><span class="sxs-lookup"><span data-stu-id="b8c39-124">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c39-125">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b8c39-125">Redistributable</span></span><br/> | <span data-ttu-id="b8c39-126">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b8c39-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="b8c39-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b8c39-127">Header</span></span><br/>          | <dl> <span data-ttu-id="b8c39-128"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="b8c39-128"><dt>Capicom.h</dt></span></span> </dl> |



 

 




