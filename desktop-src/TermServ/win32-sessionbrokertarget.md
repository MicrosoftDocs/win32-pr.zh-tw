---
title: Win32_SessionBrokerTarget 類別
description: 定義會話 broker 目標的查詢。
ms.assetid: 35de25da-cb89-4836-be14-9544b1264248
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerTarget 類別遠端桌面服務
- Win32_SessionBrokerTarget 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTarget
- Win32_SessionBrokerTarget.PluginName
- Win32_SessionBrokerTarget.TargetName
- Win32_SessionBrokerTarget.FarmName
- Win32_SessionBrokerTarget.Guid
- Win32_SessionBrokerTarget.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ceca0df64eeb9cd285737fee7c6ca6fa3a2e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844303"
---
# <a name="win32_sessionbrokertarget-class"></a><span data-ttu-id="36aea-105">Win32 \_ SessionBrokerTarget 類別</span><span class="sxs-lookup"><span data-stu-id="36aea-105">Win32\_SessionBrokerTarget class</span></span>

<span data-ttu-id="36aea-106">定義會話 broker 目標的查詢。</span><span class="sxs-lookup"><span data-stu-id="36aea-106">Defines the query for a session broker target.</span></span>

<span data-ttu-id="36aea-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="36aea-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="36aea-108">語法</span><span class="sxs-lookup"><span data-stu-id="36aea-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERTARGET_Prov"), AMENDMENT]
class Win32_SessionBrokerTarget
{
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a><span data-ttu-id="36aea-109">成員</span><span class="sxs-lookup"><span data-stu-id="36aea-109">Members</span></span>

<span data-ttu-id="36aea-110">**Win32 \_ SessionBrokerTarget** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="36aea-110">The **Win32\_SessionBrokerTarget** class has these types of members:</span></span>

-   [<span data-ttu-id="36aea-111">屬性</span><span class="sxs-lookup"><span data-stu-id="36aea-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36aea-112">屬性</span><span class="sxs-lookup"><span data-stu-id="36aea-112">Properties</span></span>

<span data-ttu-id="36aea-113">**Win32 \_ SessionBrokerTarget** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="36aea-113">The **Win32\_SessionBrokerTarget** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36aea-114">**環境**</span><span class="sxs-lookup"><span data-stu-id="36aea-114">**Environment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36aea-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36aea-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36aea-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36aea-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36aea-117">環境名稱。</span><span class="sxs-lookup"><span data-stu-id="36aea-117">The environment name.</span></span> <span data-ttu-id="36aea-118">如果虛擬機器 (VM) 目標，這可能是 VM 主機名稱。</span><span class="sxs-lookup"><span data-stu-id="36aea-118">In the case of a virtual machine (VM) target, this could be the VM host name.</span></span>

</dd> <dt>

<span data-ttu-id="36aea-119">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="36aea-119">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36aea-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36aea-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36aea-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36aea-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36aea-122">目標所屬伺服器陣列的名稱。</span><span class="sxs-lookup"><span data-stu-id="36aea-122">The name of the farm the target belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="36aea-123">**Guid**</span><span class="sxs-lookup"><span data-stu-id="36aea-123">**Guid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36aea-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36aea-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36aea-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36aea-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36aea-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="36aea-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="36aea-127">GUID (是否有目標的任何) 。</span><span class="sxs-lookup"><span data-stu-id="36aea-127">The GUID (if any) of the target.</span></span>

</dd> <dt>

<span data-ttu-id="36aea-128">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="36aea-128">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36aea-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36aea-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36aea-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36aea-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36aea-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="36aea-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="36aea-132">外掛程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="36aea-132">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="36aea-133">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="36aea-133">**TargetName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36aea-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36aea-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36aea-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36aea-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36aea-136">目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="36aea-136">The name of the target.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="36aea-137">範例</span><span class="sxs-lookup"><span data-stu-id="36aea-137">Examples</span></span>

<span data-ttu-id="36aea-138">下列查詢字串示範如何 \_ 在查詢中使用 Win32 SessionBrokerTarget 類別。</span><span class="sxs-lookup"><span data-stu-id="36aea-138">The following query string demonstrates how the Win32\_SessionBrokerTarget class is used in a query.</span></span>


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerTarget WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a><span data-ttu-id="36aea-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="36aea-139">Requirements</span></span>



| <span data-ttu-id="36aea-140">需求</span><span class="sxs-lookup"><span data-stu-id="36aea-140">Requirement</span></span> | <span data-ttu-id="36aea-141">值</span><span class="sxs-lookup"><span data-stu-id="36aea-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36aea-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36aea-142">Minimum supported client</span></span><br/> | <span data-ttu-id="36aea-143">都不支援</span><span class="sxs-lookup"><span data-stu-id="36aea-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="36aea-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36aea-144">Minimum supported server</span></span><br/> | <span data-ttu-id="36aea-145">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="36aea-145">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="36aea-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="36aea-146">Namespace</span></span><br/>                | <span data-ttu-id="36aea-147">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="36aea-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="36aea-148">MOF</span><span class="sxs-lookup"><span data-stu-id="36aea-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36aea-149"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="36aea-149"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="36aea-150">DLL</span><span class="sxs-lookup"><span data-stu-id="36aea-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36aea-151"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36aea-151"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

