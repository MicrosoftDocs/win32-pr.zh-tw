---
description: 包含 (GRL) 標頭的全域撤銷清單。
ms.assetid: 806ae550-5106-47ec-8466-f967598d3e61
title: GRL_HEADER 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GRL_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: c20c9323ac627f9f1d6c63ae893d1633fb3cd96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973403"
---
# <a name="grl_header-structure"></a><span data-ttu-id="5c3d6-103">GRL \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="5c3d6-103">GRL\_HEADER structure</span></span>

<span data-ttu-id="5c3d6-104">包含 (GRL) 標頭的全域撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-104">Contains the global revocation list (GRL) header.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c3d6-105">語法</span><span class="sxs-lookup"><span data-stu-id="5c3d6-105">Syntax</span></span>


```C++
typedef struct _GRL_HEADER {
  WCHAR    wszIdentifier[6];
  WORD     wFormatMajor;
  WORD     wFormatMinor;
  FILETIME CreationTime;
  DWORD    dwSequenceNumber;
  DWORD    dwForceRebootVersion;
  DWORD    dwForceProcessRestartVersion;
  DWORD    cbRevocationSectionOffset;
  DWORD    cRevokedKernelBinaries;
  DWORD    cRevokedUserBinaries;
  DWORD    cRevokedCertificates;
  DWORD    cTrustedRoots;
  DWORD    cbExtensibleSectionOffset;
  DWORD    cExtensibleEntries;
  DWORD    cbRenewalSectionOffset;
  DWORD    cRevokedKernelBinaryRenewals;
  DWORD    cRevokedUserBinaryRenewals;
  DWORD    cRevokedCertificateRenewals;
  DWORD    cbSignatureCoreOffset;
  DWORD    cbSignatureExtOffset;
} GRL_HEADER;
```



## <a name="members"></a><span data-ttu-id="5c3d6-106">成員</span><span class="sxs-lookup"><span data-stu-id="5c3d6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5c3d6-107">**wszIdentifier**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-107">**wszIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-108">GRL 識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-108">The GRL identifier.</span></span> <span data-ttu-id="5c3d6-109">此值一律為 L "MSGRL"。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-109">The value is always L"MSGRL".</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-110">**wFormatMajor**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-110">**wFormatMajor**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-111">主要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-111">The major version number.</span></span> <span data-ttu-id="5c3d6-112">此值目前必須為1。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-112">Currently the value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-113">**wFormatMinor**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-113">**wFormatMinor**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-114">次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-114">The minor version number.</span></span> <span data-ttu-id="5c3d6-115">此值目前必須為零。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-115">Currently the value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-116">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-116">**CreationTime**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-117">指定檔案建立時間的 **FILETIME** 值。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-117">A **FILETIME** value that specifies when the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-118">**dwSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-118">**dwSequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-119">GRL 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-119">The GRL version number.</span></span> <span data-ttu-id="5c3d6-120">值目前必須至少為3</span><span class="sxs-lookup"><span data-stu-id="5c3d6-120">Currently the value must be at least 3</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-121">**dwForceRebootVersion**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-121">**dwForceRebootVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-122">保留的。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-123">**dwForceProcessRestartVersion**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-123">**dwForceProcessRestartVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-124">保留的。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-124">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-125">**cbRevocationSectionOffset**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-125">**cbRevocationSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-126">從 GRL 開頭到核心區段的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-126">The offset, in bytes, from the start of the GRL to the Core section.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-127">**cRevokedKernelBinaries**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-127">**cRevokedKernelBinaries**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-128">在 GRL 中列出的已撤銷核心二進位檔數目。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-128">The number of revoked kernel binaries listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-129">**cRevokedUserBinaries**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-129">**cRevokedUserBinaries**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-130">在 GRL 中列出的已撤銷使用者模式二進位檔的數目。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-130">The number of revoked user-mode binaries listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-131">**cRevokedCertificates**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-131">**cRevokedCertificates**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-132">在 GRL 中列出的已撤銷憑證數目。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-132">The number of revoked certificates listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-133">**cTrustedRoots**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-133">**cTrustedRoots**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-134">在 GRL 中列出的受根信任目錄數目。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-134">The number of trusted roots listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-135">**cbExtensibleSectionOffset**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-135">**cbExtensibleSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-136">從 GRL 開頭到可擴充區段的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-136">The offset, in bytes, from the start of the GRL to the Extensible section.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-137">**cExtensibleEntries**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-137">**cExtensibleEntries**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-138">可擴充區段中的專案數。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-138">The number of entries in the Extensible section.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-139">**cbRenewalSectionOffset**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-139">**cbRenewalSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-140">從 GRL 開頭到續約區段的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-140">The offset, in bytes, from the start of the GRL to the Renewals section.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-141">**cRevokedKernelBinaryRenewals**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-141">**cRevokedKernelBinaryRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-142">在 GRL 中列出的核心二進位檔續約數目。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-142">The number of kernel binary renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-143">**cRevokedUserBinaryRenewals**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-143">**cRevokedUserBinaryRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-144">在 GRL 中列出的使用者模式二進位續約數目。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-144">The number of user-mode binary renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-145">**cRevokedCertificateRenewals**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-145">**cRevokedCertificateRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-146">在 GRL 中列出的憑證續約數目。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-146">The number of certificate renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-147">**cbSignatureCoreOffset**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-147">**cbSignatureCoreOffset**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-148">從 GRL 開頭到核心區段簽章的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-148">The offset, in bytes, from the start of the GRL to the Core section signature.</span></span>

</dd> <dt>

<span data-ttu-id="5c3d6-149">**cbSignatureExtOffset**</span><span class="sxs-lookup"><span data-stu-id="5c3d6-149">**cbSignatureExtOffset**</span></span>
</dt> <dd>

<span data-ttu-id="5c3d6-150">從 GRL 開頭到可延伸區段簽章的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-150">The offset, in bytes, from the start of the GRL to the Extensible section signature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c3d6-151">備註</span><span class="sxs-lookup"><span data-stu-id="5c3d6-151">Remarks</span></span>

<span data-ttu-id="5c3d6-152">GRL 中的所有整數都有位元組由小到小的位元組順序。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-152">All integers in the GRL have little-endian byte ordering.</span></span> <span data-ttu-id="5c3d6-153">所有結構都對齊1位元組的界限。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-153">All structures are aligned to 1-byte boundaries.</span></span>

<span data-ttu-id="5c3d6-154">SDK 標頭中未宣告此結構。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-154">This structure is not declared in an SDK header.</span></span> <span data-ttu-id="5c3d6-155">若要使用此結構，請將此處顯示的宣告新增至您的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="5c3d6-155">To use this structure, add the declaration shown here to your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c3d6-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c3d6-156">Requirements</span></span>



| <span data-ttu-id="5c3d6-157">需求</span><span class="sxs-lookup"><span data-stu-id="5c3d6-157">Requirement</span></span> | <span data-ttu-id="5c3d6-158">值</span><span class="sxs-lookup"><span data-stu-id="5c3d6-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c3d6-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c3d6-159">Minimum supported client</span></span><br/> | <span data-ttu-id="5c3d6-160">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c3d6-160">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5c3d6-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c3d6-161">Minimum supported server</span></span><br/> | <span data-ttu-id="5c3d6-162">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c3d6-162">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c3d6-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c3d6-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c3d6-164">OPM 憑證撤銷</span><span class="sxs-lookup"><span data-stu-id="5c3d6-164">OPM Certificate Revocation</span></span>](opm-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="5c3d6-165">OPM 結構</span><span class="sxs-lookup"><span data-stu-id="5c3d6-165">OPM Structures</span></span>](opm-structures.md)
</dt> </dl>

 

 




