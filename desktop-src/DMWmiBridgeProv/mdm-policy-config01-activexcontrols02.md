---
title: MDM_Policy_Config01_ActiveXControls02 類別
description: 此原則設定可決定您的組織中標準使用者可以使用哪些 ActiveX 安裝網站在其電腦上安裝 ActiveX 控制項。
ms.assetid: 242888ae-f07a-40b7-9539-29fcca9cfc40
keywords:
- MDM_Policy_Config01_ActiveXControls02 類別
- MDM_Policy_Config01_ActiveXControls02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ActiveXControls02
- MDM_Policy_Config01_ActiveXControls02.InstanceID
- MDM_Policy_Config01_ActiveXControls02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 213edcea47bc0fd3379f753613c5b884963ca781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968756"
---
# <a name="mdm_policy_config01_activexcontrols02-class"></a><span data-ttu-id="2c972-105">MDM \_ 原則 \_ Config01 \_ ActiveXControls02 類別</span><span class="sxs-lookup"><span data-stu-id="2c972-105">MDM\_Policy\_Config01\_ActiveXControls02 class</span></span>

<span data-ttu-id="2c972-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="2c972-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2c972-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="2c972-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2c972-108">此原則設定可決定您的組織中標準使用者可以使用哪些 ActiveX 安裝網站在其電腦上安裝 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="2c972-108">This policy setting determines which ActiveX installation sites standard users in your organization can use to install ActiveX controls on their computers.</span></span> <span data-ttu-id="2c972-109">啟用此設定時，系統管理員可以建立由主機 URL 指定的已核准 Activex 安裝網站清單。</span><span class="sxs-lookup"><span data-stu-id="2c972-109">When this setting is enabled, the administrator can create a list of approved Activex Install sites specified by host URL.</span></span>

<span data-ttu-id="2c972-110">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2c972-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c972-111">語法</span><span class="sxs-lookup"><span data-stu-id="2c972-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ActiveXControls02
{
  string InstanceID;
  string ParentID;
  string ApprovedInstallationSites;
};
```

## <a name="members"></a><span data-ttu-id="2c972-112">成員</span><span class="sxs-lookup"><span data-stu-id="2c972-112">Members</span></span>

<span data-ttu-id="2c972-113">**MDM \_ Policy \_ Config01 \_ ActiveXControls02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2c972-113">The **MDM\_Policy\_Config01\_ActiveXControls02** class has these types of members:</span></span>

-   [<span data-ttu-id="2c972-114">屬性</span><span class="sxs-lookup"><span data-stu-id="2c972-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c972-115">屬性</span><span class="sxs-lookup"><span data-stu-id="2c972-115">Properties</span></span>

<span data-ttu-id="2c972-116">**MDM \_ Policy \_ Config01 \_ ActiveXControls02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2c972-116">The **MDM\_Policy\_Config01\_ActiveXControls02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2c972-117">ApprovedInstallationSites</span><span class="sxs-lookup"><span data-stu-id="2c972-117">ApprovedInstallationSites</span></span>](/windows/client-management/mdm/policy-csp-activexcontrols#activexcontrols-approvedinstallationsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c972-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c972-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c972-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2c972-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2c972-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2c972-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c972-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c972-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c972-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c972-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c972-123">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2c972-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2c972-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2c972-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c972-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c972-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c972-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c972-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c972-127">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2c972-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c972-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c972-128">Requirements</span></span>



| <span data-ttu-id="2c972-129">需求</span><span class="sxs-lookup"><span data-stu-id="2c972-129">Requirement</span></span> | <span data-ttu-id="2c972-130">值</span><span class="sxs-lookup"><span data-stu-id="2c972-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c972-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c972-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2c972-132">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c972-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2c972-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c972-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2c972-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="2c972-134">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2c972-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="2c972-135">Namespace</span></span><br/>                | <span data-ttu-id="2c972-136">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="2c972-136">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2c972-137">MOF</span><span class="sxs-lookup"><span data-stu-id="2c972-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c972-138"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c972-138"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c972-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2c972-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c972-140"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c972-140"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

