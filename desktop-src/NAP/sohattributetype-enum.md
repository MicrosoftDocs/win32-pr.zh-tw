---
title: 'SoHAttributeType 列舉 (NapProtocol) '
description: 指定屬性類型―長度―值 (TLV) 物件中儲存的屬性類型。
ms.assetid: ba725bf1-1d0a-4489-b912-3e761557d772
keywords:
- SoHAttributeType 列舉 NAP
topic_type:
- apiref
api_name:
- SoHAttributeType
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db164bbedf2267aaa5941a21a56ccfd53e1e1646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317372"
---
# <a name="sohattributetype-enumeration"></a><span data-ttu-id="8c453-104">SoHAttributeType 列舉</span><span class="sxs-lookup"><span data-stu-id="8c453-104">SoHAttributeType enumeration</span></span>

> [!Note]  
> <span data-ttu-id="8c453-105">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="8c453-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8c453-106">**SoHAttributeType** 列舉會指定屬性類型―長度―值 (TLV) 物件中所儲存的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="8c453-106">The **SoHAttributeType** enumeration specifies the type of attribute stored in the attribute type-length-value (TLV) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c453-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c453-107">Syntax</span></span>


```C++
typedef enum tagSoHAttributeType { 
  sohAttributeTypeSystemHealthId          = 2,
  sohAttributeTypeIpv4FixupServers        = 3,
  sohAttributeTypeComplianceResultCodes   = 4,
  sohAttributeTypeTimeOfLastUpdate        = 5,
  sohAttributeTypeClientId                = 6,
  sohAttributeTypeVendorSpecific          = 7,
  sohAttributeTypeHealthClass             = 8,
  sohAttributeTypeSoftwareVersion         = 9,
  sohAttributeTypeProductName             = 10,
  sohAttributeTypeHealthClassStatus       = 11,
  sohAttributeTypeSoHGenerationTime       = 12,
  sohAttributeTypeErrorCodes              = 13,
  sohAttributeTypeFailureCategory         = 14,
  sohAttributeTypeIpv6FixupServers        = 15,
  sohAttributeTypeExtendedIsolationState  = 16
} SoHAttributeType;
```



## <a name="constants"></a><span data-ttu-id="8c453-108">常數</span><span class="sxs-lookup"><span data-stu-id="8c453-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8c453-109"><span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**sohAttributeTypeSystemHealthId**</span><span class="sxs-lookup"><span data-stu-id="8c453-109"><span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**sohAttributeTypeSystemHealthId**</span></span>
</dt> <dd>

<span data-ttu-id="8c453-110">指定系統健全狀況識別碼屬性類型。</span><span class="sxs-lookup"><span data-stu-id="8c453-110">Specifies the system health ID attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="8c453-111"><span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**</span><span class="sxs-lookup"><span data-stu-id="8c453-111"><span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**</span></span>
</dt> <dd>

<span data-ttu-id="8c453-112">指定 IPv4 修正伺服器屬性類型。</span><span class="sxs-lookup"><span data-stu-id="8c453-112">Specifies the IPv4 fix-up server attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="8c453-113"><span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**sohAttributeTypeComplianceResultCodes**</span><span class="sxs-lookup"><span data-stu-id="8c453-113"><span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**sohAttributeTypeComplianceResultCodes**</span></span>
</dt> <dd>

<span data-ttu-id="8c453-114">指定相容性結果碼屬性類型。</span><span class="sxs-lookup"><span data-stu-id="8c453-114">Specifies the compliance result code attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="8c453-115"><span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**sohAttributeTypeTimeOfLastUpdate**</span><span class="sxs-lookup"><span data-stu-id="8c453-115"><span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**sohAttributeTypeTimeOfLastUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="8c453-116">指定上一次更新屬性類型的時間。</span><span class="sxs-lookup"><span data-stu-id="8c453-116">Specifies the time of the last update attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="8c453-117"><span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**sohAttributeTypeClientId**</span><span class="sxs-lookup"><span data-stu-id="8c453-117"><span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**sohAttributeTypeClientId**</span></span>
</dt> <dd>

<span data-ttu-id="8c453-118">指定用戶端識別碼屬性類型。</span><span class="sxs-lookup"><span data-stu-id="8c453-118">Specifies the client ID attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="8c453-119"><span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**sohAttributeTypeVendorSpecific**</span><span class="sxs-lookup"><span data-stu-id="8c453-119"><span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**sohAttributeTypeVendorSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="8c453-120">指定廠商特定的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="8c453-120">Specifies the vendor-specific attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="8c453-121"><span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**sohAttributeTypeHealthClass**</span><span class="sxs-lookup"><span data-stu-id="8c453-121"><span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**sohAttributeTypeHealthClass**</span></span>
</dt> <dd>

<span data-ttu-id="8c453-122">指定健全狀況類別屬性類型。</span><span class="sxs-lookup"><span data-stu-id="8c453-122">Specifies the health class attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="8c453-123"><span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**sohAttributeTypeSoftwareVersion**</span><span class="sxs-lookup"><span data-stu-id="8c453-123"><span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**sohAttributeTypeSoftwareVersion**</span></span>
</dt> <dd>

<span data-ttu-id="8c453-124">指定軟體版本屬性類型。</span><span class="sxs-lookup"><span data-stu-id="8c453-124">Specifies the software version attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="8c453-125"><span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**sohAttributeTypeProductName**</span><span class="sxs-lookup"><span data-stu-id="8c453-125"><span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**sohAttributeTypeProductName**</span></span>
</dt> <dd>

<span data-ttu-id="8c453-126">指定產品名稱的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="8c453-126">Specifies the product name attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="8c453-127"><span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**sohAttributeTypeHealthClassStatus**</span><span class="sxs-lookup"><span data-stu-id="8c453-127"><span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**sohAttributeTypeHealthClassStatus**</span></span>
</dt> <dd>

<span data-ttu-id="8c453-128">指定健全狀況類別狀態屬性類型。</span><span class="sxs-lookup"><span data-stu-id="8c453-128">Specifies the health class status attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="8c453-129"><span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**sohAttributeTypeSoHGenerationTime**</span><span class="sxs-lookup"><span data-stu-id="8c453-129"><span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**sohAttributeTypeSoHGenerationTime**</span></span>
</dt> <dd>

<span data-ttu-id="8c453-130">指定健全狀況屬性類型之語句的產生時間。</span><span class="sxs-lookup"><span data-stu-id="8c453-130">Specifies the generation time of the Statement of Health attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="8c453-131"><span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**sohAttributeTypeErrorCodes**</span><span class="sxs-lookup"><span data-stu-id="8c453-131"><span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**sohAttributeTypeErrorCodes**</span></span>
</dt> <dd>

<span data-ttu-id="8c453-132">指定錯誤碼屬性類型。</span><span class="sxs-lookup"><span data-stu-id="8c453-132">Specifies the error code attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="8c453-133"><span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**sohAttributeTypeFailureCategory**</span><span class="sxs-lookup"><span data-stu-id="8c453-133"><span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**sohAttributeTypeFailureCategory**</span></span>
</dt> <dd>

<span data-ttu-id="8c453-134">指定失敗分類的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="8c453-134">Specifies the failure category attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="8c453-135"><span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**</span><span class="sxs-lookup"><span data-stu-id="8c453-135"><span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**</span></span>
</dt> <dd>

<span data-ttu-id="8c453-136">指定 IPv6 的修正伺服器屬性類型。</span><span class="sxs-lookup"><span data-stu-id="8c453-136">Specifies the IPv6 fix-up server attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="8c453-137"><span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**sohAttributeTypeExtendedIsolationState**</span><span class="sxs-lookup"><span data-stu-id="8c453-137"><span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**sohAttributeTypeExtendedIsolationState**</span></span>
</dt> <dd>

<span data-ttu-id="8c453-138">指定擴充隔離狀態屬性類型。</span><span class="sxs-lookup"><span data-stu-id="8c453-138">Specifies the extended isolation state attribute type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c453-139">備註</span><span class="sxs-lookup"><span data-stu-id="8c453-139">Remarks</span></span>

<span data-ttu-id="8c453-140">[**SoHAttributeValue**](sohattributevalue-union.md)結構會定義對應至每個屬性類型的屬性值。</span><span class="sxs-lookup"><span data-stu-id="8c453-140">The [**SoHAttributeValue**](sohattributevalue-union.md) structure defines the attribute values that correspond to each attribute type.</span></span>

<span data-ttu-id="8c453-141">NAP 系統會使用這些屬性類型：</span><span class="sxs-lookup"><span data-stu-id="8c453-141">These attribute types are consumed by the NAP system:</span></span>

-   <span data-ttu-id="8c453-142">sohAttributeTypeSystemHealthId</span><span class="sxs-lookup"><span data-stu-id="8c453-142">sohAttributeTypeSystemHealthId</span></span>
-   <span data-ttu-id="8c453-143">sohAttributeTypeIpv4FixupServers</span><span class="sxs-lookup"><span data-stu-id="8c453-143">sohAttributeTypeIpv4FixupServers</span></span>
-   <span data-ttu-id="8c453-144">sohAttributeTypeIpv6FixupServers</span><span class="sxs-lookup"><span data-stu-id="8c453-144">sohAttributeTypeIpv6FixupServers</span></span>
-   <span data-ttu-id="8c453-145">sohAttributeTypeComplianceResultCodes</span><span class="sxs-lookup"><span data-stu-id="8c453-145">sohAttributeTypeComplianceResultCodes</span></span>
-   <span data-ttu-id="8c453-146">sohAttributeTypeFailureCategory</span><span class="sxs-lookup"><span data-stu-id="8c453-146">sohAttributeTypeFailureCategory</span></span>

<span data-ttu-id="8c453-147">其餘的型別只是為了引導 Sha 和 Shv 的使用方式。</span><span class="sxs-lookup"><span data-stu-id="8c453-147">The rest of the types are only intended to guide the usage by SHAs and SHVs.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c453-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c453-148">Requirements</span></span>



| <span data-ttu-id="8c453-149">需求</span><span class="sxs-lookup"><span data-stu-id="8c453-149">Requirement</span></span> | <span data-ttu-id="8c453-150">值</span><span class="sxs-lookup"><span data-stu-id="8c453-150">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c453-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c453-151">Minimum supported client</span></span><br/> | <span data-ttu-id="8c453-152">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c453-152">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8c453-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c453-153">Minimum supported server</span></span><br/> | <span data-ttu-id="8c453-154">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c453-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8c453-155">標頭</span><span class="sxs-lookup"><span data-stu-id="8c453-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c453-156"><dt>NapProtocol。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c453-156"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c453-157">Idl</span><span class="sxs-lookup"><span data-stu-id="8c453-157">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8c453-158"><dt>NapProtocol .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8c453-158"><dt>NapProtocol.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c453-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c453-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c453-160">**SoHAttributeValue**</span><span class="sxs-lookup"><span data-stu-id="8c453-160">**SoHAttributeValue**</span></span>](sohattributevalue-union.md)
</dt> <dt>

[<span data-ttu-id="8c453-161">**SoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="8c453-161">**SoHAttribute**</span></span>](/windows/win32/api/naptypes/ns-naptypes-sohattribute)
</dt> <dt>

[<span data-ttu-id="8c453-162">**SoH**</span><span class="sxs-lookup"><span data-stu-id="8c453-162">**SoH**</span></span>](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> <dt>

[<span data-ttu-id="8c453-163">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="8c453-163">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> <dt>

[<span data-ttu-id="8c453-164">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="8c453-164">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





