---
title: MDM_DeviceStatus_TPM01 類別
description: '\_ \_ 企業會使用 MDM DeviceStatus TPM01 類別，以其企業原則查詢裝置的 TPM 版本。'
ms.assetid: 9df10fbe-91b7-49f4-9e27-6c42218a6718
keywords:
- MDM_DeviceStatus_TPM01 類別
- MDM_DeviceStatus_TPM01 類別，描述
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_TPM01
- MDM_DeviceStatus_TPM01.InstanceID
- MDM_DeviceStatus_TPM01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a7231e3801867ec7722afe40aae44b1b541a545
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843960"
---
# <a name="mdm_devicestatus_tpm01-class"></a><span data-ttu-id="bf496-105">MDM \_ DeviceStatus \_ TPM01 類別</span><span class="sxs-lookup"><span data-stu-id="bf496-105">MDM\_DeviceStatus\_TPM01 class</span></span>

<span data-ttu-id="bf496-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="bf496-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bf496-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="bf496-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bf496-108">企業會使用 **MDM \_ DeviceStatus \_ TPM01** 類別，以其企業原則查詢裝置的 TPM 版本。</span><span class="sxs-lookup"><span data-stu-id="bf496-108">The **MDM\_DeviceStatus\_TPM01** class is used by the enterprise to query the TPM version of devices with their enterprise policies.</span></span>

<span data-ttu-id="bf496-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bf496-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf496-110">語法</span><span class="sxs-lookup"><span data-stu-id="bf496-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_TPM01
{
  string InstanceID;
  string ParentID;
  string SpecificationVersion;
};
```

## <a name="members"></a><span data-ttu-id="bf496-111">成員</span><span class="sxs-lookup"><span data-stu-id="bf496-111">Members</span></span>

<span data-ttu-id="bf496-112">**MDM \_ DeviceStatus \_ TPM01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bf496-112">The **MDM\_DeviceStatus\_TPM01** class has these types of members:</span></span>

-   [<span data-ttu-id="bf496-113">屬性</span><span class="sxs-lookup"><span data-stu-id="bf496-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf496-114">屬性</span><span class="sxs-lookup"><span data-stu-id="bf496-114">Properties</span></span>

<span data-ttu-id="bf496-115">**MDM \_ DeviceStatus \_ TPM01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bf496-115">The **MDM\_DeviceStatus\_TPM01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf496-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bf496-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf496-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bf496-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf496-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf496-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf496-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bf496-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bf496-120">TPM 查詢的節點。</span><span class="sxs-lookup"><span data-stu-id="bf496-120">Node for the TPM query.</span></span>

</dd> <dt>

<span data-ttu-id="bf496-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bf496-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf496-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bf496-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf496-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf496-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf496-124">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bf496-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bf496-125">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="bf496-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="bf496-126">此類別的字串為 "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="bf496-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="bf496-127">SpecificationVersion</span><span class="sxs-lookup"><span data-stu-id="bf496-127">SpecificationVersion</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-tpm-specificationversion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf496-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bf496-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf496-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bf496-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf496-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf496-130">Requirements</span></span>



| <span data-ttu-id="bf496-131">需求</span><span class="sxs-lookup"><span data-stu-id="bf496-131">Requirement</span></span> | <span data-ttu-id="bf496-132">值</span><span class="sxs-lookup"><span data-stu-id="bf496-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf496-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf496-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bf496-134">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf496-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf496-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf496-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bf496-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="bf496-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bf496-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="bf496-137">Namespace</span></span><br/>                | <span data-ttu-id="bf496-138">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="bf496-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bf496-139">MOF</span><span class="sxs-lookup"><span data-stu-id="bf496-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf496-140"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf496-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf496-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bf496-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf496-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf496-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

