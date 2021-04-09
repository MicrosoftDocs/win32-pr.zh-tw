---
title: MDM_DevDetail_Ext01 類別
description: MDM \_ DevDetail \_ Ext01 類別會處理將裝置專屬參數提供給 oma-uri DM 伺服器的管理物件。
ms.assetid: 8b8cb8e8-a299-4a87-8206-a846a79dd647
keywords:
- MDM_DevDetail_Ext01 類別
- MDM_DevDetail_Ext01 類別，描述
topic_type:
- apiref
api_name:
- MDM_DevDetail_Ext01
- MDM_DevDetail_Ext01.InstanceID
- MDM_DevDetail_Ext01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed7d7b68ab192a50a4c029bf573f5de730b8e30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686191"
---
# <a name="mdm_devdetail_ext01-class"></a><span data-ttu-id="7bebd-105">MDM \_ DevDetail \_ Ext01 類別</span><span class="sxs-lookup"><span data-stu-id="7bebd-105">MDM\_DevDetail\_Ext01 class</span></span>

<span data-ttu-id="7bebd-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="7bebd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7bebd-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="7bebd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7bebd-108">**MDM \_ DevDetail \_ Ext01** 類別會處理將裝置專屬參數提供給 oma-uri DM 伺服器的管理物件。</span><span class="sxs-lookup"><span data-stu-id="7bebd-108">The **MDM\_DevDetail\_Ext01** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="7bebd-109">這些裝置參數不會自動從用戶端傳送到伺服器，但可由使用 OMA-URI DM 命令的伺服器進行查詢。</span><span class="sxs-lookup"><span data-stu-id="7bebd-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="7bebd-110">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7bebd-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bebd-111">語法</span><span class="sxs-lookup"><span data-stu-id="7bebd-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Ext01
{
  string InstanceID;
  string ParentID;
  string DeviceHardwareData;
  string WLANMACAddress;
};
```

## <a name="members"></a><span data-ttu-id="7bebd-112">成員</span><span class="sxs-lookup"><span data-stu-id="7bebd-112">Members</span></span>

<span data-ttu-id="7bebd-113">**MDM \_ DevDetail \_ Ext01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7bebd-113">The **MDM\_DevDetail\_Ext01** class has these types of members:</span></span>

-   [<span data-ttu-id="7bebd-114">屬性</span><span class="sxs-lookup"><span data-stu-id="7bebd-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7bebd-115">屬性</span><span class="sxs-lookup"><span data-stu-id="7bebd-115">Properties</span></span>

<span data-ttu-id="7bebd-116">**MDM \_ DevDetail \_ Ext01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7bebd-116">The **MDM\_DevDetail\_Ext01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7bebd-117">DeviceHardwareData</span><span class="sxs-lookup"><span data-stu-id="7bebd-117">DeviceHardwareData</span></span>](/windows/client-management/mdm/devdetail-csp#devicehardwaredata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bebd-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7bebd-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bebd-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7bebd-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7bebd-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7bebd-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bebd-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7bebd-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bebd-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7bebd-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bebd-123">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7bebd-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7bebd-124">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bebd-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="7bebd-125">針對此類別，字串為 "Ext"</span><span class="sxs-lookup"><span data-stu-id="7bebd-125">For this class, the string is "Ext"</span></span>

</dd> <dt>

<span data-ttu-id="7bebd-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7bebd-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bebd-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7bebd-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bebd-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7bebd-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bebd-129">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7bebd-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7bebd-130">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="7bebd-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="7bebd-131">此類別的字串為 "./DevDetail/"</span><span class="sxs-lookup"><span data-stu-id="7bebd-131">For this class, the string is "./DevDetail/"</span></span>

</dd> <dt>

[<span data-ttu-id="7bebd-132">WLANMACAddress</span><span class="sxs-lookup"><span data-stu-id="7bebd-132">WLANMACAddress</span></span>](/windows/client-management/mdm/devdetail-csp#ext-wlanmacaddress)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bebd-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7bebd-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bebd-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7bebd-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7bebd-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="7bebd-135">Requirements</span></span>



| <span data-ttu-id="7bebd-136">需求</span><span class="sxs-lookup"><span data-stu-id="7bebd-136">Requirement</span></span> | <span data-ttu-id="7bebd-137">值</span><span class="sxs-lookup"><span data-stu-id="7bebd-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bebd-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7bebd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7bebd-139">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7bebd-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7bebd-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7bebd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7bebd-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="7bebd-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7bebd-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="7bebd-142">Namespace</span></span><br/>                | <span data-ttu-id="7bebd-143">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="7bebd-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7bebd-144">MOF</span><span class="sxs-lookup"><span data-stu-id="7bebd-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bebd-145"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="7bebd-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bebd-146">DLL</span><span class="sxs-lookup"><span data-stu-id="7bebd-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bebd-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bebd-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bebd-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7bebd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bebd-149">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="7bebd-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

