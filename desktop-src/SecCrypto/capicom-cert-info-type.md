---
description: 定義要從憑證查詢的資訊。
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: 'CAPICOM_CERT_INFO_TYPE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERT_INFO_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8e38bb8940645bbefecb3822bce8de8c2e0eb902
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978696"
---
# <a name="capicom_cert_info_type-enumeration"></a><span data-ttu-id="ce2d5-103">CAPICOM \_ CERT \_ 資訊 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="ce2d5-103">CAPICOM\_CERT\_INFO\_TYPE enumeration</span></span>

<span data-ttu-id="ce2d5-104">**CAPICOM \_ CERT \_ INFO \_ 類型** 列舉類型會定義要從憑證查詢的資訊。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-104">The **CAPICOM\_CERT\_INFO\_TYPE** enumeration type defines what information is to be queried from a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="ce2d5-105">成員</span><span class="sxs-lookup"><span data-stu-id="ce2d5-105">Members</span></span>



| <span data-ttu-id="ce2d5-106">member</span><span class="sxs-lookup"><span data-stu-id="ce2d5-106">Member</span></span>                                         | <span data-ttu-id="ce2d5-107">描述</span><span class="sxs-lookup"><span data-stu-id="ce2d5-107">Description</span></span>                                                                                  | <span data-ttu-id="ce2d5-108">值</span><span class="sxs-lookup"><span data-stu-id="ce2d5-108">Value</span></span> |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="ce2d5-109">**CAPICOM \_ CERT \_ 資訊 \_ 主體 \_ 簡單 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="ce2d5-109">**CAPICOM\_CERT\_INFO\_SUBJECT\_SIMPLE\_NAME**</span></span> | <span data-ttu-id="ce2d5-110">傳回憑證主體的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-110">Returns the display name of the certificate subject.</span></span><br/>                              | <span data-ttu-id="ce2d5-111">0</span><span class="sxs-lookup"><span data-stu-id="ce2d5-111">0</span></span>     |
| <span data-ttu-id="ce2d5-112">**CAPICOM \_ CERT \_ 資訊 \_ 簽發者 \_ 簡單 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="ce2d5-112">**CAPICOM\_CERT\_INFO\_ISSUER\_SIMPLE\_NAME**</span></span>  | <span data-ttu-id="ce2d5-113">傳回憑證簽發者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-113">Returns the display name of the issuer of the certificate.</span></span><br/>                        | <span data-ttu-id="ce2d5-114">1</span><span class="sxs-lookup"><span data-stu-id="ce2d5-114">1</span></span>     |
| <span data-ttu-id="ce2d5-115">**CAPICOM \_ 憑證 \_ 資訊 \_ 主體 \_ 電子郵件 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="ce2d5-115">**CAPICOM\_CERT\_INFO\_SUBJECT\_EMAIL\_NAME**</span></span>  | <span data-ttu-id="ce2d5-116">傳回憑證主體的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-116">Returns the email address of the certificate subject.</span></span><br/>                             | <span data-ttu-id="ce2d5-117">2</span><span class="sxs-lookup"><span data-stu-id="ce2d5-117">2</span></span>     |
| <span data-ttu-id="ce2d5-118">**CAPICOM \_ 憑證 \_ 資訊 \_ 簽發者 \_ 電子郵件 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="ce2d5-118">**CAPICOM\_CERT\_INFO\_ISSUER\_EMAIL\_NAME**</span></span>   | <span data-ttu-id="ce2d5-119">傳回憑證簽發者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-119">Returns the email address of the issuer of the certificate.</span></span><br/>                       | <span data-ttu-id="ce2d5-120">3</span><span class="sxs-lookup"><span data-stu-id="ce2d5-120">3</span></span>     |
| <span data-ttu-id="ce2d5-121">**CAPICOM \_ CERT \_ 資訊 \_ 主體 \_ UPN**</span><span class="sxs-lookup"><span data-stu-id="ce2d5-121">**CAPICOM\_CERT\_INFO\_SUBJECT\_UPN**</span></span>          | <span data-ttu-id="ce2d5-122">傳回憑證主體的 UPN。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-122">Returns the UPN of the certificate subject.</span></span> <span data-ttu-id="ce2d5-123">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-123">Introduced in CAPICOM 2.0.</span></span><br/>            | <span data-ttu-id="ce2d5-124">4</span><span class="sxs-lookup"><span data-stu-id="ce2d5-124">4</span></span>     |
| <span data-ttu-id="ce2d5-125">**CAPICOM \_ CERT \_ 資訊 \_ 簽發者 \_ UPN**</span><span class="sxs-lookup"><span data-stu-id="ce2d5-125">**CAPICOM\_CERT\_INFO\_ISSUER\_UPN**</span></span>           | <span data-ttu-id="ce2d5-126">傳回憑證簽發者的 UPN。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-126">Returns the UPN of the issuer of the certificate.</span></span> <span data-ttu-id="ce2d5-127">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-127">Introduced in CAPICOM 2.0.</span></span><br/>      | <span data-ttu-id="ce2d5-128">5</span><span class="sxs-lookup"><span data-stu-id="ce2d5-128">5</span></span>     |
| <span data-ttu-id="ce2d5-129">**CAPICOM \_ CERT \_ 資訊 \_ 主體 \_ DNS \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="ce2d5-129">**CAPICOM\_CERT\_INFO\_SUBJECT\_DNS\_NAME**</span></span>    | <span data-ttu-id="ce2d5-130">傳回憑證主體的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-130">Returns the DNS name of the certificate subject.</span></span> <span data-ttu-id="ce2d5-131">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-131">Introduced in CAPICOM 2.0.</span></span><br/>       | <span data-ttu-id="ce2d5-132">6</span><span class="sxs-lookup"><span data-stu-id="ce2d5-132">6</span></span>     |
| <span data-ttu-id="ce2d5-133">**CAPICOM \_ 憑證 \_ 資訊 \_ 簽發者 \_ DNS \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="ce2d5-133">**CAPICOM\_CERT\_INFO\_ISSUER\_DNS\_NAME**</span></span>     | <span data-ttu-id="ce2d5-134">傳回憑證簽發者的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-134">Returns the DNS name of the issuer of the certificate.</span></span> <span data-ttu-id="ce2d5-135">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-135">Introduced in CAPICOM 2.0.</span></span><br/> | <span data-ttu-id="ce2d5-136">7</span><span class="sxs-lookup"><span data-stu-id="ce2d5-136">7</span></span>     |



## <a name="remarks"></a><span data-ttu-id="ce2d5-137">備註</span><span class="sxs-lookup"><span data-stu-id="ce2d5-137">Remarks</span></span>

<span data-ttu-id="ce2d5-138">[**GetInfo**](certificate-getinfo.md)方法會使用 **CAPICOM 憑證 \_ \_ 資訊 \_ 類型** 列舉類型。</span><span class="sxs-lookup"><span data-stu-id="ce2d5-138">The **CAPICOM\_CERT\_INFO\_TYPE** enumeration type is used by the [**Certificate.GetInfo**](certificate-getinfo.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce2d5-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce2d5-139">Requirements</span></span>



| <span data-ttu-id="ce2d5-140">需求</span><span class="sxs-lookup"><span data-stu-id="ce2d5-140">Requirement</span></span> | <span data-ttu-id="ce2d5-141">值</span><span class="sxs-lookup"><span data-stu-id="ce2d5-141">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ce2d5-142">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ce2d5-142">Redistributable</span></span><br/> | <span data-ttu-id="ce2d5-143">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ce2d5-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="ce2d5-144">標頭</span><span class="sxs-lookup"><span data-stu-id="ce2d5-144">Header</span></span><br/>          | <dl> <span data-ttu-id="ce2d5-145"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="ce2d5-145"><dt>Capicom.h</dt></span></span> </dl> |



 

 




