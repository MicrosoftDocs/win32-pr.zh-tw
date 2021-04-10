---
title: LSKeyPack 結構
description: 包含特定遠端桌面服務授權金鑰套件的相關資訊。
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- LSKeyPack 結構遠端桌面服務
- LPLSKeyPack 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b1ac1f51e66a0a3c15c33f2535bc02f1fd3528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934967"
---
# <a name="lskeypack-structure"></a><span data-ttu-id="44d79-105">LSKeyPack 結構</span><span class="sxs-lookup"><span data-stu-id="44d79-105">LSKeyPack structure</span></span>

<span data-ttu-id="44d79-106">包含特定遠端桌面服務授權金鑰套件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="44d79-106">Contains information about a specific Remote Desktop Services licensing key pack.</span></span>

> [!Note]  
> <span data-ttu-id="44d79-107">此結構未定義于任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="44d79-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="44d79-108">若要使用這個結構，您必須自行定義，如本主題所示。</span><span class="sxs-lookup"><span data-stu-id="44d79-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="44d79-109">語法</span><span class="sxs-lookup"><span data-stu-id="44d79-109">Syntax</span></span>


```C++
typedef struct _LSKeyPack {
  DWORD dwVersion;
  UCHAR ucKeyPackType;
  TCHAR szCompanyName[256];
  TCHAR szKeyPackId[256];
  TCHAR szProductName[256];
  TCHAR szProductId[256];
  TCHAR szProductDesc[256];
  WORD  wMajorVersion;
  WORD  wMinorVersion;
  DWORD dwPlatformType;
  UCHAR ucLicenseType;
  DWORD dwLanguageId;
  UCHAR ucChannelOfPurchase;
  TCHAR szBeginSerialNumber[256];
  DWORD dwTotalLicenseInKeyPack;
  DWORD dwProductFlags;
  DWORD dwKeyPackId;
  UCHAR ucKeyPackStatus;
  DWORD dwActivateDate;
  DWORD dwExpirationDate;
  DWORD dwNumberOfLicenses;
} LSKeyPack, *LPLSKeyPack;
```



## <a name="members"></a><span data-ttu-id="44d79-110">成員</span><span class="sxs-lookup"><span data-stu-id="44d79-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="44d79-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="44d79-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-112">金鑰套件的版本。</span><span class="sxs-lookup"><span data-stu-id="44d79-112">Version of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-113">**ucKeyPackType**</span><span class="sxs-lookup"><span data-stu-id="44d79-113">**ucKeyPackType**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-114">金鑰套件的類型。</span><span class="sxs-lookup"><span data-stu-id="44d79-114">Type of key pack.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-115">**szCompanyName**</span><span class="sxs-lookup"><span data-stu-id="44d79-115">**szCompanyName**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-116">簽發金鑰套件的公司名稱。</span><span class="sxs-lookup"><span data-stu-id="44d79-116">Name of the company that issued the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-117">**szKeyPackId**</span><span class="sxs-lookup"><span data-stu-id="44d79-117">**szKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-118">金鑰套件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="44d79-118">ID of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-119">**szProductName**</span><span class="sxs-lookup"><span data-stu-id="44d79-119">**szProductName**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-120">此金鑰套件所屬的產品名稱。</span><span class="sxs-lookup"><span data-stu-id="44d79-120">Name of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-121">**szProductId**</span><span class="sxs-lookup"><span data-stu-id="44d79-121">**szProductId**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-122">此金鑰套件所屬產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="44d79-122">ID of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-123">**szProductDesc**</span><span class="sxs-lookup"><span data-stu-id="44d79-123">**szProductDesc**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-124">此金鑰套件所屬產品的描述。</span><span class="sxs-lookup"><span data-stu-id="44d79-124">Description of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-125">**wMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="44d79-125">**wMajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-126">此金鑰套件所屬產品的主要版本。</span><span class="sxs-lookup"><span data-stu-id="44d79-126">Major version of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-127">**wMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="44d79-127">**wMinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-128">此金鑰套件所屬產品的次要版本。</span><span class="sxs-lookup"><span data-stu-id="44d79-128">Minor version of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-129">**dwPlatformType**</span><span class="sxs-lookup"><span data-stu-id="44d79-129">**dwPlatformType**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-130">平臺類型。</span><span class="sxs-lookup"><span data-stu-id="44d79-130">Platform type.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-131">**ucLicenseType**</span><span class="sxs-lookup"><span data-stu-id="44d79-131">**ucLicenseType**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-132">金鑰套件中的授權類型。</span><span class="sxs-lookup"><span data-stu-id="44d79-132">Type of licenses in the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-133">**dwLanguageId**</span><span class="sxs-lookup"><span data-stu-id="44d79-133">**dwLanguageId**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-134">語言識別碼。</span><span class="sxs-lookup"><span data-stu-id="44d79-134">Language ID.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-135">**ucChannelOfPurchase**</span><span class="sxs-lookup"><span data-stu-id="44d79-135">**ucChannelOfPurchase**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-136">購買通道。</span><span class="sxs-lookup"><span data-stu-id="44d79-136">Channel of purchase.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-137">**szBeginSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="44d79-137">**szBeginSerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-138">第一個授權的序號。</span><span class="sxs-lookup"><span data-stu-id="44d79-138">Serial number for the first license.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-139">**dwTotalLicenseInKeyPack**</span><span class="sxs-lookup"><span data-stu-id="44d79-139">**dwTotalLicenseInKeyPack**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-140">金鑰套件中的授權總數。</span><span class="sxs-lookup"><span data-stu-id="44d79-140">Total number of licenses in the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-141">**dwProductFlags**</span><span class="sxs-lookup"><span data-stu-id="44d79-141">**dwProductFlags**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-142">標誌。</span><span class="sxs-lookup"><span data-stu-id="44d79-142">Flags.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-143">**dwKeyPackId**</span><span class="sxs-lookup"><span data-stu-id="44d79-143">**dwKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-144">金鑰套件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="44d79-144">ID of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-145">**ucKeyPackStatus**</span><span class="sxs-lookup"><span data-stu-id="44d79-145">**ucKeyPackStatus**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-146">金鑰套件的狀態。</span><span class="sxs-lookup"><span data-stu-id="44d79-146">Status of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-147">**dwActivateDate**</span><span class="sxs-lookup"><span data-stu-id="44d79-147">**dwActivateDate**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-148">金鑰套件的啟用日期。</span><span class="sxs-lookup"><span data-stu-id="44d79-148">Activation date for the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-149">**dwExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="44d79-149">**dwExpirationDate**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-150">金鑰套件的到期日。</span><span class="sxs-lookup"><span data-stu-id="44d79-150">Expiration date for the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-151">**dwNumberOfLicenses**</span><span class="sxs-lookup"><span data-stu-id="44d79-151">**dwNumberOfLicenses**</span></span>
</dt> <dd>

<span data-ttu-id="44d79-152">授權數目。</span><span class="sxs-lookup"><span data-stu-id="44d79-152">Number of licenses.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44d79-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="44d79-153">Requirements</span></span>



| <span data-ttu-id="44d79-154">需求</span><span class="sxs-lookup"><span data-stu-id="44d79-154">Requirement</span></span> | <span data-ttu-id="44d79-155">值</span><span class="sxs-lookup"><span data-stu-id="44d79-155">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="44d79-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44d79-156">Minimum supported client</span></span><br/> | <span data-ttu-id="44d79-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44d79-157">Windows Vista</span></span><br/>       |
| <span data-ttu-id="44d79-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44d79-158">Minimum supported server</span></span><br/> | <span data-ttu-id="44d79-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44d79-159">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44d79-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44d79-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d79-161">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="44d79-161">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="44d79-162">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="44d79-162">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dt>

[<span data-ttu-id="44d79-163">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="44d79-163">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

 





