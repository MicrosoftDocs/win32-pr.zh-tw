---
title: MDM_RemoteFind_Location01 類別
description: MDM \_ RemoteFind \_ Location01 類別會捕獲特定裝置的位置資訊。
ms.assetid: 0c26bb3c-99b4-43ed-99ce-d976d48c4445
keywords:
- MDM_RemoteFind_Location01 類別
- MDM_RemoteFind_Location01 類別，描述
topic_type:
- apiref
api_name:
- MDM_RemoteFind_Location01
- MDM_RemoteFind_Location01.InstanceID
- MDM_RemoteFind_Location01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e1b46a7b4a0c3439f78f38a5fb6cd5b865275c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464356"
---
# <a name="mdm_remotefind_location01-class"></a><span data-ttu-id="eb703-105">MDM \_ RemoteFind \_ Location01 類別</span><span class="sxs-lookup"><span data-stu-id="eb703-105">MDM\_RemoteFind\_Location01 class</span></span>

<span data-ttu-id="eb703-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="eb703-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="eb703-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="eb703-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="eb703-108">**MDM \_ RemoteFind \_ Location01** 類別會捕獲特定裝置的位置資訊。</span><span class="sxs-lookup"><span data-stu-id="eb703-108">The **MDM\_RemoteFind\_Location01** class retrieves the location information for a particular device.</span></span>

<span data-ttu-id="eb703-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="eb703-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb703-110">語法</span><span class="sxs-lookup"><span data-stu-id="eb703-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind_Location01
{
  string   InstanceID;
  string   ParentID;
  real32   Latitude;
  real32   Longitude;
  real32   Altitude;
  sint32   Accuracy;
  sint32   AltitudeAccuracy;
  datetime Age;
};
```

## <a name="members"></a><span data-ttu-id="eb703-111">成員</span><span class="sxs-lookup"><span data-stu-id="eb703-111">Members</span></span>

<span data-ttu-id="eb703-112">**MDM \_ RemoteFind \_ Location01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="eb703-112">The **MDM\_RemoteFind\_Location01** class has these types of members:</span></span>

-   [<span data-ttu-id="eb703-113">屬性</span><span class="sxs-lookup"><span data-stu-id="eb703-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb703-114">屬性</span><span class="sxs-lookup"><span data-stu-id="eb703-114">Properties</span></span>

<span data-ttu-id="eb703-115">**MDM \_ RemoteFind \_ Location01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="eb703-115">The **MDM\_RemoteFind\_Location01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="eb703-116">精確度</span><span class="sxs-lookup"><span data-stu-id="eb703-116">Accuracy</span></span>](/windows/client-management/mdm/remotefind-csp#accuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb703-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="eb703-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb703-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="eb703-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb703-119">Age</span><span class="sxs-lookup"><span data-stu-id="eb703-119">Age</span></span>](/windows/client-management/mdm/remotefind-csp#age)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb703-120">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="eb703-120">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eb703-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="eb703-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb703-122">高度</span><span class="sxs-lookup"><span data-stu-id="eb703-122">Altitude</span></span>](/windows/client-management/mdm/remotefind-csp#altitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb703-123">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="eb703-123">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="eb703-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="eb703-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb703-125">AltitudeAccuracy</span><span class="sxs-lookup"><span data-stu-id="eb703-125">AltitudeAccuracy</span></span>](/windows/client-management/mdm/remotefind-csp#altitudeaccuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb703-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="eb703-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb703-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="eb703-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb703-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eb703-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb703-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb703-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb703-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb703-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb703-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eb703-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eb703-132">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb703-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="eb703-133">此類別的字串為 "Location"。</span><span class="sxs-lookup"><span data-stu-id="eb703-133">For this class, the string is "Location".</span></span>

</dd> <dt>

[<span data-ttu-id="eb703-134">緯度</span><span class="sxs-lookup"><span data-stu-id="eb703-134">Latitude</span></span>](/windows/client-management/mdm/remotefind-csp#latitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb703-135">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="eb703-135">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="eb703-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="eb703-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb703-137">經度</span><span class="sxs-lookup"><span data-stu-id="eb703-137">Longitude</span></span>](/windows/client-management/mdm/remotefind-csp#longitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb703-138">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="eb703-138">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="eb703-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="eb703-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb703-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="eb703-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb703-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb703-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb703-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb703-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb703-143">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eb703-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eb703-144">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="eb703-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="eb703-145">此類別的字串為 "./Vendor/MSFT/RemoteFind"</span><span class="sxs-lookup"><span data-stu-id="eb703-145">For this class, the string is "./Vendor/MSFT/RemoteFind"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb703-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb703-146">Requirements</span></span>



| <span data-ttu-id="eb703-147">需求</span><span class="sxs-lookup"><span data-stu-id="eb703-147">Requirement</span></span> | <span data-ttu-id="eb703-148">值</span><span class="sxs-lookup"><span data-stu-id="eb703-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb703-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb703-149">Minimum supported client</span></span><br/> | <span data-ttu-id="eb703-150">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb703-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eb703-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb703-151">Minimum supported server</span></span><br/> | <span data-ttu-id="eb703-152">都不支援</span><span class="sxs-lookup"><span data-stu-id="eb703-152">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="eb703-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="eb703-153">Namespace</span></span><br/>                | <span data-ttu-id="eb703-154">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="eb703-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="eb703-155">MOF</span><span class="sxs-lookup"><span data-stu-id="eb703-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb703-156"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb703-156"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb703-157">DLL</span><span class="sxs-lookup"><span data-stu-id="eb703-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb703-158"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb703-158"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="eb703-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb703-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb703-160">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="eb703-160">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

