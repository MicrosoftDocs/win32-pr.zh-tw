---
title: MDM_DevDetail_Microsoft02 類別
description: MDM \_ DevDetail \_ Microsoft02 類別會處理將裝置專屬參數提供給 oma-uri DM 伺服器的管理物件。
ms.assetid: 22a8ba26-d215-4bc5-a51b-6933d5473da3
keywords:
- MDM_DevDetail_Microsoft02 類別
- MDM_DevDetail_Microsoft02 類別，描述
topic_type:
- apiref
api_name:
- MDM_DevDetail_Microsoft02
- MDM_DevDetail_Microsoft02.InstanceID
- MDM_DevDetail_Microsoft02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b384f9a24e30ca739ff9290efc83730b6d467e4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934778"
---
# <a name="mdm_devdetail_microsoft02-class"></a><span data-ttu-id="afb88-105">MDM \_ DevDetail \_ Microsoft02 類別</span><span class="sxs-lookup"><span data-stu-id="afb88-105">MDM\_DevDetail\_Microsoft02 class</span></span>

<span data-ttu-id="afb88-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="afb88-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="afb88-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="afb88-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="afb88-108">**MDM \_ DevDetail \_ Microsoft02** 類別會處理將裝置專屬參數提供給 oma-uri DM 伺服器的管理物件。</span><span class="sxs-lookup"><span data-stu-id="afb88-108">The **MDM\_DevDetail\_Microsoft02** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="afb88-109">這些裝置參數不會自動從用戶端傳送到伺服器，但可由使用 OMA-URI DM 命令的伺服器進行查詢。</span><span class="sxs-lookup"><span data-stu-id="afb88-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="afb88-110">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="afb88-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="afb88-111">語法</span><span class="sxs-lookup"><span data-stu-id="afb88-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Microsoft02
{
  string InstanceID;
  string ParentID;
  string MobileID;
  string RadioSwV;
  string Resolution;
  string CommercializationOperator;
  sint32 ProcessorArchitecture;
  sint32 ProcessorType;
  string OSPlatform;
  string LocalTime;
  string DeviceName;
};
```

## <a name="members"></a><span data-ttu-id="afb88-112">成員</span><span class="sxs-lookup"><span data-stu-id="afb88-112">Members</span></span>

<span data-ttu-id="afb88-113">**MDM \_ DevDetail \_ Microsoft02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="afb88-113">The **MDM\_DevDetail\_Microsoft02** class has these types of members:</span></span>

-   [<span data-ttu-id="afb88-114">屬性</span><span class="sxs-lookup"><span data-stu-id="afb88-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="afb88-115">屬性</span><span class="sxs-lookup"><span data-stu-id="afb88-115">Properties</span></span>

<span data-ttu-id="afb88-116">**MDM \_ DevDetail \_ Microsoft02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="afb88-116">The **MDM\_DevDetail\_Microsoft02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="afb88-117">CommercializationOperator</span><span class="sxs-lookup"><span data-stu-id="afb88-117">CommercializationOperator</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-commercializationoperator)
</dt> <dd> <dl> <dt>

<span data-ttu-id="afb88-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="afb88-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afb88-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="afb88-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="afb88-120">DeviceName</span><span class="sxs-lookup"><span data-stu-id="afb88-120">DeviceName</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-devicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="afb88-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="afb88-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afb88-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="afb88-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="afb88-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="afb88-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afb88-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="afb88-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afb88-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="afb88-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afb88-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="afb88-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="afb88-127">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="afb88-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="afb88-128">此類別的字串為 "Microsoft"</span><span class="sxs-lookup"><span data-stu-id="afb88-128">For this class, the string is "Microsoft"</span></span>

</dd> <dt>

[<span data-ttu-id="afb88-129">LocalTime</span><span class="sxs-lookup"><span data-stu-id="afb88-129">LocalTime</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-localtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="afb88-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="afb88-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afb88-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="afb88-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="afb88-132">MobileID</span><span class="sxs-lookup"><span data-stu-id="afb88-132">MobileID</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-mobileid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="afb88-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="afb88-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afb88-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="afb88-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="afb88-135">OSPlatform</span><span class="sxs-lookup"><span data-stu-id="afb88-135">OSPlatform</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-osplatform)
</dt> <dd> <dl> <dt>

<span data-ttu-id="afb88-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="afb88-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afb88-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="afb88-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="afb88-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="afb88-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afb88-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="afb88-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afb88-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="afb88-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afb88-141">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="afb88-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="afb88-142">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="afb88-142">Describes the full path to the parent node.</span></span> <span data-ttu-id="afb88-143">此類別的字串為 "./DevDetail/Ext"</span><span class="sxs-lookup"><span data-stu-id="afb88-143">For this class, the string is "./DevDetail/Ext"</span></span>

</dd> <dt>

[<span data-ttu-id="afb88-144">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="afb88-144">ProcessorArchitecture</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processorarchitecture)
</dt> <dd> <dl> <dt>

<span data-ttu-id="afb88-145">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="afb88-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="afb88-146">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="afb88-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="afb88-147">ProcessorType</span><span class="sxs-lookup"><span data-stu-id="afb88-147">ProcessorType</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processortype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="afb88-148">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="afb88-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="afb88-149">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="afb88-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="afb88-150">RadioSwV</span><span class="sxs-lookup"><span data-stu-id="afb88-150">RadioSwV</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-radioswv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="afb88-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="afb88-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afb88-152">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="afb88-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="afb88-153">傳回無線電堆疊軟體版本號碼。</span><span class="sxs-lookup"><span data-stu-id="afb88-153">Returns the radio stack software version number.</span></span>

</dd> <dt>

[<span data-ttu-id="afb88-154">解決方法</span><span class="sxs-lookup"><span data-stu-id="afb88-154">Resolution</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-resolution)
</dt> <dd> <dl> <dt>

<span data-ttu-id="afb88-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="afb88-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afb88-156">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="afb88-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="afb88-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="afb88-157">Requirements</span></span>



| <span data-ttu-id="afb88-158">需求</span><span class="sxs-lookup"><span data-stu-id="afb88-158">Requirement</span></span> | <span data-ttu-id="afb88-159">值</span><span class="sxs-lookup"><span data-stu-id="afb88-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afb88-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="afb88-160">Minimum supported client</span></span><br/> | <span data-ttu-id="afb88-161">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afb88-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="afb88-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="afb88-162">Minimum supported server</span></span><br/> | <span data-ttu-id="afb88-163">都不支援</span><span class="sxs-lookup"><span data-stu-id="afb88-163">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="afb88-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="afb88-164">Namespace</span></span><br/>                | <span data-ttu-id="afb88-165">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="afb88-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="afb88-166">MOF</span><span class="sxs-lookup"><span data-stu-id="afb88-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afb88-167"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="afb88-167"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="afb88-168">DLL</span><span class="sxs-lookup"><span data-stu-id="afb88-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afb88-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afb88-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afb88-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afb88-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afb88-171">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="afb88-171">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

