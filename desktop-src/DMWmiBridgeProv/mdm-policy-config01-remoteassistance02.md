---
title: MDM_Policy_Config01_RemoteAssistance02 類別
description: MDM \_ Policy \_ Config01 RemoteAssistance02 類別會設定 \_ 遠端協助原則。
ms.assetid: bcc6c570-66d9-4dcd-b7f2-2d03733c0bcb
keywords:
- MDM_Policy_Config01_RemoteAssistance02 類別
- MDM_Policy_Config01_RemoteAssistance02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteAssistance02
- MDM_Policy_Config01_RemoteAssistance02.InstanceID
- MDM_Policy_Config01_RemoteAssistance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aceadb2eb784e72e4e332cdd34df44d779c99e97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843540"
---
# <a name="mdm_policy_config01_remoteassistance02-class"></a><span data-ttu-id="49f33-105">MDM \_ 原則 \_ Config01 \_ RemoteAssistance02 類別</span><span class="sxs-lookup"><span data-stu-id="49f33-105">MDM\_Policy\_Config01\_RemoteAssistance02 class</span></span>

<span data-ttu-id="49f33-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="49f33-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="49f33-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="49f33-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="49f33-108">MDM \_ Policy \_ Config01 RemoteAssistance02 類別會設定 \_ 遠端協助原則。</span><span class="sxs-lookup"><span data-stu-id="49f33-108">The MDM\_Policy\_Config01\_RemoteAssistance02 class configures the remote assistance policies.</span></span>

<span data-ttu-id="49f33-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="49f33-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="49f33-110">語法</span><span class="sxs-lookup"><span data-stu-id="49f33-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteAssistance02
{
  string InstanceID;
  string ParentID;
  string CustomizeWarningMessages;
  string SessionLogging;
  string SolicitedRemoteAssistance;
  string UnsolicitedRemoteAssistance;
};
```

## <a name="members"></a><span data-ttu-id="49f33-111">成員</span><span class="sxs-lookup"><span data-stu-id="49f33-111">Members</span></span>

<span data-ttu-id="49f33-112">**MDM \_ Policy \_ Config01 \_ RemoteAssistance02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="49f33-112">The **MDM\_Policy\_Config01\_RemoteAssistance02** class has these types of members:</span></span>

-   [<span data-ttu-id="49f33-113">屬性</span><span class="sxs-lookup"><span data-stu-id="49f33-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49f33-114">屬性</span><span class="sxs-lookup"><span data-stu-id="49f33-114">Properties</span></span>

<span data-ttu-id="49f33-115">**MDM \_ Policy \_ Config01 \_ RemoteAssistance02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="49f33-115">The **MDM\_Policy\_Config01\_RemoteAssistance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="49f33-116">CustomizeWarningMessages</span><span class="sxs-lookup"><span data-stu-id="49f33-116">CustomizeWarningMessages</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-customizewarningmessages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f33-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49f33-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f33-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="49f33-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="49f33-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="49f33-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f33-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49f33-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f33-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49f33-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f33-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="49f33-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="49f33-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="49f33-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f33-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49f33-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f33-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49f33-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f33-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="49f33-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="49f33-127">SessionLogging</span><span class="sxs-lookup"><span data-stu-id="49f33-127">SessionLogging</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-sessionlogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f33-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49f33-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f33-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="49f33-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="49f33-130">SolicitedRemoteAssistance</span><span class="sxs-lookup"><span data-stu-id="49f33-130">SolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-solicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f33-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49f33-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f33-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="49f33-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="49f33-133">UnsolicitedRemoteAssistance</span><span class="sxs-lookup"><span data-stu-id="49f33-133">UnsolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-unsolicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f33-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49f33-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f33-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="49f33-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49f33-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="49f33-136">Requirements</span></span>



| <span data-ttu-id="49f33-137">需求</span><span class="sxs-lookup"><span data-stu-id="49f33-137">Requirement</span></span> | <span data-ttu-id="49f33-138">值</span><span class="sxs-lookup"><span data-stu-id="49f33-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f33-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49f33-139">Minimum supported client</span></span><br/> | <span data-ttu-id="49f33-140">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49f33-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="49f33-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49f33-141">Minimum supported server</span></span><br/> | <span data-ttu-id="49f33-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="49f33-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="49f33-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="49f33-143">Namespace</span></span><br/>                | <span data-ttu-id="49f33-144">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="49f33-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="49f33-145">MOF</span><span class="sxs-lookup"><span data-stu-id="49f33-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49f33-146"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="49f33-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="49f33-147">DLL</span><span class="sxs-lookup"><span data-stu-id="49f33-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49f33-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49f33-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

