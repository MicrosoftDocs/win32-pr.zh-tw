---
description: 與 Store. Open 方法搭配使用，以指出如何開啟憑證存放區。
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: 'CAPICOM_STORE_OPEN_MODE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_OPEN_MODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 61fe8be0bdf75db5204066563ca07f8225678f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995402"
---
# <a name="capicom_store_open_mode-enumeration"></a><span data-ttu-id="c7fb9-103">CAPICOM \_ 存放區 \_ 開啟 \_ 模式列舉</span><span class="sxs-lookup"><span data-stu-id="c7fb9-103">CAPICOM\_STORE\_OPEN\_MODE enumeration</span></span>

<span data-ttu-id="c7fb9-104">CAPICOM \_ 存放區 \_ 開啟 \_ 模式列舉型別會與 [**STORE. open**](store-open.md) 方法搭配使用，以指出如何開啟憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="c7fb9-104">The CAPICOM\_STORE\_OPEN\_MODE enumeration type is used with the [**Store.Open**](store-open.md) method to indicate how a certificate store is to be opened.</span></span>

## <a name="members"></a><span data-ttu-id="c7fb9-105">成員</span><span class="sxs-lookup"><span data-stu-id="c7fb9-105">Members</span></span>



| <span data-ttu-id="c7fb9-106">member</span><span class="sxs-lookup"><span data-stu-id="c7fb9-106">Member</span></span>                                      | <span data-ttu-id="c7fb9-107">描述</span><span class="sxs-lookup"><span data-stu-id="c7fb9-107">Description</span></span>                                                                                                                                                              | <span data-ttu-id="c7fb9-108">值</span><span class="sxs-lookup"><span data-stu-id="c7fb9-108">Value</span></span> |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="c7fb9-109">**CAPICOM \_ 存放區 \_ 開啟 \_ 唯讀 \_**</span><span class="sxs-lookup"><span data-stu-id="c7fb9-109">**CAPICOM\_STORE\_OPEN\_READ\_ONLY**</span></span>        | <span data-ttu-id="c7fb9-110">在唯讀模式開啟存放區。</span><span class="sxs-lookup"><span data-stu-id="c7fb9-110">Open the store in read-only mode.</span></span><br/>                                                                                                                             | <span data-ttu-id="c7fb9-111">0</span><span class="sxs-lookup"><span data-stu-id="c7fb9-111">0</span></span>     |
| <span data-ttu-id="c7fb9-112">**CAPICOM \_ 存放區 \_ 開啟 \_ 讀 \_ 寫**</span><span class="sxs-lookup"><span data-stu-id="c7fb9-112">**CAPICOM\_STORE\_OPEN\_READ\_WRITE**</span></span>       | <span data-ttu-id="c7fb9-113">以讀取/寫入模式開啟存放區。</span><span class="sxs-lookup"><span data-stu-id="c7fb9-113">Open the store in read/write mode.</span></span><br/>                                                                                                                            | <span data-ttu-id="c7fb9-114">1</span><span class="sxs-lookup"><span data-stu-id="c7fb9-114">1</span></span>     |
| <span data-ttu-id="c7fb9-115">**允許的 CAPICOM \_ 存放區 \_ 開啟 \_ 上限 \_**</span><span class="sxs-lookup"><span data-stu-id="c7fb9-115">**CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED**</span></span>  | <span data-ttu-id="c7fb9-116">如果使用者具有讀取/寫入權限，請以讀取/寫入模式開啟存放區。</span><span class="sxs-lookup"><span data-stu-id="c7fb9-116">Open the store in read/write mode if the user has read/write permissions.</span></span> <span data-ttu-id="c7fb9-117">如果使用者沒有讀取/寫入權限，請在唯讀模式中開啟存放區。</span><span class="sxs-lookup"><span data-stu-id="c7fb9-117">If the user does not have read/write permissions, open the store in read-only mode.</span></span><br/> | <span data-ttu-id="c7fb9-118">2</span><span class="sxs-lookup"><span data-stu-id="c7fb9-118">2</span></span>     |
| <span data-ttu-id="c7fb9-119">**CAPICOM \_ 存放 \_ 區 \_ 僅開啟現有 \_ 的**</span><span class="sxs-lookup"><span data-stu-id="c7fb9-119">**CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY**</span></span>    | <span data-ttu-id="c7fb9-120">僅開啟現有的商店;請勿建立新的存放區。</span><span class="sxs-lookup"><span data-stu-id="c7fb9-120">Open existing stores only; do not create a new store.</span></span> <span data-ttu-id="c7fb9-121">由 CAPICOM 2.0 引進。</span><span class="sxs-lookup"><span data-stu-id="c7fb9-121">Introduced by CAPICOM 2.0.</span></span><br/>                                                                              | <span data-ttu-id="c7fb9-122">128</span><span class="sxs-lookup"><span data-stu-id="c7fb9-122">128</span></span>   |
| <span data-ttu-id="c7fb9-123">**開啟的 CAPICOM \_ 存放區 \_ \_ 包含 \_ 封存**</span><span class="sxs-lookup"><span data-stu-id="c7fb9-123">**CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED**</span></span> | <span data-ttu-id="c7fb9-124">使用存放區時，請包含封存的憑證。</span><span class="sxs-lookup"><span data-stu-id="c7fb9-124">Include archived certificates when using the store.</span></span> <span data-ttu-id="c7fb9-125">由 CAPICOM 2.0 引進。</span><span class="sxs-lookup"><span data-stu-id="c7fb9-125">Introduced by CAPICOM 2.0.</span></span><br/>                                                                                | <span data-ttu-id="c7fb9-126">256</span><span class="sxs-lookup"><span data-stu-id="c7fb9-126">256</span></span>   |



## <a name="remarks"></a><span data-ttu-id="c7fb9-127">備註</span><span class="sxs-lookup"><span data-stu-id="c7fb9-127">Remarks</span></span>

<span data-ttu-id="c7fb9-128">使用 CAPICOM \_ 存放區 \_ 開放式 \_ 模式列舉時，只能使用下列其中一個設定。</span><span class="sxs-lookup"><span data-stu-id="c7fb9-128">When using the CAPICOM\_STORE\_OPEN\_MODE enumeration, only one of the following settings can be used.</span></span>

-   <span data-ttu-id="c7fb9-129">CAPICOM \_ 存放區 \_ 開啟 \_ 唯讀 \_</span><span class="sxs-lookup"><span data-stu-id="c7fb9-129">CAPICOM\_STORE\_OPEN\_READ\_ONLY</span></span>
-   <span data-ttu-id="c7fb9-130">CAPICOM \_ 存放區 \_ 開啟 \_ 讀 \_ 寫</span><span class="sxs-lookup"><span data-stu-id="c7fb9-130">CAPICOM\_STORE\_OPEN\_READ\_WRITE</span></span>
-   <span data-ttu-id="c7fb9-131">允許的 CAPICOM \_ 存放區 \_ 開啟 \_ 上限 \_</span><span class="sxs-lookup"><span data-stu-id="c7fb9-131">CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED</span></span>

## <a name="requirements"></a><span data-ttu-id="c7fb9-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7fb9-132">Requirements</span></span>



| <span data-ttu-id="c7fb9-133">需求</span><span class="sxs-lookup"><span data-stu-id="c7fb9-133">Requirement</span></span> | <span data-ttu-id="c7fb9-134">值</span><span class="sxs-lookup"><span data-stu-id="c7fb9-134">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c7fb9-135">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c7fb9-135">Redistributable</span></span><br/> | <span data-ttu-id="c7fb9-136">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c7fb9-136">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="c7fb9-137">標頭</span><span class="sxs-lookup"><span data-stu-id="c7fb9-137">Header</span></span><br/>          | <dl> <span data-ttu-id="c7fb9-138"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="c7fb9-138"><dt>Capicom.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7fb9-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7fb9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7fb9-140">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="c7fb9-140">**Store.Open**</span></span>](store-open.md)
</dt> </dl>

 

 




