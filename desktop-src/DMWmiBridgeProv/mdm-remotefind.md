---
title: MDM_RemoteFind 類別
description: MDM \_ RemoteFind 類別會捕獲特定裝置的位置資訊。
ms.assetid: 8dfbe951-b4ca-4709-bec9-0821571f9b0e
keywords:
- MDM_RemoteFind 類別
- MDM_RemoteFind 類別，描述
topic_type:
- apiref
api_name:
- MDM_RemoteFind
- MDM_RemoteFind.InstanceID
- MDM_RemoteFind.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8930d80ede9daad5c721cd3b226c85e3d9918a19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685551"
---
# <a name="mdm_remotefind-class"></a><span data-ttu-id="592a4-105">MDM \_ RemoteFind 類別</span><span class="sxs-lookup"><span data-stu-id="592a4-105">MDM\_RemoteFind class</span></span>

<span data-ttu-id="592a4-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="592a4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="592a4-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="592a4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="592a4-108">**MDM \_ RemoteFind** 類別會捕獲特定裝置的位置資訊。</span><span class="sxs-lookup"><span data-stu-id="592a4-108">The **MDM\_RemoteFind** class retrieves the location information for a particular device.</span></span>

<span data-ttu-id="592a4-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="592a4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="592a4-110">語法</span><span class="sxs-lookup"><span data-stu-id="592a4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind
{
  string InstanceID;
  string ParentID;
  sint32 DesiredAccuracy;
  sint32 MaximumAge;
  sint32 Timeout;
};
```

## <a name="members"></a><span data-ttu-id="592a4-111">成員</span><span class="sxs-lookup"><span data-stu-id="592a4-111">Members</span></span>

<span data-ttu-id="592a4-112">**MDM \_ RemoteFind** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="592a4-112">The **MDM\_RemoteFind** class has these types of members:</span></span>

-   [<span data-ttu-id="592a4-113">屬性</span><span class="sxs-lookup"><span data-stu-id="592a4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="592a4-114">屬性</span><span class="sxs-lookup"><span data-stu-id="592a4-114">Properties</span></span>

<span data-ttu-id="592a4-115">**MDM \_ RemoteFind** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="592a4-115">The **MDM\_RemoteFind** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="592a4-116">DesiredAccuracy</span><span class="sxs-lookup"><span data-stu-id="592a4-116">DesiredAccuracy</span></span>](/windows/client-management/mdm/remotefind-csp#desiredaccuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="592a4-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="592a4-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="592a4-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="592a4-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="592a4-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="592a4-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592a4-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="592a4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="592a4-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="592a4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="592a4-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="592a4-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="592a4-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="592a4-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="592a4-124">此類別的字串為 "RemoteFind"。</span><span class="sxs-lookup"><span data-stu-id="592a4-124">For this class, the string is "RemoteFind".</span></span>

</dd> <dt>

[<span data-ttu-id="592a4-125">MaximumAge</span><span class="sxs-lookup"><span data-stu-id="592a4-125">MaximumAge</span></span>](/windows/client-management/mdm/remotefind-csp#maximumage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="592a4-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="592a4-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="592a4-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="592a4-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="592a4-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="592a4-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592a4-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="592a4-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="592a4-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="592a4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="592a4-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="592a4-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="592a4-132">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="592a4-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="592a4-133">此類別的字串為 "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="592a4-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="592a4-134">逾時</span><span class="sxs-lookup"><span data-stu-id="592a4-134">Timeout</span></span>](/windows/client-management/mdm/remotefind-csp#timeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="592a4-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="592a4-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="592a4-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="592a4-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="592a4-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="592a4-137">Requirements</span></span>



| <span data-ttu-id="592a4-138">需求</span><span class="sxs-lookup"><span data-stu-id="592a4-138">Requirement</span></span> | <span data-ttu-id="592a4-139">值</span><span class="sxs-lookup"><span data-stu-id="592a4-139">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="592a4-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="592a4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="592a4-141">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="592a4-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="592a4-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="592a4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="592a4-143">都不支援</span><span class="sxs-lookup"><span data-stu-id="592a4-143">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="592a4-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="592a4-144">Namespace</span></span><br/>                | <span data-ttu-id="592a4-145">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="592a4-145">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                              |
| <span data-ttu-id="592a4-146">MOF</span><span class="sxs-lookup"><span data-stu-id="592a4-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="592a4-147"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="592a4-147"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="592a4-148">DLL</span><span class="sxs-lookup"><span data-stu-id="592a4-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="592a4-149"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="592a4-149"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="592a4-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="592a4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="592a4-151">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="592a4-151">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

