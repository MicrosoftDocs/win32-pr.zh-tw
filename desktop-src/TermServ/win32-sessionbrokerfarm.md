---
title: Win32_SessionBrokerFarm 類別
description: 定義會話代理程式伺服器陣列的查詢。
ms.assetid: 55a2a7ea-e891-4723-b919-ee3c908eaffb
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerFarm 類別遠端桌面服務
- Win32_SessionBrokerFarm 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarm
- Win32_SessionBrokerFarm.PluginName
- Win32_SessionBrokerFarm.FarmName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a3ccbb5e1e08a036fb9973d552db73ee1607c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465293"
---
# <a name="win32_sessionbrokerfarm-class"></a><span data-ttu-id="0fd47-105">Win32 \_ SessionBrokerFarm 類別</span><span class="sxs-lookup"><span data-stu-id="0fd47-105">Win32\_SessionBrokerFarm class</span></span>

<span data-ttu-id="0fd47-106">定義會話代理程式伺服器陣列的查詢。</span><span class="sxs-lookup"><span data-stu-id="0fd47-106">Defines the query for a session broker farm.</span></span>

<span data-ttu-id="0fd47-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0fd47-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd47-108">語法</span><span class="sxs-lookup"><span data-stu-id="0fd47-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARM_Prov"), AMENDMENT]
class Win32_SessionBrokerFarm
{
  string PluginName;
  string FarmName;
};
```

## <a name="members"></a><span data-ttu-id="0fd47-109">成員</span><span class="sxs-lookup"><span data-stu-id="0fd47-109">Members</span></span>

<span data-ttu-id="0fd47-110">**Win32 \_ SessionBrokerFarm** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0fd47-110">The **Win32\_SessionBrokerFarm** class has these types of members:</span></span>

-   [<span data-ttu-id="0fd47-111">屬性</span><span class="sxs-lookup"><span data-stu-id="0fd47-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0fd47-112">屬性</span><span class="sxs-lookup"><span data-stu-id="0fd47-112">Properties</span></span>

<span data-ttu-id="0fd47-113">**Win32 \_ SessionBrokerFarm** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0fd47-113">The **Win32\_SessionBrokerFarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0fd47-114">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="0fd47-114">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fd47-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0fd47-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fd47-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0fd47-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fd47-117">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0fd47-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0fd47-118">需要查詢的會話代理人伺服器陣列的名稱。</span><span class="sxs-lookup"><span data-stu-id="0fd47-118">The name of the session broker farm that needs to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="0fd47-119">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="0fd47-119">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fd47-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0fd47-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fd47-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0fd47-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fd47-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0fd47-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0fd47-123">外掛程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="0fd47-123">The name of the plug-in.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="0fd47-124">範例</span><span class="sxs-lookup"><span data-stu-id="0fd47-124">Examples</span></span>

<span data-ttu-id="0fd47-125">下列查詢字串示範如何在查詢中使用 **Win32 \_ SessionBrokerFarm** 類別。</span><span class="sxs-lookup"><span data-stu-id="0fd47-125">The following query string demonstrates how the **Win32\_SessionBrokerFarm** class is used in a query.</span></span>


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerFarm WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a><span data-ttu-id="0fd47-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fd47-126">Requirements</span></span>



| <span data-ttu-id="0fd47-127">需求</span><span class="sxs-lookup"><span data-stu-id="0fd47-127">Requirement</span></span> | <span data-ttu-id="0fd47-128">值</span><span class="sxs-lookup"><span data-stu-id="0fd47-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd47-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0fd47-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd47-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="0fd47-130">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0fd47-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0fd47-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd47-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0fd47-132">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="0fd47-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="0fd47-133">Namespace</span></span><br/>                | <span data-ttu-id="0fd47-134">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="0fd47-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="0fd47-135">MOF</span><span class="sxs-lookup"><span data-stu-id="0fd47-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0fd47-136"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="0fd47-136"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0fd47-137">DLL</span><span class="sxs-lookup"><span data-stu-id="0fd47-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fd47-138"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fd47-138"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

