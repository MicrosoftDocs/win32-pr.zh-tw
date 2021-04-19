---
description: 根據可用的位置定義擴充金鑰使用方式名稱。
ms.assetid: 78f9f9cb-46e7-4f81-a16e-503750a0d743
title: 'CAPICOM_EKU 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EKU
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: e1d2f4f435fa31df00b87e20254aad57b690b047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994703"
---
# <a name="capicom_eku-enumeration"></a><span data-ttu-id="16e03-103">CAPICOM \_ EKU 列舉</span><span class="sxs-lookup"><span data-stu-id="16e03-103">CAPICOM\_EKU enumeration</span></span>

<span data-ttu-id="16e03-104">**CAPICOM \_ EKU** 列舉型別會根據可用的位置來定義擴充金鑰使用方式名稱。</span><span class="sxs-lookup"><span data-stu-id="16e03-104">The **CAPICOM\_EKU** enumeration type defines the extended key usage names based on where they can be used.</span></span>

## <a name="members"></a><span data-ttu-id="16e03-105">成員</span><span class="sxs-lookup"><span data-stu-id="16e03-105">Members</span></span>



| <span data-ttu-id="16e03-106">member</span><span class="sxs-lookup"><span data-stu-id="16e03-106">Member</span></span>                                     | <span data-ttu-id="16e03-107">描述</span><span class="sxs-lookup"><span data-stu-id="16e03-107">Description</span></span>                                                                                                                                                 | <span data-ttu-id="16e03-108">值</span><span class="sxs-lookup"><span data-stu-id="16e03-108">Value</span></span> |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="16e03-109">**CAPICOM \_ EKU \_ 其他**</span><span class="sxs-lookup"><span data-stu-id="16e03-109">**CAPICOM\_EKU\_OTHER**</span></span>                    | <span data-ttu-id="16e03-110">憑證具有在本機原則中定義的使用方式。</span><span class="sxs-lookup"><span data-stu-id="16e03-110">Certificate has uses defined in local policy.</span></span> <span data-ttu-id="16e03-111">如果需要的 EKU 未預先定義，而且應用程式必須設定 OID 值，就會使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="16e03-111">This is used if the EKU needed is not predefined and the OID value must be set by the application.</span></span><br/> | <span data-ttu-id="16e03-112">0</span><span class="sxs-lookup"><span data-stu-id="16e03-112">0</span></span>     |
| <span data-ttu-id="16e03-113">**CAPICOM \_ EKU \_ 伺服器 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="16e03-113">**CAPICOM\_EKU\_SERVER\_AUTH**</span></span>             | <span data-ttu-id="16e03-114">憑證可以用來驗證服務器。</span><span class="sxs-lookup"><span data-stu-id="16e03-114">Certificate can be used to authenticate a server.</span></span><br/>                                                                                                | <span data-ttu-id="16e03-115">1</span><span class="sxs-lookup"><span data-stu-id="16e03-115">1</span></span>     |
| <span data-ttu-id="16e03-116">**CAPICOM \_ EKU \_ 用戶端 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="16e03-116">**CAPICOM\_EKU\_CLIENT\_AUTH**</span></span>             | <span data-ttu-id="16e03-117">憑證可以用來驗證用戶端。</span><span class="sxs-lookup"><span data-stu-id="16e03-117">Certificate can be used to authenticate a client.</span></span><br/>                                                                                                | <span data-ttu-id="16e03-118">2</span><span class="sxs-lookup"><span data-stu-id="16e03-118">2</span></span>     |
| <span data-ttu-id="16e03-119">**CAPICOM \_ EKU 程式 \_ 代碼 \_ 簽署**</span><span class="sxs-lookup"><span data-stu-id="16e03-119">**CAPICOM\_EKU\_CODE\_SIGNING**</span></span>            | <span data-ttu-id="16e03-120">憑證可以用來建立數位簽章。</span><span class="sxs-lookup"><span data-stu-id="16e03-120">Certificate can be used to create a digital signature.</span></span><br/>                                                                                           | <span data-ttu-id="16e03-121">3</span><span class="sxs-lookup"><span data-stu-id="16e03-121">3</span></span>     |
| <span data-ttu-id="16e03-122">**CAPICOM \_ EKU \_ 電子郵件 \_ 保護**</span><span class="sxs-lookup"><span data-stu-id="16e03-122">**CAPICOM\_EKU\_EMAIL\_PROTECTION**</span></span>        | <span data-ttu-id="16e03-123">憑證可用於電子郵件保護。</span><span class="sxs-lookup"><span data-stu-id="16e03-123">Certificate can be used for email protection.</span></span><br/>                                                                                                    | <span data-ttu-id="16e03-124">4</span><span class="sxs-lookup"><span data-stu-id="16e03-124">4</span></span>     |
| <span data-ttu-id="16e03-125">**CAPICOM \_ EKU \_ 智慧卡 \_ 登入**</span><span class="sxs-lookup"><span data-stu-id="16e03-125">**CAPICOM\_EKU\_SMARTCARD\_LOGON**</span></span>         | <span data-ttu-id="16e03-126">憑證可用於智慧卡登入。</span><span class="sxs-lookup"><span data-stu-id="16e03-126">Certificate can be used for smart card logon.</span></span> <span data-ttu-id="16e03-127">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="16e03-127">Introduced in CAPICOM 2.0.</span></span><br/>                                                                         | <span data-ttu-id="16e03-128">5</span><span class="sxs-lookup"><span data-stu-id="16e03-128">5</span></span>     |
| <span data-ttu-id="16e03-129">**CAPICOM \_ EKU \_ 加密 \_ 檔 \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="16e03-129">**CAPICOM\_EKU\_ENCRYPTING\_FILE\_SYSTEM**</span></span> | <span data-ttu-id="16e03-130">憑證可用於 EFS。</span><span class="sxs-lookup"><span data-stu-id="16e03-130">Certificate can be used for EFS.</span></span> <span data-ttu-id="16e03-131">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="16e03-131">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                      | <span data-ttu-id="16e03-132">6</span><span class="sxs-lookup"><span data-stu-id="16e03-132">6</span></span>     |



## <a name="remarks"></a><span data-ttu-id="16e03-133">備註</span><span class="sxs-lookup"><span data-stu-id="16e03-133">Remarks</span></span>

<span data-ttu-id="16e03-134">Eku 會使用 **CAPICOM \_ eku** 列舉型別 [**。Name**](eku-name.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="16e03-134">The **CAPICOM\_EKU** enumeration type is used by the [**EKU.Name**](eku-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="16e03-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="16e03-135">Requirements</span></span>



| <span data-ttu-id="16e03-136">需求</span><span class="sxs-lookup"><span data-stu-id="16e03-136">Requirement</span></span> | <span data-ttu-id="16e03-137">值</span><span class="sxs-lookup"><span data-stu-id="16e03-137">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="16e03-138">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="16e03-138">Redistributable</span></span><br/> | <span data-ttu-id="16e03-139">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="16e03-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="16e03-140">標頭</span><span class="sxs-lookup"><span data-stu-id="16e03-140">Header</span></span><br/>          | <dl> <span data-ttu-id="16e03-141"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="16e03-141"><dt>Capicom.h</dt></span></span> </dl> |



 

 




