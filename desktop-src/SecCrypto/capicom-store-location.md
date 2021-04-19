---
description: 指出憑證存放區的位置。
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: 'CAPICOM_STORE_LOCATION 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 24b2e786e2821c39c6ff67f5919dca2ac0c6bfe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000907"
---
# <a name="capicom_store_location-enumeration"></a><span data-ttu-id="060db-103">CAPICOM \_ 存放區 \_ 位置列舉</span><span class="sxs-lookup"><span data-stu-id="060db-103">CAPICOM\_STORE\_LOCATION enumeration</span></span>

<span data-ttu-id="060db-104">**CAPICOM \_ 存放區 \_ 位置** 列舉型別指出 [*憑證存放區*](../secgloss/c-gly.md)的位置。</span><span class="sxs-lookup"><span data-stu-id="060db-104">The **CAPICOM\_STORE\_LOCATION** enumeration type indicates the location of a [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="060db-105">成員</span><span class="sxs-lookup"><span data-stu-id="060db-105">Members</span></span>



| <span data-ttu-id="060db-106">member</span><span class="sxs-lookup"><span data-stu-id="060db-106">Member</span></span>                                      | <span data-ttu-id="060db-107">描述</span><span class="sxs-lookup"><span data-stu-id="060db-107">Description</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="060db-108">值</span><span class="sxs-lookup"><span data-stu-id="060db-108">Value</span></span> |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="060db-109">**CAPICOM \_ 記憶體 \_ 存放區**</span><span class="sxs-lookup"><span data-stu-id="060db-109">**CAPICOM\_MEMORY\_STORE**</span></span>                  | <span data-ttu-id="060db-110">存放區是記憶體存放區。</span><span class="sxs-lookup"><span data-stu-id="060db-110">The store is a memory store.</span></span> <span data-ttu-id="060db-111">存放區內容中的任何變更都不會保存。</span><span class="sxs-lookup"><span data-stu-id="060db-111">Any changes in the contents of the store are not persisted.</span></span><br/>                                                                                                                                                                              | <span data-ttu-id="060db-112">0</span><span class="sxs-lookup"><span data-stu-id="060db-112">0</span></span>     |
| <span data-ttu-id="060db-113">**CAPICOM \_ 本機 \_ 電腦 \_ 存放區**</span><span class="sxs-lookup"><span data-stu-id="060db-113">**CAPICOM\_LOCAL\_MACHINE\_STORE**</span></span>          | <span data-ttu-id="060db-114">存放區是本機電腦存放區。</span><span class="sxs-lookup"><span data-stu-id="060db-114">The store is a local machine store.</span></span> <span data-ttu-id="060db-115">只有當使用者擁有讀取/寫入權限時，本機電腦存放區才能成為讀取/寫入存放區。</span><span class="sxs-lookup"><span data-stu-id="060db-115">Local machine stores can be read/write stores only if the user has read/write permissions.</span></span> <span data-ttu-id="060db-116">如果使用者具有讀取/寫入權限，且存放區已開啟讀取/寫入，則會保存存放區內容中的變更。</span><span class="sxs-lookup"><span data-stu-id="060db-116">If the user has read/write permissions and if the store is opened read/write, then changes in the contents of the store are persisted.</span></span><br/> | <span data-ttu-id="060db-117">1</span><span class="sxs-lookup"><span data-stu-id="060db-117">1</span></span>     |
| <span data-ttu-id="060db-118">**CAPICOM \_ 目前的 \_ 使用者 \_ 存放區**</span><span class="sxs-lookup"><span data-stu-id="060db-118">**CAPICOM\_CURRENT\_USER\_STORE**</span></span>           | <span data-ttu-id="060db-119">存放區是目前的使用者存放區。</span><span class="sxs-lookup"><span data-stu-id="060db-119">The store is a current user store.</span></span> <span data-ttu-id="060db-120">目前的使用者存放區可能是「讀取/寫入」存放區。</span><span class="sxs-lookup"><span data-stu-id="060db-120">A current user store may be a read/write store.</span></span> <span data-ttu-id="060db-121">如果是，就會保存存放區內容中的變更。</span><span class="sxs-lookup"><span data-stu-id="060db-121">If it is, changes in the contents of the store are persisted.</span></span><br/>                                                                                                                      | <span data-ttu-id="060db-122">2</span><span class="sxs-lookup"><span data-stu-id="060db-122">2</span></span>     |
| <span data-ttu-id="060db-123">**CAPICOM \_ ACTIVE \_ DIRECTORY \_ 使用者 \_ 存放區**</span><span class="sxs-lookup"><span data-stu-id="060db-123">**CAPICOM\_ACTIVE\_DIRECTORY\_USER\_STORE**</span></span> | <span data-ttu-id="060db-124">存放區是 Active Directory 存放區。</span><span class="sxs-lookup"><span data-stu-id="060db-124">The store is an Active Directory store.</span></span> <span data-ttu-id="060db-125">Active Directory 存放區只能在唯讀模式中開啟。</span><span class="sxs-lookup"><span data-stu-id="060db-125">Active Directory stores can be opened only in read-only mode.</span></span> <span data-ttu-id="060db-126">憑證無法在 Active Directory 存放區中新增或移除。</span><span class="sxs-lookup"><span data-stu-id="060db-126">Certificates cannot be added to or removed from Active Directory stores.</span></span><br/>                                                                                        | <span data-ttu-id="060db-127">3</span><span class="sxs-lookup"><span data-stu-id="060db-127">3</span></span>     |
| <span data-ttu-id="060db-128">**CAPICOM \_ 智慧 \_ 卡 \_ 使用者 \_ 存放區**</span><span class="sxs-lookup"><span data-stu-id="060db-128">**CAPICOM\_SMART\_CARD\_USER\_STORE**</span></span>       | <span data-ttu-id="060db-129">存放區支援以智慧卡為基礎的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="060db-129">Stores support smart card–based certificate stores.</span></span> <span data-ttu-id="060db-130">存放區是一組目前的智慧卡。</span><span class="sxs-lookup"><span data-stu-id="060db-130">The store is the group of present smart cards.</span></span> <span data-ttu-id="060db-131">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="060db-131">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                                                                         | <span data-ttu-id="060db-132">4</span><span class="sxs-lookup"><span data-stu-id="060db-132">4</span></span>     |



## <a name="remarks"></a><span data-ttu-id="060db-133">備註</span><span class="sxs-lookup"><span data-stu-id="060db-133">Remarks</span></span>

<span data-ttu-id="060db-134">下列方法會使用 **CAPICOM \_ 存放區 \_ 位置** 列舉類型：</span><span class="sxs-lookup"><span data-stu-id="060db-134">The **CAPICOM\_STORE\_LOCATION** enumeration type is used by the following methods:</span></span>

-   [<span data-ttu-id="060db-135">**PrivateKey。開啟**</span><span class="sxs-lookup"><span data-stu-id="060db-135">**PrivateKey.Open**</span></span>](privatekey-open.md)
-   [<span data-ttu-id="060db-136">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="060db-136">**Store.Open**</span></span>](store-open.md)

## <a name="requirements"></a><span data-ttu-id="060db-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="060db-137">Requirements</span></span>



| <span data-ttu-id="060db-138">需求</span><span class="sxs-lookup"><span data-stu-id="060db-138">Requirement</span></span> | <span data-ttu-id="060db-139">值</span><span class="sxs-lookup"><span data-stu-id="060db-139">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="060db-140">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="060db-140">Redistributable</span></span><br/> | <span data-ttu-id="060db-141">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="060db-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="060db-142">標頭</span><span class="sxs-lookup"><span data-stu-id="060db-142">Header</span></span><br/>          | <dl> <span data-ttu-id="060db-143"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="060db-143"><dt>Capicom.h</dt></span></span> </dl> |



 

 
