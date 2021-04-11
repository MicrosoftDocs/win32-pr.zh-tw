---
title: MDM_WindowsLicensing_Subscriptions01_01 類別
description: MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01 類別是針對訂用帳戶相關的授權管理案例而設計。
ms.assetid: dc3b7eae-89d3-4e66-a65f-f100e23ea9fd
keywords:
- MDM_WindowsLicensing_Subscriptions01_01 類別
- MDM_WindowsLicensing_Subscriptions01_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing_Subscriptions01_01
- MDM_WindowsLicensing_Subscriptions01_01.InstanceID
- MDM_WindowsLicensing_Subscriptions01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911c578bd0e3cbc56c61f2cf85438660e8f437b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104939"
---
# <a name="mdm_windowslicensing_subscriptions01_01-class"></a><span data-ttu-id="b865d-105">MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="b865d-105">MDM\_WindowsLicensing\_Subscriptions01\_01 class</span></span>

<span data-ttu-id="b865d-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="b865d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b865d-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="b865d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b865d-108">**MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** 類別是針對訂用帳戶相關的授權管理案例而設計。</span><span class="sxs-lookup"><span data-stu-id="b865d-108">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class is designed for subscription-related licensing management scenarios.</span></span>

<span data-ttu-id="b865d-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b865d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b865d-110">語法</span><span class="sxs-lookup"><span data-stu-id="b865d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing_Subscriptions01_01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="b865d-111">成員</span><span class="sxs-lookup"><span data-stu-id="b865d-111">Members</span></span>

<span data-ttu-id="b865d-112">**MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b865d-112">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="b865d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b865d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b865d-114">屬性</span><span class="sxs-lookup"><span data-stu-id="b865d-114">Properties</span></span>

<span data-ttu-id="b865d-115">**MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b865d-115">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b865d-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b865d-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b865d-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b865d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b865d-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b865d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b865d-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b865d-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b865d-120">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="b865d-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="b865d-121">名稱</span><span class="sxs-lookup"><span data-stu-id="b865d-121">Name</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b865d-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b865d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b865d-123">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b865d-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b865d-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b865d-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b865d-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b865d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b865d-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b865d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b865d-127">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b865d-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b865d-128">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b865d-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="b865d-129">此類別的字串為 "./Vendor/MSFT/WindowsLicensing"</span><span class="sxs-lookup"><span data-stu-id="b865d-129">For this class, the string is "./Vendor/MSFT/WindowsLicensing"</span></span>

</dd> <dt>

[<span data-ttu-id="b865d-130">狀態</span><span class="sxs-lookup"><span data-stu-id="b865d-130">Status</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b865d-131">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b865d-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b865d-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b865d-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b865d-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="b865d-133">Requirements</span></span>



| <span data-ttu-id="b865d-134">需求</span><span class="sxs-lookup"><span data-stu-id="b865d-134">Requirement</span></span> | <span data-ttu-id="b865d-135">值</span><span class="sxs-lookup"><span data-stu-id="b865d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b865d-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b865d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b865d-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b865d-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b865d-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b865d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b865d-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="b865d-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b865d-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="b865d-140">Namespace</span></span><br/>                | <span data-ttu-id="b865d-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="b865d-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b865d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b865d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b865d-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="b865d-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b865d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b865d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b865d-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b865d-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

