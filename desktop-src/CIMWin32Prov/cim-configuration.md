---
description: CIM \_ 設定物件允許將 cim 設定物件中 (定義的參數集群組 \_) 和一個或多個 managed 系統專案的相依性。
ms.assetid: f597fe78-be50-4d31-b1eb-d219acaf1751
ms.tgt_platform: multiple
title: CIM_Configuration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Configuration
- CIM_Configuration.Caption
- CIM_Configuration.Description
- CIM_Configuration.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c069f5c7186d08f01b54fe02c0568dbb4ff43d26
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688979"
---
# <a name="cim_configuration-class"></a><span data-ttu-id="0fc2b-103">CIM 設定 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="0fc2b-103">CIM\_Configuration class</span></span>

<span data-ttu-id="0fc2b-104">Cim 設定物件允許將 [**cim \_ 設定**](cim-setting.md)物件中 (定義的參數集群組) 和一個或多個 managed 系統專案的相依性。 **\_**</span><span class="sxs-lookup"><span data-stu-id="0fc2b-104">The **CIM\_Configuration** object allows the grouping of parameter sets (defined in [**CIM\_Setting**](cim-setting.md) objects) and dependencies for one or more managed system elements.</span></span> <span data-ttu-id="0fc2b-105">此物件代表受管理系統元素的特定行為或所需的功能狀態。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-105">This object represents a certain behavior, or a desired functional state for the managed system elements.</span></span> <span data-ttu-id="0fc2b-106">所需的功能狀態通常是由外部需求（例如時間或位置）所驅動。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-106">The desired functional state is typically driven by external requirements, such as time or location.</span></span> <span data-ttu-id="0fc2b-107">例如，若要從家裡連線到郵件系統，則會有數據機的相依性;然而，網路介面卡的相依性存在於工作中。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-107">For example, to connect to a mail system from home, a dependency on a modem exists; whereas, a dependency on a network adapter exists at work.</span></span> <span data-ttu-id="0fc2b-108">適用于相關邏輯裝置的設定 (在此範例中，您可以透過 **CIM \_** 設定來定義和匯總 POTS 數據機和網路介面卡) 。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-108">Settings for the pertinent logical devices (in this example, POTS modem and network adapter) can be defined and aggregated by **CIM\_Configuration**.</span></span> <span data-ttu-id="0fc2b-109">因此，您可以藉由將相關相依性和 [**CIM \_ 設定**](cim-setting.md) 物件分組，來定義兩個「連接到郵件」設定。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-109">Therefore, two "Connect to Mail" configurations can be defined by grouping the relevant dependencies and [**CIM\_Setting**](cim-setting.md) objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0fc2b-110">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0fc2b-111">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0fc2b-112">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0fc2b-113">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fc2b-114">語法</span><span class="sxs-lookup"><span data-stu-id="0fc2b-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{4C51D7AE-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_Configuration
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="0fc2b-115">成員</span><span class="sxs-lookup"><span data-stu-id="0fc2b-115">Members</span></span>

<span data-ttu-id="0fc2b-116">**CIM 設定 \_** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0fc2b-116">The **CIM\_Configuration** class has these types of members:</span></span>

-   [<span data-ttu-id="0fc2b-117">屬性</span><span class="sxs-lookup"><span data-stu-id="0fc2b-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0fc2b-118">屬性</span><span class="sxs-lookup"><span data-stu-id="0fc2b-118">Properties</span></span>

<span data-ttu-id="0fc2b-119">**CIM 設定 \_** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-119">The **CIM\_Configuration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0fc2b-120">**標題**</span><span class="sxs-lookup"><span data-stu-id="0fc2b-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fc2b-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0fc2b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fc2b-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0fc2b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fc2b-123">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="0fc2b-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0fc2b-124">**CIM \_** 設定物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-124">Short textual description of the **CIM\_Configuration** object.</span></span>

</dd> <dt>

<span data-ttu-id="0fc2b-125">**說明**</span><span class="sxs-lookup"><span data-stu-id="0fc2b-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fc2b-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0fc2b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fc2b-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0fc2b-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fc2b-128">**CIM \_** 設定物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-128">Textual description of the **CIM\_Configuration** object.</span></span>

</dd> <dt>

<span data-ttu-id="0fc2b-129">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0fc2b-129">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fc2b-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0fc2b-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fc2b-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0fc2b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fc2b-132">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="0fc2b-132">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0fc2b-133">已知 **CIM \_** 設定物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-133">Label by which the **CIM\_Configuration** object is known.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fc2b-134">備註</span><span class="sxs-lookup"><span data-stu-id="0fc2b-134">Remarks</span></span>

<span data-ttu-id="0fc2b-135">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-135">WMI does not implement this class.</span></span>

<span data-ttu-id="0fc2b-136">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0fc2b-137">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0fc2b-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fc2b-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fc2b-138">Requirements</span></span>



| <span data-ttu-id="0fc2b-139">需求</span><span class="sxs-lookup"><span data-stu-id="0fc2b-139">Requirement</span></span> | <span data-ttu-id="0fc2b-140">值</span><span class="sxs-lookup"><span data-stu-id="0fc2b-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fc2b-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0fc2b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0fc2b-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fc2b-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0fc2b-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0fc2b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0fc2b-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fc2b-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0fc2b-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="0fc2b-145">Namespace</span></span><br/>                | <span data-ttu-id="0fc2b-146">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0fc2b-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0fc2b-147">MOF</span><span class="sxs-lookup"><span data-stu-id="0fc2b-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0fc2b-148"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0fc2b-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0fc2b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="0fc2b-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fc2b-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fc2b-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

