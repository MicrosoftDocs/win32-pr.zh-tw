---
title: MDM_DeviceStatus_Antispyware01 類別
description: '\_ \_ 企業會使用 MDM DeviceStatus Antispyware01 類別，以其企業原則查詢裝置的反間諜功能合規性狀態。'
ms.assetid: 53275aa1-ff7d-4630-b6c5-aedce3f4665a
keywords:
- MDM_DeviceStatus_Antispyware01 類別
- MDM_DeviceStatus_Antispyware01 類別，描述
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Antispyware01
- MDM_DeviceStatus_Antispyware01.InstanceID
- MDM_DeviceStatus_Antispyware01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91468c98981c93e211b3e3bee99564574f7a56cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843967"
---
# <a name="mdm_devicestatus_antispyware01-class"></a><span data-ttu-id="04b33-105">MDM \_ DeviceStatus \_ Antispyware01 類別</span><span class="sxs-lookup"><span data-stu-id="04b33-105">MDM\_DeviceStatus\_Antispyware01 class</span></span>

<span data-ttu-id="04b33-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="04b33-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="04b33-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="04b33-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="04b33-108">企業會使用 **MDM \_ DeviceStatus \_ Antispyware01** 類別，以其企業原則查詢裝置的反間諜功能合規性狀態。</span><span class="sxs-lookup"><span data-stu-id="04b33-108">The **MDM\_DeviceStatus\_Antispyware01** class is used by the enterprise to query the state of antispyware compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="04b33-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="04b33-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b33-110">語法</span><span class="sxs-lookup"><span data-stu-id="04b33-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Antispyware01
{
  string InstanceID;
  string ParentID;
  sint32 SignatureStatus;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="04b33-111">成員</span><span class="sxs-lookup"><span data-stu-id="04b33-111">Members</span></span>

<span data-ttu-id="04b33-112">**MDM \_ DeviceStatus \_ Antispyware01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="04b33-112">The **MDM\_DeviceStatus\_Antispyware01** class has these types of members:</span></span>

-   [<span data-ttu-id="04b33-113">屬性</span><span class="sxs-lookup"><span data-stu-id="04b33-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04b33-114">屬性</span><span class="sxs-lookup"><span data-stu-id="04b33-114">Properties</span></span>

<span data-ttu-id="04b33-115">**MDM \_ DeviceStatus \_ Antispyware01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="04b33-115">The **MDM\_DeviceStatus\_Antispyware01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04b33-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="04b33-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b33-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04b33-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04b33-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04b33-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04b33-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="04b33-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="04b33-120">反間諜軟體查詢的節點。</span><span class="sxs-lookup"><span data-stu-id="04b33-120">Node for the antispyware query.</span></span>

</dd> <dt>

<span data-ttu-id="04b33-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="04b33-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b33-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04b33-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04b33-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04b33-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04b33-124">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="04b33-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="04b33-125">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="04b33-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="04b33-126">此類別的字串為 "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="04b33-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="04b33-127">SignatureStatus</span><span class="sxs-lookup"><span data-stu-id="04b33-127">SignatureStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-antivirus-signaturestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b33-128">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="04b33-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="04b33-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="04b33-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="04b33-130">狀態</span><span class="sxs-lookup"><span data-stu-id="04b33-130">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b33-131">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="04b33-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="04b33-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="04b33-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04b33-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="04b33-133">Requirements</span></span>



| <span data-ttu-id="04b33-134">需求</span><span class="sxs-lookup"><span data-stu-id="04b33-134">Requirement</span></span> | <span data-ttu-id="04b33-135">值</span><span class="sxs-lookup"><span data-stu-id="04b33-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04b33-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04b33-136">Minimum supported client</span></span><br/> | <span data-ttu-id="04b33-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04b33-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="04b33-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04b33-138">Minimum supported server</span></span><br/> | <span data-ttu-id="04b33-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="04b33-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="04b33-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="04b33-140">Namespace</span></span><br/>                | <span data-ttu-id="04b33-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="04b33-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="04b33-142">MOF</span><span class="sxs-lookup"><span data-stu-id="04b33-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04b33-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="04b33-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="04b33-144">DLL</span><span class="sxs-lookup"><span data-stu-id="04b33-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04b33-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04b33-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

