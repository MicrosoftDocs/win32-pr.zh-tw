---
title: MDM_VPNv2_CryptographySuite03 類別
description: MDM \_ >vpnv2 \_ CryptographySuite03 類別包含原生 VPN 設定檔的密碼編譯資訊。
ms.assetid: d8d16d43-bd54-4ca8-a850-ce48390df7d6
keywords:
- MDM_VPNv2_CryptographySuite03 類別
- MDM_VPNv2_CryptographySuite03 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_CryptographySuite03
- MDM_VPNv2_CryptographySuite03.InstanceID
- MDM_VPNv2_CryptographySuite03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553f2dcddd4d7c7e0926945a80f74f6aba2a9467
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465344"
---
# <a name="mdm_vpnv2_cryptographysuite03-class"></a><span data-ttu-id="6ee12-105">MDM \_ >vpnv2 \_ CryptographySuite03 類別</span><span class="sxs-lookup"><span data-stu-id="6ee12-105">MDM\_VPNv2\_CryptographySuite03 class</span></span>

<span data-ttu-id="6ee12-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="6ee12-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6ee12-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="6ee12-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6ee12-108">**MDM \_ >vpnv2 \_ CryptographySuite03** 類別包含原生 VPN 設定檔的密碼編譯資訊。</span><span class="sxs-lookup"><span data-stu-id="6ee12-108">The **MDM\_VPNv2\_CryptographySuite03** class contains cryptography information for the native VPN profile.</span></span>

<span data-ttu-id="6ee12-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6ee12-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee12-110">語法</span><span class="sxs-lookup"><span data-stu-id="6ee12-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_CryptographySuite03
{
  string InstanceID;
  string ParentID;
  string AuthenticationTransformConstants;
  string CipherTransformConstants;
  string EncryptionMethod;
  string IntegrityCheckMethod;
  string DHGroup;
  string PfsGroup;
};
```

## <a name="members"></a><span data-ttu-id="6ee12-111">成員</span><span class="sxs-lookup"><span data-stu-id="6ee12-111">Members</span></span>

<span data-ttu-id="6ee12-112">**MDM \_ >vpnv2 \_ CryptographySuite03** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6ee12-112">The **MDM\_VPNv2\_CryptographySuite03** class has these types of members:</span></span>

-   [<span data-ttu-id="6ee12-113">屬性</span><span class="sxs-lookup"><span data-stu-id="6ee12-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ee12-114">屬性</span><span class="sxs-lookup"><span data-stu-id="6ee12-114">Properties</span></span>

<span data-ttu-id="6ee12-115">**MDM \_ >vpnv2 \_ CryptographySuite03** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6ee12-115">The **MDM\_VPNv2\_CryptographySuite03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6ee12-116">AuthenticationTransformConstants</span><span class="sxs-lookup"><span data-stu-id="6ee12-116">AuthenticationTransformConstants</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-authenticationtransformconstants)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ee12-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ee12-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ee12-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6ee12-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ee12-119">CipherTransformConstants</span><span class="sxs-lookup"><span data-stu-id="6ee12-119">CipherTransformConstants</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-ciphertransformconstants)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ee12-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ee12-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ee12-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6ee12-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ee12-122">DHGroup</span><span class="sxs-lookup"><span data-stu-id="6ee12-122">DHGroup</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-dhgroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ee12-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ee12-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ee12-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6ee12-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ee12-125">EncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="6ee12-125">EncryptionMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ee12-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ee12-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ee12-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6ee12-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6ee12-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6ee12-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ee12-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ee12-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ee12-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ee12-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ee12-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6ee12-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6ee12-132">節點，包含 IPSec 通道的屬性。</span><span class="sxs-lookup"><span data-stu-id="6ee12-132">Node containing the properties of IPSec tunnels.</span></span>

</dd> <dt>

[<span data-ttu-id="6ee12-133">IntegrityCheckMethod</span><span class="sxs-lookup"><span data-stu-id="6ee12-133">IntegrityCheckMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-integritycheckmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ee12-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ee12-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ee12-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6ee12-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6ee12-136">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6ee12-136">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ee12-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ee12-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ee12-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ee12-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ee12-139">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6ee12-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6ee12-140">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="6ee12-140">Describes the full path to the parent node.</span></span> <span data-ttu-id="6ee12-141">針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span><span class="sxs-lookup"><span data-stu-id="6ee12-141">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span></span>

</dd> <dt>

[<span data-ttu-id="6ee12-142">PfsGroup</span><span class="sxs-lookup"><span data-stu-id="6ee12-142">PfsGroup</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-pfsgroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ee12-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6ee12-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ee12-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6ee12-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ee12-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ee12-145">Requirements</span></span>



| <span data-ttu-id="6ee12-146">需求</span><span class="sxs-lookup"><span data-stu-id="6ee12-146">Requirement</span></span> | <span data-ttu-id="6ee12-147">值</span><span class="sxs-lookup"><span data-stu-id="6ee12-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee12-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ee12-148">Minimum supported client</span></span><br/> | <span data-ttu-id="6ee12-149">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ee12-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ee12-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ee12-150">Minimum supported server</span></span><br/> | <span data-ttu-id="6ee12-151">都不支援</span><span class="sxs-lookup"><span data-stu-id="6ee12-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6ee12-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="6ee12-152">Namespace</span></span><br/>                | <span data-ttu-id="6ee12-153">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="6ee12-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6ee12-154">MOF</span><span class="sxs-lookup"><span data-stu-id="6ee12-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ee12-155"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ee12-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ee12-156">DLL</span><span class="sxs-lookup"><span data-stu-id="6ee12-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ee12-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ee12-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

