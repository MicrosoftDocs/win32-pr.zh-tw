---
title: MDM_DeviceStatus_OS01 類別
description: '\_ \_ 企業會使用 MDM DeviceStatus OS01 類別，以其企業原則查詢裝置上的作業系統。'
ms.assetid: 887dc453-f6b5-4f09-8ce1-b87f71dd8396
keywords:
- MDM_DeviceStatus_OS01 類別
- MDM_DeviceStatus_OS01 類別，描述
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_OS01
- MDM_DeviceStatus_OS01.InstanceID
- MDM_DeviceStatus_OS01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01bff7a57d71b3d651ea2b97a0eac5b2ccd94255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105000"
---
# <a name="mdm_devicestatus_os01-class"></a><span data-ttu-id="9c589-105">MDM \_ DeviceStatus \_ OS01 類別</span><span class="sxs-lookup"><span data-stu-id="9c589-105">MDM\_DeviceStatus\_OS01 class</span></span>

<span data-ttu-id="9c589-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="9c589-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9c589-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="9c589-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9c589-108">企業會使用 **MDM \_ DeviceStatus \_ OS01** 類別，以其企業原則查詢裝置上的作業系統。</span><span class="sxs-lookup"><span data-stu-id="9c589-108">The **MDM\_DeviceStatus\_OS01** class is used by the enterprise to query the operating system on devices with their enterprise policies.</span></span>

<span data-ttu-id="9c589-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9c589-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c589-110">語法</span><span class="sxs-lookup"><span data-stu-id="9c589-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_OS01
{
  string InstanceID;
  string ParentID;
  string Edition;
};
```

## <a name="members"></a><span data-ttu-id="9c589-111">成員</span><span class="sxs-lookup"><span data-stu-id="9c589-111">Members</span></span>

<span data-ttu-id="9c589-112">**MDM \_ DeviceStatus \_ OS01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9c589-112">The **MDM\_DeviceStatus\_OS01** class has these types of members:</span></span>

-   [<span data-ttu-id="9c589-113">屬性</span><span class="sxs-lookup"><span data-stu-id="9c589-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c589-114">屬性</span><span class="sxs-lookup"><span data-stu-id="9c589-114">Properties</span></span>

<span data-ttu-id="9c589-115">**MDM \_ DeviceStatus \_ OS01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9c589-115">The **MDM\_DeviceStatus\_OS01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9c589-116">版本(Edition)</span><span class="sxs-lookup"><span data-stu-id="9c589-116">Edition</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-os-edition)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c589-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9c589-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c589-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9c589-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9c589-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9c589-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c589-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9c589-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c589-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c589-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c589-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9c589-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9c589-123">作業系統查詢的節點。</span><span class="sxs-lookup"><span data-stu-id="9c589-123">Node for the OS query.</span></span>

</dd> <dt>

<span data-ttu-id="9c589-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9c589-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c589-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9c589-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c589-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c589-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c589-127">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9c589-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9c589-128">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="9c589-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="9c589-129">此類別的字串為 "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="9c589-129">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c589-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c589-130">Requirements</span></span>



| <span data-ttu-id="9c589-131">需求</span><span class="sxs-lookup"><span data-stu-id="9c589-131">Requirement</span></span> | <span data-ttu-id="9c589-132">值</span><span class="sxs-lookup"><span data-stu-id="9c589-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c589-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c589-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9c589-134">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c589-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9c589-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c589-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9c589-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="9c589-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9c589-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="9c589-137">Namespace</span></span><br/>                | <span data-ttu-id="9c589-138">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="9c589-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9c589-139">MOF</span><span class="sxs-lookup"><span data-stu-id="9c589-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c589-140"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c589-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c589-141">DLL</span><span class="sxs-lookup"><span data-stu-id="9c589-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c589-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c589-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

