---
title: MDM_DevDetail 類別
description: MDM \_ DevDetail 類別會處理將裝置專屬參數提供給 OMA-URI DM 伺服器的管理物件。
ms.assetid: 1a709051-656a-4900-b354-efbd208b46fc
keywords:
- MDM_DevDetail 類別
- MDM_DevDetail 類別，描述
topic_type:
- apiref
api_name:
- MDM_DevDetail
- MDM_DevDetail.InstanceID
- MDM_DevDetail.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751c4e147dd0b60398ed16eeb3eb60a8a768307f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966133"
---
# <a name="mdm_devdetail-class"></a><span data-ttu-id="07c97-105">MDM \_ DevDetail 類別</span><span class="sxs-lookup"><span data-stu-id="07c97-105">MDM\_DevDetail class</span></span>

<span data-ttu-id="07c97-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="07c97-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="07c97-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="07c97-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="07c97-108">**MDM \_ DevDetail** 類別會處理將裝置專屬參數提供給 oma-uri DM 伺服器的管理物件。</span><span class="sxs-lookup"><span data-stu-id="07c97-108">The **MDM\_DevDetail** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="07c97-109">這些裝置參數不會自動從用戶端傳送到伺服器，但可由使用 OMA-URI DM 命令的伺服器進行查詢。</span><span class="sxs-lookup"><span data-stu-id="07c97-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="07c97-110">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="07c97-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="07c97-111">語法</span><span class="sxs-lookup"><span data-stu-id="07c97-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail
{
  string  InstanceID;
  string  ParentID;
  string  DevTyp;
  string  OEM;
  string  FwV;
  string  SwV;
  string  HwV;
  boolean LrgObj;
};
```

## <a name="members"></a><span data-ttu-id="07c97-112">成員</span><span class="sxs-lookup"><span data-stu-id="07c97-112">Members</span></span>

<span data-ttu-id="07c97-113">**MDM \_ DevDetail** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="07c97-113">The **MDM\_DevDetail** class has these types of members:</span></span>

-   [<span data-ttu-id="07c97-114">屬性</span><span class="sxs-lookup"><span data-stu-id="07c97-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="07c97-115">屬性</span><span class="sxs-lookup"><span data-stu-id="07c97-115">Properties</span></span>

<span data-ttu-id="07c97-116">**MDM \_ DevDetail** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="07c97-116">The **MDM\_DevDetail** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="07c97-117">DevTyp</span><span class="sxs-lookup"><span data-stu-id="07c97-117">DevTyp</span></span>](/windows/client-management/mdm/devdetail-csp#devtyp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c97-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07c97-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07c97-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="07c97-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07c97-120">FwV</span><span class="sxs-lookup"><span data-stu-id="07c97-120">FwV</span></span>](/windows/client-management/mdm/devdetail-csp#fwv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c97-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07c97-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07c97-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="07c97-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07c97-123">HwV</span><span class="sxs-lookup"><span data-stu-id="07c97-123">HwV</span></span>](/windows/client-management/mdm/devdetail-csp#hwv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c97-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07c97-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07c97-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="07c97-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07c97-126">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="07c97-126">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c97-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07c97-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07c97-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07c97-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07c97-129">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="07c97-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="07c97-130">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="07c97-130">Identifies the name of the parent node.</span></span> <span data-ttu-id="07c97-131">針對此類別，字串為 "DevDetail"</span><span class="sxs-lookup"><span data-stu-id="07c97-131">For this class, the string is "DevDetail"</span></span>

</dd> <dt>

[<span data-ttu-id="07c97-132">LrgObj</span><span class="sxs-lookup"><span data-stu-id="07c97-132">LrgObj</span></span>](/windows/client-management/mdm/devdetail-csp#lrgobj)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c97-133">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="07c97-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07c97-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="07c97-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07c97-135">OEM</span><span class="sxs-lookup"><span data-stu-id="07c97-135">OEM</span></span>](/windows/client-management/mdm/devdetail-csp#oem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c97-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07c97-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07c97-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="07c97-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07c97-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="07c97-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c97-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07c97-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07c97-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07c97-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07c97-141">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="07c97-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="07c97-142">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="07c97-142">Describes the full path to the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="07c97-143">SwV</span><span class="sxs-lookup"><span data-stu-id="07c97-143">SwV</span></span>](/windows/client-management/mdm/devdetail-csp#swv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c97-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07c97-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07c97-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="07c97-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07c97-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="07c97-146">Requirements</span></span>



| <span data-ttu-id="07c97-147">需求</span><span class="sxs-lookup"><span data-stu-id="07c97-147">Requirement</span></span> | <span data-ttu-id="07c97-148">值</span><span class="sxs-lookup"><span data-stu-id="07c97-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07c97-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07c97-149">Minimum supported client</span></span><br/> | <span data-ttu-id="07c97-150">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07c97-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="07c97-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07c97-151">Minimum supported server</span></span><br/> | <span data-ttu-id="07c97-152">都不支援</span><span class="sxs-lookup"><span data-stu-id="07c97-152">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="07c97-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="07c97-153">Namespace</span></span><br/>                | <span data-ttu-id="07c97-154">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="07c97-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="07c97-155">MOF</span><span class="sxs-lookup"><span data-stu-id="07c97-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07c97-156"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="07c97-156"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="07c97-157">DLL</span><span class="sxs-lookup"><span data-stu-id="07c97-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07c97-158"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07c97-158"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07c97-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07c97-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c97-160">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="07c97-160">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

