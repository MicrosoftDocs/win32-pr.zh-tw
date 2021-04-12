---
title: MDM_Policy_Config01_RemoteShell02 類別
description: MDM \_ Policy \_ Config01 RemoteShell02 類別會設定 \_ 遠端 shell 原則。
ms.assetid: 7026fadb-ec6a-4696-a24c-1b1e071b94b0
keywords:
- MDM_Policy_Config01_RemoteShell02 類別
- MDM_Policy_Config01_RemoteShell02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteShell02
- MDM_Policy_Config01_RemoteShell02.InstanceID
- MDM_Policy_Config01_RemoteShell02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c318b0c6f23e92d90091495fdc25993d6958ca56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465453"
---
# <a name="mdm_policy_config01_remoteshell02-class"></a><span data-ttu-id="c7672-105">MDM \_ 原則 \_ Config01 \_ RemoteShell02 類別</span><span class="sxs-lookup"><span data-stu-id="c7672-105">MDM\_Policy\_Config01\_RemoteShell02 class</span></span>

<span data-ttu-id="c7672-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="c7672-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c7672-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="c7672-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c7672-108">MDM \_ Policy \_ Config01 RemoteShell02 類別會設定 \_ 遠端 shell 原則。</span><span class="sxs-lookup"><span data-stu-id="c7672-108">The MDM\_Policy\_Config01\_RemoteShell02 class configures the remote shell policies.</span></span>

<span data-ttu-id="c7672-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c7672-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7672-110">語法</span><span class="sxs-lookup"><span data-stu-id="c7672-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteShell02
{
  string InstanceID;
  string ParentID;
  string AllowRemoteShellAccess;
  string MaxConcurrentUsers;
  string SpecifyIdleTimeout;
  string SpecifyMaxMemory;
  string SpecifyMaxProcesses;
  string SpecifyMaxRemoteShells;
  string SpecifyShellTimeout;
};
```

## <a name="members"></a><span data-ttu-id="c7672-111">成員</span><span class="sxs-lookup"><span data-stu-id="c7672-111">Members</span></span>

<span data-ttu-id="c7672-112">**MDM \_ Policy \_ Config01 \_ RemoteShell02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c7672-112">The **MDM\_Policy\_Config01\_RemoteShell02** class has these types of members:</span></span>

-   [<span data-ttu-id="c7672-113">屬性</span><span class="sxs-lookup"><span data-stu-id="c7672-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7672-114">屬性</span><span class="sxs-lookup"><span data-stu-id="c7672-114">Properties</span></span>

<span data-ttu-id="c7672-115">**MDM \_ Policy \_ Config01 \_ RemoteShell02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c7672-115">The **MDM\_Policy\_Config01\_RemoteShell02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c7672-116">AllowRemoteShellAccess</span><span class="sxs-lookup"><span data-stu-id="c7672-116">AllowRemoteShellAccess</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-allowremoteshellaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7672-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7672-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7672-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c7672-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c7672-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c7672-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7672-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7672-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7672-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7672-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7672-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c7672-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c7672-123">MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="c7672-123">MaxConcurrentUsers</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-maxconcurrentusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7672-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7672-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7672-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c7672-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c7672-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c7672-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7672-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7672-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7672-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7672-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7672-129">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c7672-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c7672-130">SpecifyIdleTimeout</span><span class="sxs-lookup"><span data-stu-id="c7672-130">SpecifyIdleTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyidletimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7672-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7672-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7672-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c7672-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c7672-133">SpecifyMaxMemory</span><span class="sxs-lookup"><span data-stu-id="c7672-133">SpecifyMaxMemory</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxmemory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7672-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7672-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7672-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c7672-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c7672-136">SpecifyMaxProcesses</span><span class="sxs-lookup"><span data-stu-id="c7672-136">SpecifyMaxProcesses</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7672-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7672-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7672-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c7672-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c7672-139">SpecifyMaxRemoteShells</span><span class="sxs-lookup"><span data-stu-id="c7672-139">SpecifyMaxRemoteShells</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxremoteshells)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7672-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7672-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7672-141">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c7672-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c7672-142">SpecifyShellTimeout</span><span class="sxs-lookup"><span data-stu-id="c7672-142">SpecifyShellTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyshelltimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7672-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7672-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7672-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c7672-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7672-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7672-145">Requirements</span></span>



| <span data-ttu-id="c7672-146">需求</span><span class="sxs-lookup"><span data-stu-id="c7672-146">Requirement</span></span> | <span data-ttu-id="c7672-147">值</span><span class="sxs-lookup"><span data-stu-id="c7672-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7672-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7672-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c7672-149">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7672-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7672-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7672-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c7672-151">都不支援</span><span class="sxs-lookup"><span data-stu-id="c7672-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c7672-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="c7672-152">Namespace</span></span><br/>                | <span data-ttu-id="c7672-153">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="c7672-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c7672-154">MOF</span><span class="sxs-lookup"><span data-stu-id="c7672-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7672-155"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7672-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7672-156">DLL</span><span class="sxs-lookup"><span data-stu-id="c7672-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7672-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7672-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

