---
title: 'SoHAttributeValue 聯集 (NapProtocol .h) '
description: 在 SoHAttribute 結構中定義型別成員的內容。
ms.assetid: 53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12
keywords:
- SoHAttributeValue 聯集 NAP
topic_type:
- apiref
api_name:
- SoHAttributeValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36660e4e360ff0df31bb3a76d06c50e5d366c894
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466457"
---
# <a name="sohattributevalue-union"></a><span data-ttu-id="6671d-104">SoHAttributeValue 聯集</span><span class="sxs-lookup"><span data-stu-id="6671d-104">SoHAttributeValue union</span></span>

> [!Note]  
> <span data-ttu-id="6671d-105">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="6671d-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6671d-106">**SoHAttributeValue** 聯集會在 [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)結構中定義 **型** 別成員的內容。</span><span class="sxs-lookup"><span data-stu-id="6671d-106">The **SoHAttributeValue** union defines the contents of the **type** member in a [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) structure.</span></span> <span data-ttu-id="6671d-107">**SoHAttributeValue** 聯集的結構取決於 [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)結構的 **型** 別成員中指定的 [**SoHAttributeType**](sohattributetype-enum.md) 。</span><span class="sxs-lookup"><span data-stu-id="6671d-107">The structure of the **SoHAttributeValue** union is determined by the [**SoHAttributeType**](sohattributetype-enum.md) specified in the **type** member of the [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6671d-108">語法</span><span class="sxs-lookup"><span data-stu-id="6671d-108">Syntax</span></span>


```C++
typedef union tagSoHAttributeValue {
  SystemHealthEntityId     idVal;
  struct tagIpv4Addresses {
    UINT16      count;
    Ipv4Address *addresses;
  } v4AddressesVal;
  struct tagIpv6Addresses {
    UINT16      count;
    Ipv6Address *addresses;
  } v6AddressesVal;
  ResultCodes              codesVal;
  FILETIME                 dateTimeVal;
  struct tagVendorSpecific {
    UINT32 vendorId;
    UINT16 size;
    BYTE   *vendorSpecificData;
  } vendorSpecificVal;
  UINT8                    uint8Val;
  struct tagOctetString {
    UINT16 size;
    BYTE   *data;
  } octetStringVal;
} SoHAttributeValue;
```



## <a name="members"></a><span data-ttu-id="6671d-109">成員</span><span class="sxs-lookup"><span data-stu-id="6671d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="6671d-110">**idVal**</span><span class="sxs-lookup"><span data-stu-id="6671d-110">**idVal**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-111">**案例 (sohAttributeTypeSystemHealthId)**</span><span class="sxs-lookup"><span data-stu-id="6671d-111">**case(sohAttributeTypeSystemHealthId)**</span></span>

<span data-ttu-id="6671d-112">包含系統健康狀態代理程式識別碼的唯一 [SystemHealthEntityId](nap-datatypes.md) ， (SHA) 或系統健康狀態驗證， (建立此 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包的 SHV) 。</span><span class="sxs-lookup"><span data-stu-id="6671d-112">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the System Health Agent (SHA) or System Health Validator (SHV) that constructed this [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="6671d-113">**v4AddressesVal**</span><span class="sxs-lookup"><span data-stu-id="6671d-113">**v4AddressesVal**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-114">**案例 (sohAttributeTypeIpv4FixupServers)**</span><span class="sxs-lookup"><span data-stu-id="6671d-114">**case(sohAttributeTypeIpv4FixupServers)**</span></span>

<span data-ttu-id="6671d-115">NAP 系統正在使用的修正伺服器的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="6671d-115">The IPv4 addresses of the fix-up servers in use by the NAP system.</span></span>

<dl> <dt>

<span data-ttu-id="6671d-116">**計數**</span><span class="sxs-lookup"><span data-stu-id="6671d-116">**count**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-117">介於1到 [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md)的 **位址** 成員中的 IPv4 位址數目。</span><span class="sxs-lookup"><span data-stu-id="6671d-117">The number of IPv4 addresses in the **addresses** member in the range 1 to [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6671d-118">**位址**</span><span class="sxs-lookup"><span data-stu-id="6671d-118">**addresses**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-119">[**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address)結構的陣列，其中包含 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="6671d-119">An array of [**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) structures that contain the IPv4 addresses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6671d-120">**v6AddressesVal**</span><span class="sxs-lookup"><span data-stu-id="6671d-120">**v6AddressesVal**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-121">**案例 (sohAttributeTypeIpv6FixupServers)**</span><span class="sxs-lookup"><span data-stu-id="6671d-121">**case(sohAttributeTypeIpv6FixupServers)**</span></span>

<span data-ttu-id="6671d-122">NAP 系統正在使用的修正伺服器 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="6671d-122">The IPv6 addresses of the fix-up servers in use by the NAP system.</span></span>

<dl> <dt>

<span data-ttu-id="6671d-123">**計數**</span><span class="sxs-lookup"><span data-stu-id="6671d-123">**count**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-124">介於1到 [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md)的 **位址** 成員中的 IPv4 位址數目。</span><span class="sxs-lookup"><span data-stu-id="6671d-124">The number of IPv4 addresses in the **addresses** member in the range 1 to [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6671d-125">**位址**</span><span class="sxs-lookup"><span data-stu-id="6671d-125">**addresses**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-126">[**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address)結構的陣列，其中包含 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="6671d-126">An array of [**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) structures that contain the IPv4 addresses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6671d-127">**codesVal**</span><span class="sxs-lookup"><span data-stu-id="6671d-127">**codesVal**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-128">**案例 (sohAttributeTypeComplianceResultCodes、sohAttributeTypeErrorCodes)**</span><span class="sxs-lookup"><span data-stu-id="6671d-128">**case(sohAttributeTypeComplianceResultCodes, sohAttributeTypeErrorCodes)**</span></span>

<span data-ttu-id="6671d-129">[**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes)結構，其中包含應用程式定義的用戶端或 [**NAP 錯誤常數**](nap-error-constants.md)的合規性結果碼。</span><span class="sxs-lookup"><span data-stu-id="6671d-129">A [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) structure that contains either the application defined compliance result codes of the client or [**NAP error constants**](nap-error-constants.md).</span></span> <span data-ttu-id="6671d-130">[**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)封包必須包含此 Tlv 或 **sohAttributeTypeFailureCategory** 的 tlv。</span><span class="sxs-lookup"><span data-stu-id="6671d-130">An [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet must contain this TLV or the **sohAttributeTypeFailureCategory** TLV.</span></span>

</dd> <dt>

<span data-ttu-id="6671d-131">**dateTimeVal**</span><span class="sxs-lookup"><span data-stu-id="6671d-131">**dateTimeVal**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-132">**案例 (sohAttributeTypeTimeOfLastUpdate、sohAttributeTypeSoHGenerationTime)**</span><span class="sxs-lookup"><span data-stu-id="6671d-132">**case(sohAttributeTypeTimeOfLastUpdate, sohAttributeTypeSoHGenerationTime)**</span></span>

<span data-ttu-id="6671d-133">[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)結構，其中包含上次 [**Soh**](/windows/win32/api/naptypes/ns-naptypes-soh)更新或 **SoH** 產生時間的時間。</span><span class="sxs-lookup"><span data-stu-id="6671d-133">A [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains the time of the last [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) update or the **SoH** generation time.</span></span>

</dd> <dt>

<span data-ttu-id="6671d-134">**vendorSpecificVal**</span><span class="sxs-lookup"><span data-stu-id="6671d-134">**vendorSpecificVal**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-135">**案例 (sohAttributeTypeVendorSpecific)**</span><span class="sxs-lookup"><span data-stu-id="6671d-135">**case(sohAttributeTypeVendorSpecific)**</span></span>

<span data-ttu-id="6671d-136">由廠商定義的應用程式特定資料。</span><span class="sxs-lookup"><span data-stu-id="6671d-136">Application-specific data that is defined by the vendor.</span></span>

<dl> <dt>

<span data-ttu-id="6671d-137">**vendorId**</span><span class="sxs-lookup"><span data-stu-id="6671d-137">**vendorId**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-138">4位元組的識別碼，定義 SHA/SHV 配對識別碼。</span><span class="sxs-lookup"><span data-stu-id="6671d-138">A 4-byte identifier that defines the SHA/SHV pair ID.</span></span> <span data-ttu-id="6671d-139">前3個位元組是供應商的 IETF 指派 SMI-S 碼，最後一個位元組會識別元件本身。</span><span class="sxs-lookup"><span data-stu-id="6671d-139">The first 3 bytes are the IETF-assigned SMI code of the vendor, and the last byte identifies the component itself.</span></span> <span data-ttu-id="6671d-140">在執行 SHA 或 SHV 時，請勿使用指派給 [**NAP 廠商常數**](nap-vendor-constants.md)上內部 Microsoft 系統健康情況元件的識別碼值。</span><span class="sxs-lookup"><span data-stu-id="6671d-140">When implementing a SHA or SHV, do not use the ID values assigned to internal Microsoft system health components on [**NAP vendor constants**](nap-vendor-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6671d-141">**size**</span><span class="sxs-lookup"><span data-stu-id="6671d-141">**size**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-142">從0到 ([**maxSoHAttributeSize**](nap-type-constants.md) -4) 範圍中廠商資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6671d-142">The size, in bytes, of the vendor data in the range 0 to ([**maxSoHAttributeSize**](nap-type-constants.md) - 4).</span></span>

</dd> <dt>

<span data-ttu-id="6671d-143">**vendorSpecificData**</span><span class="sxs-lookup"><span data-stu-id="6671d-143">**vendorSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-144">以網路位元組順序排列之廠商特定資料的指標。</span><span class="sxs-lookup"><span data-stu-id="6671d-144">A pointer to the vendor specific data in network byte order.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6671d-145">**uint8Val**</span><span class="sxs-lookup"><span data-stu-id="6671d-145">**uint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-146">**案例 (sohAttributeTypeHealthClass、sohAttributeTypeFailureCategory、sohAttributeTypeExtendedIsolationState)**</span><span class="sxs-lookup"><span data-stu-id="6671d-146">**case(sohAttributeTypeHealthClass, sohAttributeTypeFailureCategory,sohAttributeTypeExtendedIsolationState)**</span></span>

<span data-ttu-id="6671d-147">NAP 元件的健全狀況類別、失敗類別或擴充隔離狀態，表示為 [**HealthClassValue**](healthclassvalue-enum.md) 或 [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) 值，或 [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) 結構。</span><span class="sxs-lookup"><span data-stu-id="6671d-147">The health class, failure category, or extended isolation state of a NAP component as either a [**HealthClassValue**](healthclassvalue-enum.md) or [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) value, or a [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6671d-148">**octetStringVal**</span><span class="sxs-lookup"><span data-stu-id="6671d-148">**octetStringVal**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-149">**預設值**</span><span class="sxs-lookup"><span data-stu-id="6671d-149">**default**</span></span>

<span data-ttu-id="6671d-150">下列屬性的值是八位字串：</span><span class="sxs-lookup"><span data-stu-id="6671d-150">The following attributes' values are octet strings:</span></span>

-   <span data-ttu-id="6671d-151">sohAttributeTypeSoftwareVersion</span><span class="sxs-lookup"><span data-stu-id="6671d-151">sohAttributeTypeSoftwareVersion</span></span>
-   <span data-ttu-id="6671d-152">sohAttributeTypeClientId</span><span class="sxs-lookup"><span data-stu-id="6671d-152">sohAttributeTypeClientId</span></span>
-   <span data-ttu-id="6671d-153">sohAttributeTypeProductName</span><span class="sxs-lookup"><span data-stu-id="6671d-153">sohAttributeTypeProductName</span></span>
-   <span data-ttu-id="6671d-154">sohAttributeTypeHealthClassStatus</span><span class="sxs-lookup"><span data-stu-id="6671d-154">sohAttributeTypeHealthClassStatus</span></span>

<span data-ttu-id="6671d-155">基於向前相容性，所有無法辨識的屬性都會以八位字串的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="6671d-155">For forward compatibility, all unrecognized attributes are returned as octet strings.</span></span> <span data-ttu-id="6671d-156">**資料** 必須以網路位元組順序排序。</span><span class="sxs-lookup"><span data-stu-id="6671d-156">**data** must be in network byte order.</span></span>

<dl> <dt>

<span data-ttu-id="6671d-157">**size**</span><span class="sxs-lookup"><span data-stu-id="6671d-157">**size**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-158">範圍0到 [**maxSoHAttributeSize**](nap-type-constants.md)的 **資料** 大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6671d-158">The size, in bytes, of **data** in the range 0 to [**maxSoHAttributeSize**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6671d-159">**data**</span><span class="sxs-lookup"><span data-stu-id="6671d-159">**data**</span></span>
</dt> <dd>

<span data-ttu-id="6671d-160">八位字串值的指標。</span><span class="sxs-lookup"><span data-stu-id="6671d-160">A pointer to the octet string value.</span></span>

</dd> </dl> </dd> </dl>

## <a name="actual-data-layout"></a><span data-ttu-id="6671d-161">實際資料版面配置</span><span class="sxs-lookup"><span data-stu-id="6671d-161">Actual data layout</span></span>

<span data-ttu-id="6671d-162">由於 SDK 發行環境的本質，在語法區塊中不會清楚地表示等位。</span><span class="sxs-lookup"><span data-stu-id="6671d-162">Due to the nature of the SDK publishing environment, unions are not clearly represented in syntax blocks.</span></span> <span data-ttu-id="6671d-163">以下是 NapProtocol .h 標頭檔中的實際語法。</span><span class="sxs-lookup"><span data-stu-id="6671d-163">Here is the actual syntax from the NapProtocol.h header file.</span></span>


```C++
#include <windows.h>

typedef [switch_type(SoHAttributeType)] 
   union tagSoHAttributeValue
   {
      [case(sohAttributeTypeSystemHealthId)]
         SystemHealthEntityId idVal;
   
      [case(sohAttributeTypeIpv4FixupServers)]
         struct tagIpv4Addresses
         {
            [range(1, maxIpv4CountPerSoHAttribute)] 
               UINT16 count;
            [size_is(count)] Ipv4Address* addresses;
         } v4AddressesVal;

      [case(sohAttributeTypeIpv6FixupServers)]
         struct tagIpv6Addresses
         {
            [range(1, maxIpv6CountPerSoHAttribute)]
               UINT16 count;
            [size_is(count)] Ipv6Address* addresses;
         } v6AddressesVal;

      [case(sohAttributeTypeComplianceResultCodes, 
            sohAttributeTypeErrorCodes)]
         ResultCodes codesVal;

      [case(sohAttributeTypeTimeOfLastUpdate, 
            sohAttributeTypeSoHGenerationTime)]
         FILETIME dateTimeVal;

      [case(sohAttributeTypeVendorSpecific)]
         struct tagVendorSpecific
         {
            UINT32 vendorId;
            [range(0, maxSoHAttributeSize - 4)] 
               UINT16 size;
            [size_is(size)] BYTE* vendorSpecificData;
         } vendorSpecificVal;

      [case(sohAttributeTypeHealthClass, 
            sohAttributeTypeFailureCategory,
            sohAttributeTypeExtendedIsolationState)]
         UINT8 uint8Val;

      [default]
         struct tagOctetString
         {
            [range(0, maxSoHAttributeSize)] UINT16 size;
            [size_is(size)] BYTE* data;
         } octetStringVal;

   } SoHAttributeValue;
};
```



## <a name="remarks"></a><span data-ttu-id="6671d-164">備註</span><span class="sxs-lookup"><span data-stu-id="6671d-164">Remarks</span></span>

<span data-ttu-id="6671d-165">NAP 系統會使用這些屬性類型：</span><span class="sxs-lookup"><span data-stu-id="6671d-165">These attribute types are consumed by the NAP system:</span></span>

-   <span data-ttu-id="6671d-166">sohAttributeTypeSystemHealthId</span><span class="sxs-lookup"><span data-stu-id="6671d-166">sohAttributeTypeSystemHealthId</span></span>
-   <span data-ttu-id="6671d-167">sohAttributeTypeIpv4FixupServers</span><span class="sxs-lookup"><span data-stu-id="6671d-167">sohAttributeTypeIpv4FixupServers</span></span>
-   <span data-ttu-id="6671d-168">sohAttributeTypeIpv6FixupServers</span><span class="sxs-lookup"><span data-stu-id="6671d-168">sohAttributeTypeIpv6FixupServers</span></span>
-   <span data-ttu-id="6671d-169">sohAttributeTypeComplianceResultCodes</span><span class="sxs-lookup"><span data-stu-id="6671d-169">sohAttributeTypeComplianceResultCodes</span></span>
-   <span data-ttu-id="6671d-170">sohAttributeTypeFailureCategory</span><span class="sxs-lookup"><span data-stu-id="6671d-170">sohAttributeTypeFailureCategory</span></span>

<span data-ttu-id="6671d-171">[**SoHAttributeTypes**](sohattributetype-enum.md)的其餘部分純粹是 Sha 和 shv 使用的規範性指導方針。</span><span class="sxs-lookup"><span data-stu-id="6671d-171">The rest of the [**SoHAttributeTypes**](sohattributetype-enum.md) are meant purely as prescriptive guidance for usage by SHAs and SHVs.</span></span>

## <a name="requirements"></a><span data-ttu-id="6671d-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="6671d-172">Requirements</span></span>



| <span data-ttu-id="6671d-173">需求</span><span class="sxs-lookup"><span data-stu-id="6671d-173">Requirement</span></span> | <span data-ttu-id="6671d-174">值</span><span class="sxs-lookup"><span data-stu-id="6671d-174">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6671d-175">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6671d-175">Minimum supported client</span></span><br/> | <span data-ttu-id="6671d-176">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6671d-176">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6671d-177">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6671d-177">Minimum supported server</span></span><br/> | <span data-ttu-id="6671d-178">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6671d-178">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6671d-179">標頭</span><span class="sxs-lookup"><span data-stu-id="6671d-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="6671d-180"><dt>NapProtocol。h</dt></span><span class="sxs-lookup"><span data-stu-id="6671d-180"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="6671d-181">Idl</span><span class="sxs-lookup"><span data-stu-id="6671d-181">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6671d-182"><dt>NapProtocol .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6671d-182"><dt>NapProtocol.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6671d-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6671d-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6671d-184">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="6671d-184">NAP Reference</span></span>](nap-reference.md)
</dt> <dt>

[<span data-ttu-id="6671d-185">NAP 結構</span><span class="sxs-lookup"><span data-stu-id="6671d-185">NAP Structures</span></span>](nap-structures.md)
</dt> </dl>

 

