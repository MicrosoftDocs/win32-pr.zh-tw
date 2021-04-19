---
description: CAPICOM \_ 憑證 \_ 尋找 \_ 類型列舉類型會定義用來尋找特定憑證的搜尋準則類型。 此列舉類型是在 CAPICOM 2.0 中引進。
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: 'CAPICOM_CERTIFICATE_FIND_TYPE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_FIND_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: c5c867b230ba2045d97619d7f55e257bd7803b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982932"
---
# <a name="capicom_certificate_find_type-enumeration"></a><span data-ttu-id="115f2-104">CAPICOM \_ 憑證 \_ 尋找 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="115f2-104">CAPICOM\_CERTIFICATE\_FIND\_TYPE enumeration</span></span>

<span data-ttu-id="115f2-105">**CAPICOM \_ 憑證 \_ 尋找 \_ 類型** 列舉類型會定義用來尋找特定憑證的搜尋準則類型。</span><span class="sxs-lookup"><span data-stu-id="115f2-105">The **CAPICOM\_CERTIFICATE\_FIND\_TYPE** enumeration type defines the type of search criteria used to find specific certificates.</span></span> <span data-ttu-id="115f2-106">此列舉類型是在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="115f2-106">This enumeration type was introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="115f2-107">成員</span><span class="sxs-lookup"><span data-stu-id="115f2-107">Members</span></span>



| <span data-ttu-id="115f2-108">member</span><span class="sxs-lookup"><span data-stu-id="115f2-108">Member</span></span>                                                | <span data-ttu-id="115f2-109">描述</span><span class="sxs-lookup"><span data-stu-id="115f2-109">Description</span></span>                                                                                                                                 | <span data-ttu-id="115f2-110">值</span><span class="sxs-lookup"><span data-stu-id="115f2-110">Value</span></span> |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="115f2-111">**CAPICOM \_ 憑證 \_ 尋找 \_ SHA1 \_ 雜湊**</span><span class="sxs-lookup"><span data-stu-id="115f2-111">**CAPICOM\_CERTIFICATE\_FIND\_SHA1\_HASH**</span></span>            | <span data-ttu-id="115f2-112">傳回符合指定之 SHA1 雜湊的憑證。</span><span class="sxs-lookup"><span data-stu-id="115f2-112">Returns certificates matching a specified SHA1 hash.</span></span><br/>                                                                             | <span data-ttu-id="115f2-113">0</span><span class="sxs-lookup"><span data-stu-id="115f2-113">0</span></span>     |
| <span data-ttu-id="115f2-114">**CAPICOM \_ 憑證 \_ 尋找 \_ 主體 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="115f2-114">**CAPICOM\_CERTIFICATE\_FIND\_SUBJECT\_NAME**</span></span>         | <span data-ttu-id="115f2-115">傳回主體名稱完全或部分符合指定主體名稱的憑證。</span><span class="sxs-lookup"><span data-stu-id="115f2-115">Returns certificates whose subject name exactly or partially matches a specified subject name.</span></span><br/>                                   | <span data-ttu-id="115f2-116">1</span><span class="sxs-lookup"><span data-stu-id="115f2-116">1</span></span>     |
| <span data-ttu-id="115f2-117">**CAPICOM \_ 憑證 \_ 尋找 \_ 簽發者 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="115f2-117">**CAPICOM\_CERTIFICATE\_FIND\_ISSUER\_NAME**</span></span>          | <span data-ttu-id="115f2-118">傳回簽發者名稱完全或部分符合指定簽發者名稱的憑證。</span><span class="sxs-lookup"><span data-stu-id="115f2-118">Returns certificates whose issuer name exactly or partially matches a specified issuer name.</span></span><br/>                                     | <span data-ttu-id="115f2-119">2</span><span class="sxs-lookup"><span data-stu-id="115f2-119">2</span></span>     |
| <span data-ttu-id="115f2-120">**CAPICOM \_ 憑證 \_ 尋找 \_ 根 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="115f2-120">**CAPICOM\_CERTIFICATE\_FIND\_ROOT\_NAME**</span></span>            | <span data-ttu-id="115f2-121">傳回根主體名稱完全或部分符合指定之根主體名稱的憑證。</span><span class="sxs-lookup"><span data-stu-id="115f2-121">Returns certificates whose root subject name exactly or partially matches a specified root subject name.</span></span><br/>                         | <span data-ttu-id="115f2-122">3</span><span class="sxs-lookup"><span data-stu-id="115f2-122">3</span></span>     |
| <span data-ttu-id="115f2-123">**CAPICOM \_ 憑證 \_ 尋找 \_ 範本 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="115f2-123">**CAPICOM\_CERTIFICATE\_FIND\_TEMPLATE\_NAME**</span></span>        | <span data-ttu-id="115f2-124">傳回範本名稱符合指定範本名稱的憑證。</span><span class="sxs-lookup"><span data-stu-id="115f2-124">Returns certificates whose template name matches a specified template name.</span></span><br/>                                                      | <span data-ttu-id="115f2-125">4</span><span class="sxs-lookup"><span data-stu-id="115f2-125">4</span></span>     |
| <span data-ttu-id="115f2-126">**CAPICOM \_ 憑證 \_ 尋找 \_ 延伸模組**</span><span class="sxs-lookup"><span data-stu-id="115f2-126">**CAPICOM\_CERTIFICATE\_FIND\_EXTENSION**</span></span>             | <span data-ttu-id="115f2-127">傳回副檔名符合指定副檔名的憑證。</span><span class="sxs-lookup"><span data-stu-id="115f2-127">Returns certificates that have an extension that matches a specified extension.</span></span><br/>                                                  | <span data-ttu-id="115f2-128">5</span><span class="sxs-lookup"><span data-stu-id="115f2-128">5</span></span>     |
| <span data-ttu-id="115f2-129">**CAPICOM \_ 憑證 \_ 尋找 \_ 擴充 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="115f2-129">**CAPICOM\_CERTIFICATE\_FIND\_EXTENDED\_PROPERTY**</span></span>    | <span data-ttu-id="115f2-130">傳回具有擴充屬性的憑證，其屬性識別碼符合指定的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="115f2-130">Returns certificates that have an extended property whose property identifier matches a specified property identifier.</span></span><br/>           | <span data-ttu-id="115f2-131">6</span><span class="sxs-lookup"><span data-stu-id="115f2-131">6</span></span>     |
| <span data-ttu-id="115f2-132">**CAPICOM \_ 憑證 \_ 尋找 \_ 應用程式 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="115f2-132">**CAPICOM\_CERTIFICATE\_FIND\_APPLICATION\_POLICY**</span></span>   | <span data-ttu-id="115f2-133">傳回存放區中的憑證，其中包含增強金鑰使用方法擴充功能或屬性（property）與使用識別碼合併。</span><span class="sxs-lookup"><span data-stu-id="115f2-133">Returns certificates in the store that have either an enhanced key usage extension or property combined with a usage identifier.</span></span><br/> | <span data-ttu-id="115f2-134">7</span><span class="sxs-lookup"><span data-stu-id="115f2-134">7</span></span>     |
| <span data-ttu-id="115f2-135">**CAPICOM \_ 憑證 \_ 尋找 \_ 憑證 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="115f2-135">**CAPICOM\_CERTIFICATE\_FIND\_CERTIFICATE\_POLICY**</span></span>   | <span data-ttu-id="115f2-136">傳回包含指定之原則 OID 的憑證。</span><span class="sxs-lookup"><span data-stu-id="115f2-136">Returns certificates containing a specified policy OID.</span></span><br/>                                                                          | <span data-ttu-id="115f2-137">8</span><span class="sxs-lookup"><span data-stu-id="115f2-137">8</span></span>     |
| <span data-ttu-id="115f2-138">**CAPICOM \_ 憑證 \_ 尋找 \_ 時間 \_ 有效**</span><span class="sxs-lookup"><span data-stu-id="115f2-138">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_VALID**</span></span>           | <span data-ttu-id="115f2-139">傳回時間有效的憑證。</span><span class="sxs-lookup"><span data-stu-id="115f2-139">Returns certificates whose time is valid.</span></span><br/>                                                                                        | <span data-ttu-id="115f2-140">9</span><span class="sxs-lookup"><span data-stu-id="115f2-140">9</span></span>     |
| <span data-ttu-id="115f2-141">**CAPICOM \_ 憑證 \_ 尋找 \_ 時間 \_ 尚未 \_ \_ 生效**</span><span class="sxs-lookup"><span data-stu-id="115f2-141">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_NOT\_YET\_VALID**</span></span> | <span data-ttu-id="115f2-142">傳回時間尚未生效的憑證。</span><span class="sxs-lookup"><span data-stu-id="115f2-142">Returns certificates whose time is not yet valid.</span></span><br/>                                                                                | <span data-ttu-id="115f2-143">10</span><span class="sxs-lookup"><span data-stu-id="115f2-143">10</span></span>    |
| <span data-ttu-id="115f2-144">**CAPICOM \_ 憑證 \_ 尋找 \_ 時間已 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="115f2-144">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_EXPIRED**</span></span>         | <span data-ttu-id="115f2-145">傳回時間已過期的憑證。</span><span class="sxs-lookup"><span data-stu-id="115f2-145">Returns certificates whose time has expired.</span></span><br/>                                                                                     | <span data-ttu-id="115f2-146">11</span><span class="sxs-lookup"><span data-stu-id="115f2-146">11</span></span>    |
| <span data-ttu-id="115f2-147">**CAPICOM \_ 憑證 \_ 尋找 \_ 金鑰 \_ 使用方式**</span><span class="sxs-lookup"><span data-stu-id="115f2-147">**CAPICOM\_CERTIFICATE\_FIND\_KEY\_USAGE**</span></span>            | <span data-ttu-id="115f2-148">傳回包含金鑰的憑證，可使用指定的方式來使用。</span><span class="sxs-lookup"><span data-stu-id="115f2-148">Returns certificates containing a key that can be used in the specified manner.</span></span><br/>                                                  | <span data-ttu-id="115f2-149">12</span><span class="sxs-lookup"><span data-stu-id="115f2-149">12</span></span>    |



## <a name="remarks"></a><span data-ttu-id="115f2-150">備註</span><span class="sxs-lookup"><span data-stu-id="115f2-150">Remarks</span></span>

<span data-ttu-id="115f2-151">**CAPICOM \_ 憑證 \_ 尋找 \_ 類型** 列舉類型是由 certificate [**. find**](certificates-find.md)方法所使用。</span><span class="sxs-lookup"><span data-stu-id="115f2-151">The **CAPICOM\_CERTIFICATE\_FIND\_TYPE** enumeration type is used by the [**Certificates.Find**](certificates-find.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="115f2-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="115f2-152">Requirements</span></span>



| <span data-ttu-id="115f2-153">需求</span><span class="sxs-lookup"><span data-stu-id="115f2-153">Requirement</span></span> | <span data-ttu-id="115f2-154">值</span><span class="sxs-lookup"><span data-stu-id="115f2-154">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="115f2-155">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="115f2-155">Redistributable</span></span><br/> | <span data-ttu-id="115f2-156">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="115f2-156">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="115f2-157">標頭</span><span class="sxs-lookup"><span data-stu-id="115f2-157">Header</span></span><br/>          | <dl> <span data-ttu-id="115f2-158"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="115f2-158"><dt>Capicom.h</dt></span></span> </dl> |



 

 




