---
description: CIM \_ DirectorySpecification 類別會捕捉 software 元素的主要目錄結構。 此類別是用來將軟體專案的檔案組織成可在電腦系統上重新置放的可管理單位。
ms.assetid: faeab356-e470-477b-97d2-1a19ce1d8d21
ms.tgt_platform: multiple
title: CIM_DirectorySpecification 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecification
- CIM_DirectorySpecification.CheckID
- CIM_DirectorySpecification.Caption
- CIM_DirectorySpecification.Description
- CIM_DirectorySpecification.CheckMode
- CIM_DirectorySpecification.Name
- CIM_DirectorySpecification.TargetOperatingSystem
- CIM_DirectorySpecification.Version
- CIM_DirectorySpecification.SoftwareElementID
- CIM_DirectorySpecification.SoftwareElementState
- CIM_DirectorySpecification.DirectoryPath
- CIM_DirectorySpecification.DirectoryType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a7eb6ae627c8ed9b5639e573e1d2d89132698ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111069"
---
# <a name="cim_directoryspecification-class"></a><span data-ttu-id="10467-104">CIM \_ DirectorySpecification 類別</span><span class="sxs-lookup"><span data-stu-id="10467-104">CIM\_DirectorySpecification class</span></span>

<span data-ttu-id="10467-105">**CIM \_ DirectorySpecification** 類別會捕捉 software 元素的主要目錄結構。</span><span class="sxs-lookup"><span data-stu-id="10467-105">The **CIM\_DirectorySpecification** class captures the major directory structure of a software element.</span></span> <span data-ttu-id="10467-106">此類別是用來將軟體專案的檔案組織成可在電腦系統上重新置放的可管理單位。</span><span class="sxs-lookup"><span data-stu-id="10467-106">This class is used to organize the files of a software element into manageable units that can be relocated on a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10467-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="10467-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="10467-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="10467-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="10467-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="10467-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="10467-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="10467-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="10467-111">語法</span><span class="sxs-lookup"><span data-stu-id="10467-111">Syntax</span></span>

``` syntax
[UUID("{A524EE6E-DB29-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_DirectorySpecification : CIM_Check
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
  string  DirectoryPath;
  uint16  DirectoryType;
};
```

## <a name="members"></a><span data-ttu-id="10467-112">成員</span><span class="sxs-lookup"><span data-stu-id="10467-112">Members</span></span>

<span data-ttu-id="10467-113">**CIM \_ DirectorySpecification** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="10467-113">The **CIM\_DirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="10467-114">方法</span><span class="sxs-lookup"><span data-stu-id="10467-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="10467-115">屬性</span><span class="sxs-lookup"><span data-stu-id="10467-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="10467-116">方法</span><span class="sxs-lookup"><span data-stu-id="10467-116">Methods</span></span>

<span data-ttu-id="10467-117">**CIM \_ DirectorySpecification** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="10467-117">The **CIM\_DirectorySpecification** class has these methods.</span></span>



| <span data-ttu-id="10467-118">方法</span><span class="sxs-lookup"><span data-stu-id="10467-118">Method</span></span>                                                              | <span data-ttu-id="10467-119">描述</span><span class="sxs-lookup"><span data-stu-id="10467-119">Description</span></span>                                                                     |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="10467-120">**調用**</span><span class="sxs-lookup"><span data-stu-id="10467-120">**Invoke**</span></span>](invoke-method-in-class-cim-directoryspecification.md) | <span data-ttu-id="10467-121">評估特定檢查。</span><span class="sxs-lookup"><span data-stu-id="10467-121">Evaluates a particular check.</span></span> <span data-ttu-id="10467-122">這個方法不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="10467-122">This method is not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="10467-123">屬性</span><span class="sxs-lookup"><span data-stu-id="10467-123">Properties</span></span>

<span data-ttu-id="10467-124">**CIM \_ DirectorySpecification** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="10467-124">The **CIM\_DirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10467-125">**標題**</span><span class="sxs-lookup"><span data-stu-id="10467-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10467-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10467-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10467-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10467-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10467-128">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="10467-128">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="10467-129">主體的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="10467-129">A short textual description of the subject.</span></span>

<span data-ttu-id="10467-130">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="10467-130">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="10467-131">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="10467-131">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10467-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10467-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10467-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10467-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10467-134">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="10467-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="10467-135">與其他索引鍵搭配使用來唯一識別檢查的識別碼。</span><span class="sxs-lookup"><span data-stu-id="10467-135">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="10467-136">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="10467-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="10467-137">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="10467-137">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10467-138">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="10467-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10467-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10467-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10467-140">若 **為 TRUE**，則條件應該存在於環境中。</span><span class="sxs-lookup"><span data-stu-id="10467-140">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="10467-141">例如，檔案應該在系統上，因此叫 [**用方法應該**](invoke-method-in-class-cim-check.md) 傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="10467-141">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="10467-142">如果 **為 FALSE**，則條件不應該存在。</span><span class="sxs-lookup"><span data-stu-id="10467-142">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="10467-143">例如，檔案不在系統上，因此 [**Invoke**](invoke-method-in-class-cim-check.md) 方法應該傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="10467-143">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="10467-144">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="10467-144">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="10467-145">**說明**</span><span class="sxs-lookup"><span data-stu-id="10467-145">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10467-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10467-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10467-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10467-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10467-148">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="10467-148">A description of the objects.</span></span>

<span data-ttu-id="10467-149">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="10467-149">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="10467-150">**DirectoryPath**</span><span class="sxs-lookup"><span data-stu-id="10467-150">**DirectoryPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10467-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10467-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10467-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10467-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10467-153">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="10467-153">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="10467-154">目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="10467-154">Directory name.</span></span> <span data-ttu-id="10467-155">應用程式提供者所提供的值是預設或建議的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="10467-155">The value supplied by an application provider is a default or recommended path name.</span></span> <span data-ttu-id="10467-156">您可以針對特定環境變更此值。</span><span class="sxs-lookup"><span data-stu-id="10467-156">The value can be changed for a particular environment.</span></span>

</dd> <dt>

<span data-ttu-id="10467-157">**DirectoryType**</span><span class="sxs-lookup"><span data-stu-id="10467-157">**DirectoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10467-158">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="10467-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10467-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10467-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10467-160">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 位置 \| 001.2」 ) </span><span class="sxs-lookup"><span data-stu-id="10467-160">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Location\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="10467-161">描述的目錄類型。</span><span class="sxs-lookup"><span data-stu-id="10467-161">Type of directory being described.</span></span>

<dt>

<span id="Product_base_directory"></span><span id="product_base_directory"></span><span id="PRODUCT_BASE_DIRECTORY"></span>

<span data-ttu-id="10467-162">**產品基底目錄** (0) </span><span class="sxs-lookup"><span data-stu-id="10467-162">**Product base directory** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_executable_directory"></span><span id="product_executable_directory"></span><span id="PRODUCT_EXECUTABLE_DIRECTORY"></span>

<span data-ttu-id="10467-163">**產品可執行檔目錄** (1) </span><span class="sxs-lookup"><span data-stu-id="10467-163">**Product executable directory** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_library_directory"></span><span id="product_library_directory"></span><span id="PRODUCT_LIBRARY_DIRECTORY"></span>

<span data-ttu-id="10467-164">**產品程式庫目錄** (2) </span><span class="sxs-lookup"><span data-stu-id="10467-164">**Product library directory** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_configuration_directory"></span><span id="product_configuration_directory"></span><span id="PRODUCT_CONFIGURATION_DIRECTORY"></span>

<span data-ttu-id="10467-165">**Product configuration directory** (3) </span><span class="sxs-lookup"><span data-stu-id="10467-165">**Product configuration directory** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_include_directory"></span><span id="product_include_directory"></span><span id="PRODUCT_INCLUDE_DIRECTORY"></span>

<span data-ttu-id="10467-166">**產品包含目錄** (4) </span><span class="sxs-lookup"><span data-stu-id="10467-166">**Product include directory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_working_directory"></span><span id="product_working_directory"></span><span id="PRODUCT_WORKING_DIRECTORY"></span>

<span data-ttu-id="10467-167">**產品工作目錄** (5) </span><span class="sxs-lookup"><span data-stu-id="10467-167">**Product working directory** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_log_directory"></span><span id="product_log_directory"></span><span id="PRODUCT_LOG_DIRECTORY"></span>

<span data-ttu-id="10467-168">**產品記錄目錄** (6) </span><span class="sxs-lookup"><span data-stu-id="10467-168">**Product log directory** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_base_directory"></span><span id="shared_base_directory"></span><span id="SHARED_BASE_DIRECTORY"></span>

<span data-ttu-id="10467-169">**共用的基底目錄** (7) </span><span class="sxs-lookup"><span data-stu-id="10467-169">**Shared base directory** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_executable_directory"></span><span id="shared_executable_directory"></span><span id="SHARED_EXECUTABLE_DIRECTORY"></span>

<span data-ttu-id="10467-170">**共用可執行目錄** (8) </span><span class="sxs-lookup"><span data-stu-id="10467-170">**Shared executable directory** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_library_directory"></span><span id="shared_library_directory"></span><span id="SHARED_LIBRARY_DIRECTORY"></span>

<span data-ttu-id="10467-171">**共用程式庫目錄** (9) </span><span class="sxs-lookup"><span data-stu-id="10467-171">**Shared library directory** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_include_directory"></span><span id="shared_include_directory"></span><span id="SHARED_INCLUDE_DIRECTORY"></span>

<span data-ttu-id="10467-172">**共用的 include 目錄** (10) </span><span class="sxs-lookup"><span data-stu-id="10467-172">**Shared include directory** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="System_base_directory"></span><span id="system_base_directory"></span><span id="SYSTEM_BASE_DIRECTORY"></span>

<span data-ttu-id="10467-173">**系統基底目錄** (11) </span><span class="sxs-lookup"><span data-stu-id="10467-173">**System base directory** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="System_executable_directory"></span><span id="system_executable_directory"></span><span id="SYSTEM_EXECUTABLE_DIRECTORY"></span>

<span data-ttu-id="10467-174">**系統可執行檔目錄** (12) </span><span class="sxs-lookup"><span data-stu-id="10467-174">**System executable directory** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="System_library_directory"></span><span id="system_library_directory"></span><span id="SYSTEM_LIBRARY_DIRECTORY"></span>

<span data-ttu-id="10467-175">**系統程式庫目錄** (13) </span><span class="sxs-lookup"><span data-stu-id="10467-175">**System library directory** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="System_configuration_directory"></span><span id="system_configuration_directory"></span><span id="SYSTEM_CONFIGURATION_DIRECTORY"></span>

<span data-ttu-id="10467-176">**系統組態目錄** (14) </span><span class="sxs-lookup"><span data-stu-id="10467-176">**System configuration directory** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="System_include_directory"></span><span id="system_include_directory"></span><span id="SYSTEM_INCLUDE_DIRECTORY"></span>

<span data-ttu-id="10467-177">**System include directory** (15) </span><span class="sxs-lookup"><span data-stu-id="10467-177">**System include directory** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="System_log_directory"></span><span id="system_log_directory"></span><span id="SYSTEM_LOG_DIRECTORY"></span>

<span data-ttu-id="10467-178">**系統記錄檔目錄** (16) </span><span class="sxs-lookup"><span data-stu-id="10467-178">**System log directory** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10467-179">**其他** (17) </span><span class="sxs-lookup"><span data-stu-id="10467-179">**Other** (17)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10467-180">**名稱**</span><span class="sxs-lookup"><span data-stu-id="10467-180">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10467-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10467-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10467-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10467-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10467-183">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Name**") 、 [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="10467-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="10467-184">用來識別軟體元素的名稱</span><span class="sxs-lookup"><span data-stu-id="10467-184">Name used to identify the software element</span></span>

<span data-ttu-id="10467-185">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="10467-185">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="10467-186">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="10467-186">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10467-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10467-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10467-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10467-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10467-189">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementID**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="10467-189">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="10467-190">這是此軟體元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="10467-190">This is an identifier for this software element.</span></span>

<span data-ttu-id="10467-191">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="10467-191">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="10467-192">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="10467-192">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10467-193">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="10467-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10467-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10467-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10467-195">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="10467-195">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="10467-196">軟體元素的軟體專案狀態。</span><span class="sxs-lookup"><span data-stu-id="10467-196">The software element state of a software element.</span></span>

<span data-ttu-id="10467-197">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="10467-197">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="10467-198"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="10467-198"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="10467-199">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="10467-199">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="10467-200"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="10467-200"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="10467-201">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="10467-201">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="10467-202"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="10467-202"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="10467-203">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="10467-203">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="10467-204"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="10467-204"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="10467-205">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="10467-205">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10467-206">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="10467-206">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10467-207">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="10467-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10467-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10467-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10467-209">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| Software Component Information \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="10467-209">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="10467-210">Software 元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="10467-210">Target operating system of the software element.</span></span>

<span data-ttu-id="10467-211">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="10467-211">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10467-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="10467-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10467-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="10467-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="10467-214"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="10467-214"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="10467-215">Mac OS</span><span class="sxs-lookup"><span data-stu-id="10467-215">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="10467-216"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="10467-216"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="10467-217">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="10467-217">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="10467-218"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="10467-218"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="10467-219"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="10467-219"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="10467-220"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="10467-220"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="10467-221"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="10467-221"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="10467-222">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="10467-222">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="10467-223"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="10467-223"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="10467-224">HP-UX</span><span class="sxs-lookup"><span data-stu-id="10467-224">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="10467-225"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="10467-225"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="10467-226"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="10467-226"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="10467-227"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="10467-227"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="10467-228"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="10467-228"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="10467-229"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="10467-229"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="10467-230">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="10467-230">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="10467-231"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="10467-231"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="10467-232"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="10467-232"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="10467-233">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="10467-233">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="10467-234"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="10467-234"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="10467-235">Windows 95</span><span class="sxs-lookup"><span data-stu-id="10467-235">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="10467-236"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="10467-236"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="10467-237">Windows 98</span><span class="sxs-lookup"><span data-stu-id="10467-237">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="10467-238"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="10467-238"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="10467-239">Windows NT</span><span class="sxs-lookup"><span data-stu-id="10467-239">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="10467-240"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="10467-240"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="10467-241">Windows CE</span><span class="sxs-lookup"><span data-stu-id="10467-241">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="10467-242"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="10467-242"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="10467-243">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="10467-243">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="10467-244"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="10467-244"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="10467-245"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="10467-245"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="10467-246"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="10467-246"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="10467-247"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="10467-247"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="10467-248"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="10467-248"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="10467-249"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="10467-249"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="10467-250"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="10467-250"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="10467-251"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="10467-251"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="10467-252"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="10467-252"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="10467-253"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="10467-253"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="10467-254"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="10467-254"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="10467-255"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="10467-255"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="10467-256">系列</span><span class="sxs-lookup"><span data-stu-id="10467-256">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="10467-257"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="10467-257"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="10467-258">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="10467-258">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="10467-259"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="10467-259"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="10467-260">將 NT</span><span class="sxs-lookup"><span data-stu-id="10467-260">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="10467-261"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="10467-261"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="10467-262">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="10467-262">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="10467-263"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="10467-263"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="10467-264"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="10467-264"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="10467-265"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="10467-265"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="10467-266"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="10467-266"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="10467-267"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="10467-267"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="10467-268"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="10467-268"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="10467-269">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="10467-269">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="10467-270"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="10467-270"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="10467-271"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="10467-271"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="10467-272"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="10467-272"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="10467-273"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="10467-273"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="10467-274">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="10467-274">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="10467-275"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="10467-275"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="10467-276"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="10467-276"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="10467-277"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="10467-277"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="10467-278"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="10467-278"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="10467-279"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="10467-279"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="10467-280"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="10467-280"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="10467-281"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="10467-281"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="10467-282"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="10467-282"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="10467-283"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="10467-283"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="10467-284"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="10467-284"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="10467-285"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="10467-285"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="10467-286">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="10467-286">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="10467-287"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="10467-287"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="10467-288"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="10467-288"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="10467-289"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="10467-289"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="10467-290"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="10467-290"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="10467-291"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="10467-291"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10467-292">**版本**</span><span class="sxs-lookup"><span data-stu-id="10467-292">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10467-293">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10467-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10467-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10467-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10467-295">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Version**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="10467-295">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="10467-296">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="10467-296">Version of the operation.</span></span>

<span data-ttu-id="10467-297">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="10467-297">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="10467-298"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="10467-298"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="10467-299"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="10467-299"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="10467-300">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="10467-300">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10467-301">備註</span><span class="sxs-lookup"><span data-stu-id="10467-301">Remarks</span></span>

<span data-ttu-id="10467-302">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="10467-302">WMI does not implement this class.</span></span> <span data-ttu-id="10467-303">針對衍生自 **CIM \_ DirectorySpecification** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="10467-303">For classes derived from **CIM\_DirectorySpecification**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="10467-304">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="10467-304">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="10467-305">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="10467-305">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="10467-306">規格需求</span><span class="sxs-lookup"><span data-stu-id="10467-306">Requirements</span></span>



| <span data-ttu-id="10467-307">需求</span><span class="sxs-lookup"><span data-stu-id="10467-307">Requirement</span></span> | <span data-ttu-id="10467-308">值</span><span class="sxs-lookup"><span data-stu-id="10467-308">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10467-309">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10467-309">Minimum supported client</span></span><br/> | <span data-ttu-id="10467-310">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10467-310">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10467-311">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10467-311">Minimum supported server</span></span><br/> | <span data-ttu-id="10467-312">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10467-312">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10467-313">命名空間</span><span class="sxs-lookup"><span data-stu-id="10467-313">Namespace</span></span><br/>                | <span data-ttu-id="10467-314">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="10467-314">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="10467-315">MOF</span><span class="sxs-lookup"><span data-stu-id="10467-315">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10467-316"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="10467-316"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="10467-317">DLL</span><span class="sxs-lookup"><span data-stu-id="10467-317">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10467-318"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10467-318"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10467-319">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10467-319">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10467-320">**CIM \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="10467-320">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

