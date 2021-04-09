---
description: CIM \_ 檢查類別代表一種條件或特性，此條件或特性在定義的環境中應該是 true，或是由 cim 系統內容類別的實例所設定的範圍 \_ 。
ms.assetid: f7862fe5-4412-4d57-b5fa-03c939ddba02
ms.tgt_platform: multiple
title: CIM_Check 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Check
- CIM_Check.CheckID
- CIM_Check.Caption
- CIM_Check.Description
- CIM_Check.CheckMode
- CIM_Check.Name
- CIM_Check.TargetOperatingSystem
- CIM_Check.Version
- CIM_Check.SoftwareElementID
- CIM_Check.SoftwareElementState
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cbe742fb4cd2510ec4c502f89b3b3b1eb79bc47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847406"
---
# <a name="cim_check-class"></a><span data-ttu-id="9c6f3-103">CIM \_ 檢查類別</span><span class="sxs-lookup"><span data-stu-id="9c6f3-103">CIM\_Check class</span></span>

<span data-ttu-id="9c6f3-104">**Cim \_ 檢查** 類別代表一種條件或特性，此條件或特性在定義的環境中應該是 true，或是由 [**cim 系統 \_ 環境**](cim-computersystem.md)類別的實例所設定的範圍。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-104">The **CIM\_Check** class represents a condition or characteristic that is expected to be true in an environment defined or scoped by an instance of a [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span> <span data-ttu-id="9c6f3-105">與特定軟體專案相關聯的檢查會使用 [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md)關聯的 [**階段**] 屬性組織成兩個群組的其中一個。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-105">The checks associated with a particular software element are organized into one of two groups using the **Phase** property of the [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association.</span></span>

<span data-ttu-id="9c6f3-106">當軟體專案在特定環境中時，預期會滿足的條件就稱為「狀態」條件。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-106">Conditions that are expected to be satisfied when a software element is in a particular environment are known as in-state conditions.</span></span> <span data-ttu-id="9c6f3-107">將目前的軟體專案轉換為下一個狀態時，必須滿足的條件就稱為「下一州」條件。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-107">Conditions that must be satisfied to transition the current software element to its next state are known as next-state conditions.</span></span>

<span data-ttu-id="9c6f3-108">[**Cim 系統 \_ 系統**](cim-computersystem.md)物件代表已安裝 [**cim \_ SoftwareElement**](cim-softwareelement.md)或將安裝 **cim \_ SoftwareElement** 的環境。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-108">A [**CIM\_ComputerSystem**](cim-computersystem.md) object represents the environment in which a [**CIM\_SoftwareElement**](cim-softwareelement.md) is already installed, or in which a **CIM\_SoftwareElement** will be installed.</span></span> <span data-ttu-id="9c6f3-109">如果已安裝軟體專案，則會使用 [**cim \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) 關聯來識別代表「環境」的 cim 程式 **識別碼 \_** 物件。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-109">For the case in which a software element is already installed, the [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) association is used to identify the **CIM\_ComputerSystem** object that represents the "environment."</span></span> <span data-ttu-id="9c6f3-110">當軟體專案發佈並安裝在不同的電腦上時，目標系統 **的 \_ CIM** 系統元件物件就是環境。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-110">When a software element is being distributed and installed on a different computer, the **CIM\_ComputerSystem** object for the targeted system is the environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9c6f3-111">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9c6f3-112">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9c6f3-113">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9c6f3-114">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c6f3-115">語法</span><span class="sxs-lookup"><span data-stu-id="9c6f3-115">Syntax</span></span>

``` syntax
[UUID("{7A9135CA-DB21-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Check
{
  string  CheckID;
  string  Caption;
  string  Description;
  boolean CheckMode;
  string  Name;
  uint16  TargetOperatingSystem;
  string  Version;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
};
```

## <a name="members"></a><span data-ttu-id="9c6f3-116">成員</span><span class="sxs-lookup"><span data-stu-id="9c6f3-116">Members</span></span>

<span data-ttu-id="9c6f3-117">**CIM \_ 檢查** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9c6f3-117">The **CIM\_Check** class has these types of members:</span></span>

-   [<span data-ttu-id="9c6f3-118">方法</span><span class="sxs-lookup"><span data-stu-id="9c6f3-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="9c6f3-119">屬性</span><span class="sxs-lookup"><span data-stu-id="9c6f3-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9c6f3-120">方法</span><span class="sxs-lookup"><span data-stu-id="9c6f3-120">Methods</span></span>

<span data-ttu-id="9c6f3-121">**CIM \_ 檢查** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-121">The **CIM\_Check** class has these methods.</span></span>



| <span data-ttu-id="9c6f3-122">方法</span><span class="sxs-lookup"><span data-stu-id="9c6f3-122">Method</span></span>                                             | <span data-ttu-id="9c6f3-123">描述</span><span class="sxs-lookup"><span data-stu-id="9c6f3-123">Description</span></span>                                                   |
|:---------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="9c6f3-124">**調用**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-124">**Invoke**</span></span>](invoke-method-in-class-cim-check.md) | <span data-ttu-id="9c6f3-125">採取特定動作。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-125">Takes a particular action.</span></span> <span data-ttu-id="9c6f3-126">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9c6f3-127">屬性</span><span class="sxs-lookup"><span data-stu-id="9c6f3-127">Properties</span></span>

<span data-ttu-id="9c6f3-128">**CIM \_ 檢查** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-128">The **CIM\_Check** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c6f3-129">**標題**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f3-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c6f3-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-132">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-132">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9c6f3-133">主體的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-133">A short textual description of the subject.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f3-134">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-134">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f3-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c6f3-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-137">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9c6f3-138">與其他索引鍵搭配使用來唯一識別檢查的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-138">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f3-139">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-139">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f3-140">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c6f3-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f3-142">若 **為 TRUE**，則條件應該存在於環境中。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-142">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="9c6f3-143">例如，檔案應該在系統上，因此叫 [**用方法應該**](invoke-method-in-class-cim-check.md) 傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-143">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="9c6f3-144">如果 **為 FALSE**，則條件不應該存在。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-144">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="9c6f3-145">例如，檔案不在系統上，因此 [**Invoke**](invoke-method-in-class-cim-check.md) 方法應該傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-145">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f3-146">**說明**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f3-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c6f3-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c6f3-149">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-149">A description of the objects.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f3-150">**名稱**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-150">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f3-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c6f3-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-153">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Name**") 、 [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-153">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9c6f3-154">用來識別軟體元素的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-154">Name used to identify the software element.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f3-155">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-155">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f3-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c6f3-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-158">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementID**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-158">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9c6f3-159">這是此軟體元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-159">This is an identifier for this software element.</span></span>

</dd> <dt>

<span data-ttu-id="9c6f3-160">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-160">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f3-161">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c6f3-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-163">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9c6f3-163">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9c6f3-164">軟體元素的軟體專案狀態。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-164">The software element state of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="9c6f3-165"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-165"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-166">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-166">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="9c6f3-167"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-167"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-168">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-168">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="9c6f3-169"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-169"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-170">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-170">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="9c6f3-171"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-171"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-172">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-172">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c6f3-173">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-173">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f3-174">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c6f3-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-176">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| Software Component Information \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="9c6f3-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="9c6f3-177">Software 元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-177">Target operating system of the software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c6f3-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9c6f3-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="9c6f3-180"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-180"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-181">Mac OS</span><span class="sxs-lookup"><span data-stu-id="9c6f3-181">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="9c6f3-182"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-182"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-183">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="9c6f3-183">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="9c6f3-184"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-184"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="9c6f3-185"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-185"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="9c6f3-186"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-186"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="9c6f3-187"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-187"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-188">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="9c6f3-188">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="9c6f3-189"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-189"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-190">HP-UX</span><span class="sxs-lookup"><span data-stu-id="9c6f3-190">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="9c6f3-191"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-191"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="9c6f3-192"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-192"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="9c6f3-193"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-193"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="9c6f3-194"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-194"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="9c6f3-195"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-195"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-196">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-196">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="9c6f3-197"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-197"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="9c6f3-198"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-198"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-199">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="9c6f3-199">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="9c6f3-200"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-200"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-201">Windows 95</span><span class="sxs-lookup"><span data-stu-id="9c6f3-201">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="9c6f3-202"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-202"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-203">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9c6f3-203">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="9c6f3-204"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-204"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-205">Windows NT</span><span class="sxs-lookup"><span data-stu-id="9c6f3-205">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="9c6f3-206"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-206"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-207">Windows CE</span><span class="sxs-lookup"><span data-stu-id="9c6f3-207">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="9c6f3-208"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-208"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-209">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="9c6f3-209">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="9c6f3-210"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-210"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="9c6f3-211"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-211"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="9c6f3-212"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-212"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="9c6f3-213"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-213"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="9c6f3-214"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-214"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="9c6f3-215"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-215"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="9c6f3-216"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-216"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="9c6f3-217"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-217"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="9c6f3-218"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-218"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="9c6f3-219"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-219"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="9c6f3-220"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-220"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="9c6f3-221"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-221"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-222">系列</span><span class="sxs-lookup"><span data-stu-id="9c6f3-222">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="9c6f3-223"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-223"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-224">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="9c6f3-224">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="9c6f3-225"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-225"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-226">將 NT</span><span class="sxs-lookup"><span data-stu-id="9c6f3-226">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="9c6f3-227"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-227"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-228">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="9c6f3-228">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="9c6f3-229"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-229"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="9c6f3-230"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-230"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="9c6f3-231"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-231"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="9c6f3-232"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-232"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="9c6f3-233"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-233"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="9c6f3-234"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-234"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-235">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="9c6f3-235">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="9c6f3-236"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-236"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="9c6f3-237"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-237"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="9c6f3-238"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-238"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="9c6f3-239"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-239"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-240">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="9c6f3-240">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="9c6f3-241"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-241"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="9c6f3-242"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-242"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="9c6f3-243"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-243"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="9c6f3-244"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-244"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="9c6f3-245"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-245"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="9c6f3-246"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-246"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="9c6f3-247"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-247"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="9c6f3-248"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-248"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="9c6f3-249"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-249"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="9c6f3-250"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-250"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="9c6f3-251"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-251"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="9c6f3-252">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="9c6f3-252">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="9c6f3-253"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-253"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="9c6f3-254"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-254"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="9c6f3-255"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-255"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="9c6f3-256"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-256"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="9c6f3-257"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="9c6f3-257"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9c6f3-258">**版本**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-258">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6f3-259">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9c6f3-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c6f3-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c6f3-261">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Version**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="9c6f3-261">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="9c6f3-262">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-262">Version of the operation.</span></span>

<span data-ttu-id="9c6f3-263">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="9c6f3-263">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="9c6f3-264"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="9c6f3-264"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="9c6f3-265"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="9c6f3-265"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c6f3-266">備註</span><span class="sxs-lookup"><span data-stu-id="9c6f3-266">Remarks</span></span>

<span data-ttu-id="9c6f3-267">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-267">WMI does not implement this class.</span></span> <span data-ttu-id="9c6f3-268">如需衍生自 **CIM \_ 檢查** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-268">For more information about classes derived from **CIM\_Check**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9c6f3-269">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-269">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9c6f3-270">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9c6f3-270">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c6f3-271">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c6f3-271">Requirements</span></span>



| <span data-ttu-id="9c6f3-272">需求</span><span class="sxs-lookup"><span data-stu-id="9c6f3-272">Requirement</span></span> | <span data-ttu-id="9c6f3-273">值</span><span class="sxs-lookup"><span data-stu-id="9c6f3-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c6f3-274">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c6f3-274">Minimum supported client</span></span><br/> | <span data-ttu-id="9c6f3-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c6f3-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9c6f3-276">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c6f3-276">Minimum supported server</span></span><br/> | <span data-ttu-id="9c6f3-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c6f3-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9c6f3-278">命名空間</span><span class="sxs-lookup"><span data-stu-id="9c6f3-278">Namespace</span></span><br/>                | <span data-ttu-id="9c6f3-279">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9c6f3-279">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9c6f3-280">MOF</span><span class="sxs-lookup"><span data-stu-id="9c6f3-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c6f3-281"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c6f3-281"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c6f3-282">DLL</span><span class="sxs-lookup"><span data-stu-id="9c6f3-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c6f3-283"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c6f3-283"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

