---
description: CIM \_ VersionCompatibilityCheck 類別會指定是否允許建立軟體元素的下一個狀態。
ms.assetid: 3a04c489-e44e-44c7-8945-d6047ba0d6df
ms.tgt_platform: multiple
title: CIM_VersionCompatibilityCheck 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VersionCompatibilityCheck
- CIM_VersionCompatibilityCheck.CheckID
- CIM_VersionCompatibilityCheck.Caption
- CIM_VersionCompatibilityCheck.Description
- CIM_VersionCompatibilityCheck.CheckMode
- CIM_VersionCompatibilityCheck.Name
- CIM_VersionCompatibilityCheck.TargetOperatingSystem
- CIM_VersionCompatibilityCheck.Version
- CIM_VersionCompatibilityCheck.SoftwareElementID
- CIM_VersionCompatibilityCheck.SoftwareElementState
- CIM_VersionCompatibilityCheck.AllowDownVersion
- CIM_VersionCompatibilityCheck.AllowMultipleVersions
- CIM_VersionCompatibilityCheck.Reinstall
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 00a37d52add8c9697371fd0ee8d0a24d9c487f61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936247"
---
# <a name="cim_versioncompatibilitycheck-class"></a><span data-ttu-id="9a810-103">CIM \_ VersionCompatibilityCheck 類別</span><span class="sxs-lookup"><span data-stu-id="9a810-103">CIM\_VersionCompatibilityCheck class</span></span>

<span data-ttu-id="9a810-104">**CIM \_ VersionCompatibilityCheck** 類別會指定是否允許建立軟體元素的下一個狀態。</span><span class="sxs-lookup"><span data-stu-id="9a810-104">The **CIM\_VersionCompatibilityCheck** class specifies whether it is permissible to create the next state of a software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a810-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="9a810-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9a810-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="9a810-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9a810-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9a810-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9a810-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="9a810-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a810-109">語法</span><span class="sxs-lookup"><span data-stu-id="9a810-109">Syntax</span></span>

``` syntax
[UUID("{D368CA4A-DB31-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VersionCompatibilityCheck : CIM_Check
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
  boolean AllowDownVersion;
  boolean AllowMultipleVersions;
  boolean Reinstall;
};
```

## <a name="members"></a><span data-ttu-id="9a810-110">成員</span><span class="sxs-lookup"><span data-stu-id="9a810-110">Members</span></span>

<span data-ttu-id="9a810-111">**CIM \_ VersionCompatibilityCheck** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9a810-111">The **CIM\_VersionCompatibilityCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="9a810-112">方法</span><span class="sxs-lookup"><span data-stu-id="9a810-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9a810-113">屬性</span><span class="sxs-lookup"><span data-stu-id="9a810-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9a810-114">方法</span><span class="sxs-lookup"><span data-stu-id="9a810-114">Methods</span></span>

<span data-ttu-id="9a810-115">**CIM \_ VersionCompatibilityCheck** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9a810-115">The **CIM\_VersionCompatibilityCheck** class has these methods.</span></span>



| <span data-ttu-id="9a810-116">方法</span><span class="sxs-lookup"><span data-stu-id="9a810-116">Method</span></span>                                                                 | <span data-ttu-id="9a810-117">描述</span><span class="sxs-lookup"><span data-stu-id="9a810-117">Description</span></span>                                                   |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="9a810-118">**調用**</span><span class="sxs-lookup"><span data-stu-id="9a810-118">**Invoke**</span></span>](invoke-method-in-class-cim-versioncompatibilitycheck.md) | <span data-ttu-id="9a810-119">採取特定動作。</span><span class="sxs-lookup"><span data-stu-id="9a810-119">Takes a particular action.</span></span> <span data-ttu-id="9a810-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="9a810-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9a810-121">屬性</span><span class="sxs-lookup"><span data-stu-id="9a810-121">Properties</span></span>

<span data-ttu-id="9a810-122">**CIM \_ VersionCompatibilityCheck** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9a810-122">The **CIM\_VersionCompatibilityCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a810-123">**AllowDownVersion**</span><span class="sxs-lookup"><span data-stu-id="9a810-123">**AllowDownVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a810-124">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9a810-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a810-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9a810-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a810-126">若 **為 TRUE**，則不論環境中是否已有較高或更高版本的 software 專案，軟體專案都可以轉換為下一個狀態。</span><span class="sxs-lookup"><span data-stu-id="9a810-126">If **TRUE**, the software element can transition to its next state whether or not if a higher or latter version of the software element already exists in the environment.</span></span>

</dd> <dt>

<span data-ttu-id="9a810-127">**AllowMultipleVersions**</span><span class="sxs-lookup"><span data-stu-id="9a810-127">**AllowMultipleVersions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a810-128">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9a810-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a810-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9a810-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a810-130">控制在系統上設定產品之多個版本的能力。</span><span class="sxs-lookup"><span data-stu-id="9a810-130">Controls the ability to configure multiple versions of a product on a system.</span></span>

</dd> <dt>

<span data-ttu-id="9a810-131">**標題**</span><span class="sxs-lookup"><span data-stu-id="9a810-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a810-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9a810-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a810-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9a810-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a810-134">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="9a810-134">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9a810-135">主體的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="9a810-135">A short textual description of the subject.</span></span>

<span data-ttu-id="9a810-136">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="9a810-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a810-137">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="9a810-137">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a810-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9a810-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a810-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9a810-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a810-140">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="9a810-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9a810-141">與其他索引鍵搭配使用來唯一識別檢查的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a810-141">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="9a810-142">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="9a810-142">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a810-143">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="9a810-143">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a810-144">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9a810-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a810-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9a810-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a810-146">若 **為 TRUE**，則條件應該存在於環境中。</span><span class="sxs-lookup"><span data-stu-id="9a810-146">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="9a810-147">例如，檔案應該在系統上，因此叫 [**用方法應該**](invoke-method-in-class-cim-check.md) 傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="9a810-147">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="9a810-148">如果 **為 FALSE**，則條件不應該存在。</span><span class="sxs-lookup"><span data-stu-id="9a810-148">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="9a810-149">例如，檔案不在系統上，因此 [**Invoke**](invoke-method-in-class-cim-check.md) 方法應該傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9a810-149">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="9a810-150">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="9a810-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a810-151">**說明**</span><span class="sxs-lookup"><span data-stu-id="9a810-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a810-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9a810-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a810-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9a810-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a810-154">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="9a810-154">A description of the objects.</span></span>

<span data-ttu-id="9a810-155">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="9a810-155">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a810-156">**名稱**</span><span class="sxs-lookup"><span data-stu-id="9a810-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a810-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9a810-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a810-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9a810-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a810-159">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Name**") 、 [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="9a810-159">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9a810-160">用來識別軟體元素的名稱</span><span class="sxs-lookup"><span data-stu-id="9a810-160">Name used to identify the software element</span></span>

<span data-ttu-id="9a810-161">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="9a810-161">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a810-162">**安裝**</span><span class="sxs-lookup"><span data-stu-id="9a810-162">**Reinstall**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a810-163">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9a810-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a810-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9a810-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a810-165">若 **為 TRUE**，則不論環境中是否已有相同版本的軟體專案，軟體專案都可以轉換為下一個狀態。</span><span class="sxs-lookup"><span data-stu-id="9a810-165">If **TRUE**, the software element can transition to its next state whether or not a software element of the same version already exists in the environment.</span></span>

</dd> <dt>

<span data-ttu-id="9a810-166">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="9a810-166">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a810-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9a810-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a810-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9a810-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a810-169">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementID**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="9a810-169">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9a810-170">這是此軟體元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a810-170">This is an identifier for this software element.</span></span>

<span data-ttu-id="9a810-171">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="9a810-171">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a810-172">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="9a810-172">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a810-173">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9a810-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9a810-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9a810-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a810-175">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9a810-175">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9a810-176">軟體元素的軟體專案狀態。</span><span class="sxs-lookup"><span data-stu-id="9a810-176">The software element state of a software element.</span></span>

<span data-ttu-id="9a810-177">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="9a810-177">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="9a810-178"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="9a810-178"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="9a810-179"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="9a810-179"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="9a810-180"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="9a810-180"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="9a810-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="9a810-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9a810-182">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="9a810-182">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a810-183">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9a810-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9a810-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9a810-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a810-185">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| Software Component Information \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="9a810-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="9a810-186">Software 元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="9a810-186">Target operating system of the software element.</span></span>

<span data-ttu-id="9a810-187">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="9a810-187">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9a810-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="9a810-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9a810-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="9a810-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="9a810-190"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="9a810-190"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-191">Mac OS</span><span class="sxs-lookup"><span data-stu-id="9a810-191">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="9a810-192"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="9a810-192"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-193">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="9a810-193">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="9a810-194"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="9a810-194"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="9a810-195"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="9a810-195"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="9a810-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="9a810-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="9a810-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="9a810-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-198">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="9a810-198">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="9a810-199"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="9a810-199"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-200">HP-UX</span><span class="sxs-lookup"><span data-stu-id="9a810-200">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="9a810-201"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="9a810-201"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="9a810-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="9a810-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="9a810-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="9a810-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="9a810-204"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="9a810-204"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="9a810-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="9a810-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-206">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="9a810-206">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="9a810-207"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="9a810-207"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="9a810-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="9a810-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-209">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="9a810-209">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="9a810-210"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="9a810-210"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-211">Windows 95</span><span class="sxs-lookup"><span data-stu-id="9a810-211">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="9a810-212"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="9a810-212"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-213">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9a810-213">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="9a810-214"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="9a810-214"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-215">Windows NT</span><span class="sxs-lookup"><span data-stu-id="9a810-215">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="9a810-216"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="9a810-216"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-217">Windows CE</span><span class="sxs-lookup"><span data-stu-id="9a810-217">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="9a810-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="9a810-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-219">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="9a810-219">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="9a810-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="9a810-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="9a810-221"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="9a810-221"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="9a810-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="9a810-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="9a810-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="9a810-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="9a810-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="9a810-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="9a810-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="9a810-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="9a810-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="9a810-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="9a810-227"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="9a810-227"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="9a810-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="9a810-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="9a810-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="9a810-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="9a810-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="9a810-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="9a810-231"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="9a810-231"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-232">系列</span><span class="sxs-lookup"><span data-stu-id="9a810-232">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="9a810-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="9a810-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-234">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="9a810-234">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="9a810-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="9a810-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-236">將 NT</span><span class="sxs-lookup"><span data-stu-id="9a810-236">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="9a810-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="9a810-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-238">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="9a810-238">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="9a810-239"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="9a810-239"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="9a810-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="9a810-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="9a810-241"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="9a810-241"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="9a810-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="9a810-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="9a810-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="9a810-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="9a810-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="9a810-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-245">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="9a810-245">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="9a810-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="9a810-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="9a810-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="9a810-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="9a810-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="9a810-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="9a810-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="9a810-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-250">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="9a810-250">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="9a810-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="9a810-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="9a810-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="9a810-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="9a810-253"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="9a810-253"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="9a810-254"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="9a810-254"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="9a810-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="9a810-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="9a810-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="9a810-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="9a810-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="9a810-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="9a810-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="9a810-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="9a810-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="9a810-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="9a810-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="9a810-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="9a810-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="9a810-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="9a810-262">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="9a810-262">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="9a810-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="9a810-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="9a810-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="9a810-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="9a810-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="9a810-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="9a810-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="9a810-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="9a810-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="9a810-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9a810-268">**版本**</span><span class="sxs-lookup"><span data-stu-id="9a810-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a810-269">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9a810-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a810-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9a810-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a810-271">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Version**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="9a810-271">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="9a810-272">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="9a810-272">Version of the operation.</span></span>

<span data-ttu-id="9a810-273">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="9a810-273">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="9a810-274"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="9a810-274"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="9a810-275"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="9a810-275"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="9a810-276">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="9a810-276">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a810-277">備註</span><span class="sxs-lookup"><span data-stu-id="9a810-277">Remarks</span></span>

<span data-ttu-id="9a810-278">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="9a810-278">WMI does not implement this class.</span></span>

<span data-ttu-id="9a810-279">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="9a810-279">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9a810-280">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9a810-280">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a810-281">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a810-281">Requirements</span></span>



| <span data-ttu-id="9a810-282">需求</span><span class="sxs-lookup"><span data-stu-id="9a810-282">Requirement</span></span> | <span data-ttu-id="9a810-283">值</span><span class="sxs-lookup"><span data-stu-id="9a810-283">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a810-284">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a810-284">Minimum supported client</span></span><br/> | <span data-ttu-id="9a810-285">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a810-285">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a810-286">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a810-286">Minimum supported server</span></span><br/> | <span data-ttu-id="9a810-287">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a810-287">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a810-288">命名空間</span><span class="sxs-lookup"><span data-stu-id="9a810-288">Namespace</span></span><br/>                | <span data-ttu-id="9a810-289">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9a810-289">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9a810-290">MOF</span><span class="sxs-lookup"><span data-stu-id="9a810-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a810-291"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a810-291"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a810-292">DLL</span><span class="sxs-lookup"><span data-stu-id="9a810-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a810-293"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a810-293"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a810-294">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a810-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a810-295">**CIM \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="9a810-295">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

