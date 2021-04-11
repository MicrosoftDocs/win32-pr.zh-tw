---
description: Win32 \_ PRINTERDRIVER WMI 類別代表 win32 印表機實例的驅動程式 \_ 。
ms.assetid: baf48bbf-60a3-4d9b-93b7-c1b22518a9c1
ms.tgt_platform: multiple
title: Win32_PrinterDriver 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver
- Win32_PrinterDriver.Caption
- Win32_PrinterDriver.ConfigFile
- Win32_PrinterDriver.CreationClassName
- Win32_PrinterDriver.DataFile
- Win32_PrinterDriver.DefaultDataType
- Win32_PrinterDriver.DependentFiles
- Win32_PrinterDriver.Description
- Win32_PrinterDriver.DriverPath
- Win32_PrinterDriver.FilePath
- Win32_PrinterDriver.HelpFile
- Win32_PrinterDriver.InfName
- Win32_PrinterDriver.InstallDate
- Win32_PrinterDriver.MonitorName
- Win32_PrinterDriver.Name
- Win32_PrinterDriver.OEMUrl
- Win32_PrinterDriver.Started
- Win32_PrinterDriver.StartMode
- Win32_PrinterDriver.Status
- Win32_PrinterDriver.SupportedPlatform
- Win32_PrinterDriver.SystemCreationClassName
- Win32_PrinterDriver.SystemName
- Win32_PrinterDriver.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 615d6561e12f67edee34e0de84dade12f250e0f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847318"
---
# <a name="win32_printerdriver-class"></a><span data-ttu-id="cde51-103">Win32 \_ PrinterDriver 類別</span><span class="sxs-lookup"><span data-stu-id="cde51-103">Win32\_PrinterDriver class</span></span>

<span data-ttu-id="cde51-104">**Win32 \_ PrinterDriver** [WMI 類別](../wmisdk/retrieving-a-class.md)代表 [**win32 \_ 印表機**](win32-printer.md)實例的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="cde51-104">The **Win32\_PrinterDriver** [WMI class](../wmisdk/retrieving-a-class.md) represents the drivers for a [**Win32\_Printer**](win32-printer.md) instance.</span></span>

<span data-ttu-id="cde51-105">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含所有繼承的屬性，但不包括方法。</span><span class="sxs-lookup"><span data-stu-id="cde51-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties, but excludes methods.</span></span> <span data-ttu-id="cde51-106">如需方法的參考資訊，請參閱本主題中的方法表格。</span><span class="sxs-lookup"><span data-stu-id="cde51-106">For reference information about methods, see the table of methods in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="cde51-107">語法</span><span class="sxs-lookup"><span data-stu-id="cde51-107">Syntax</span></span>

``` syntax
class Win32_PrinterDriver : CIM_Service
{
  string   Caption;
  string   ConfigFile;
  string   CreationClassName;
  string   DataFile;
  string   DefaultDataType;
  string   DependentFiles[];
  string   Description;
  string   DriverPath;
  string   FilePath;
  string   HelpFile;
  string   InfName;
  datetime InstallDate;
  string   MonitorName;
  string   Name;
  string   OEMUrl;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SupportedPlatform;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Version;
};
```

## <a name="members"></a><span data-ttu-id="cde51-108">成員</span><span class="sxs-lookup"><span data-stu-id="cde51-108">Members</span></span>

<span data-ttu-id="cde51-109">**Win32 \_ PrinterDriver** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cde51-109">The **Win32\_PrinterDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="cde51-110">方法</span><span class="sxs-lookup"><span data-stu-id="cde51-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="cde51-111">屬性</span><span class="sxs-lookup"><span data-stu-id="cde51-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cde51-112">方法</span><span class="sxs-lookup"><span data-stu-id="cde51-112">Methods</span></span>

<span data-ttu-id="cde51-113">**Win32 \_ PrinterDriver** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="cde51-113">The **Win32\_PrinterDriver** class has these methods.</span></span>



| <span data-ttu-id="cde51-114">方法</span><span class="sxs-lookup"><span data-stu-id="cde51-114">Method</span></span>                                                                           | <span data-ttu-id="cde51-115">描述</span><span class="sxs-lookup"><span data-stu-id="cde51-115">Description</span></span>                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="cde51-116">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="cde51-116">**AddPrinterDriver**</span></span>](addprinterdriver-method-in-class-win32-printerdriver.md) | <span data-ttu-id="cde51-117">建立新的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="cde51-117">Creates a new printer driver.</span></span><br/> |
| [<span data-ttu-id="cde51-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="cde51-118">**StartService**</span></span>](startservice-method-in-class-win32-printerdriver.md)         | <span data-ttu-id="cde51-119">啟動列印服務。</span><span class="sxs-lookup"><span data-stu-id="cde51-119">Starts print service.</span></span><br/>         |
| [<span data-ttu-id="cde51-120">**StopService**</span><span class="sxs-lookup"><span data-stu-id="cde51-120">**StopService**</span></span>](stopservice-method-in-class-win32-printerdriver.md)           | <span data-ttu-id="cde51-121">停止列印服務。</span><span class="sxs-lookup"><span data-stu-id="cde51-121">Stops print service.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="cde51-122">屬性</span><span class="sxs-lookup"><span data-stu-id="cde51-122">Properties</span></span>

<span data-ttu-id="cde51-123">**Win32 \_ PrinterDriver** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cde51-123">The **Win32\_PrinterDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cde51-124">**標題**</span><span class="sxs-lookup"><span data-stu-id="cde51-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde51-127">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="cde51-127">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cde51-128">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="cde51-128">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="cde51-129">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="cde51-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cde51-130">**Read-configfile**</span><span class="sxs-lookup"><span data-stu-id="cde51-130">**ConfigFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cde51-133">此印表機驅動程式的設定檔。</span><span class="sxs-lookup"><span data-stu-id="cde51-133">Configuration file for this printer driver.</span></span>

<span data-ttu-id="cde51-134">範例： "pscrptui.dll"</span><span class="sxs-lookup"><span data-stu-id="cde51-134">Example: "pscrptui.dll"</span></span>

</dd> <dt>

<span data-ttu-id="cde51-135">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cde51-135">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde51-138">限定詞： [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="cde51-138">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="cde51-139">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="cde51-139">Name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="cde51-140">搭配這個類別的其他重要屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="cde51-140">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cde51-141">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="cde51-141">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="cde51-142">**檔**</span><span class="sxs-lookup"><span data-stu-id="cde51-142">**DataFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde51-145">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM \_ 資料檔案檔案名) </span><span class="sxs-lookup"><span data-stu-id="cde51-145">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM\_DataFile.FileName)</span></span>
</dt> </dl>

<span data-ttu-id="cde51-146">此印表機驅動程式的資料檔案。</span><span class="sxs-lookup"><span data-stu-id="cde51-146">Data file for this printer driver.</span></span>

<span data-ttu-id="cde51-147">範例： "qms810"</span><span class="sxs-lookup"><span data-stu-id="cde51-147">Example: "qms810.ppd"</span></span>

</dd> <dt>

<span data-ttu-id="cde51-148">**DefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="cde51-148">**DefaultDataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cde51-151">此印表機驅動程式的預設資料類型。</span><span class="sxs-lookup"><span data-stu-id="cde51-151">Default data type for this printer driver.</span></span>

<span data-ttu-id="cde51-152">範例： "EMF"</span><span class="sxs-lookup"><span data-stu-id="cde51-152">Example: "EMF"</span></span>

</dd> <dt>

<span data-ttu-id="cde51-153">**DependentFiles**</span><span class="sxs-lookup"><span data-stu-id="cde51-153">**DependentFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-154">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="cde51-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cde51-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cde51-156">此印表機驅動程式的相依檔案陣列。</span><span class="sxs-lookup"><span data-stu-id="cde51-156">Array of dependent files for this printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="cde51-157">**說明**</span><span class="sxs-lookup"><span data-stu-id="cde51-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde51-160">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="cde51-160">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cde51-161">描述連結的批註。</span><span class="sxs-lookup"><span data-stu-id="cde51-161">Comment that describes the link.</span></span>

<span data-ttu-id="cde51-162">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="cde51-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cde51-163">**DriverPath**</span><span class="sxs-lookup"><span data-stu-id="cde51-163">**DriverPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde51-166">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM \_ 資料檔案。路徑) </span><span class="sxs-lookup"><span data-stu-id="cde51-166">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM\_DataFile.Path)</span></span>
</dt> </dl>

<span data-ttu-id="cde51-167">此印表機驅動程式的路徑。</span><span class="sxs-lookup"><span data-stu-id="cde51-167">Path for this printer driver.</span></span>

<span data-ttu-id="cde51-168">範例： "C： \\ \\ 驅動程式 \\ \\pscript.dll"</span><span class="sxs-lookup"><span data-stu-id="cde51-168">Example: "C:\\\\drivers\\\\pscript.dll"</span></span>

</dd> <dt>

<span data-ttu-id="cde51-169">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="cde51-169">**FilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-171">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cde51-171">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cde51-172">所要使用之 INF 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="cde51-172">Path to the INF file being used.</span></span>

<span data-ttu-id="cde51-173">範例： "c： \\ \\ temp \\ \\ driver"</span><span class="sxs-lookup"><span data-stu-id="cde51-173">Example: "c:\\\\temp\\\\driver"</span></span>

</dd> <dt>

<span data-ttu-id="cde51-174">**HelpFile**</span><span class="sxs-lookup"><span data-stu-id="cde51-174">**HelpFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cde51-177">此印表機驅動程式的說明檔。</span><span class="sxs-lookup"><span data-stu-id="cde51-177">Help file for this printer driver.</span></span>

<span data-ttu-id="cde51-178">範例： "pscrptui .hlp"</span><span class="sxs-lookup"><span data-stu-id="cde51-178">Example: "pscrptui.hlp"</span></span>

</dd> <dt>

<span data-ttu-id="cde51-179">**InfName**</span><span class="sxs-lookup"><span data-stu-id="cde51-179">**InfName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cde51-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cde51-182">所使用的 INF 檔案名。</span><span class="sxs-lookup"><span data-stu-id="cde51-182">Name of the INF file being used.</span></span> <span data-ttu-id="cde51-183">預設值是使用作業系統提供的印表機 INF 檔案。</span><span class="sxs-lookup"><span data-stu-id="cde51-183">The default is to use an operating system provided printer INF file.</span></span> <span data-ttu-id="cde51-184">如果印表機的製造商直接提供驅動程式，而不是作業系統，則會使用不同的檔案名。</span><span class="sxs-lookup"><span data-stu-id="cde51-184">A different file name is used if the driver is provided directly by the manufacturer of the printer and not the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="cde51-185">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cde51-185">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-186">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="cde51-186">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde51-188">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="cde51-188">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cde51-189">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="cde51-189">Date and time the object is installed.</span></span> <span data-ttu-id="cde51-190">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="cde51-190">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="cde51-191">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="cde51-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cde51-192">**MonitorName**</span><span class="sxs-lookup"><span data-stu-id="cde51-192">**MonitorName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-193">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cde51-195">此印表機驅動程式的監視名稱。</span><span class="sxs-lookup"><span data-stu-id="cde51-195">Name of the monitor for this printer driver.</span></span>

<span data-ttu-id="cde51-196">範例： "PJL monitor"</span><span class="sxs-lookup"><span data-stu-id="cde51-196">Example: "PJL monitor"</span></span>

</dd> <dt>

<span data-ttu-id="cde51-197">**名稱**</span><span class="sxs-lookup"><span data-stu-id="cde51-197">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde51-200">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="cde51-200">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="cde51-201">此印表機的驅動程式名稱。</span><span class="sxs-lookup"><span data-stu-id="cde51-201">Driver name for this printer.</span></span> <span data-ttu-id="cde51-202">這是由 **名稱**、 **版本** 和 **SupportedPlatform** 值所組成的複合索引鍵。</span><span class="sxs-lookup"><span data-stu-id="cde51-202">This is a compound key composed of the **Name**, **Version**, and **SupportedPlatform** values.</span></span>

<span data-ttu-id="cde51-203">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) ，並且會覆寫該類別中的 **名稱** 定義。</span><span class="sxs-lookup"><span data-stu-id="cde51-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) and overrides the **Name** definition in that class.</span></span>

</dd> <dt>

<span data-ttu-id="cde51-204">**OEMUrl**</span><span class="sxs-lookup"><span data-stu-id="cde51-204">**OEMUrl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-205">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cde51-207">World Wide Web (WWW) 連結至印表機製造商的網站。</span><span class="sxs-lookup"><span data-stu-id="cde51-207">World Wide Web (WWW) link to the printer manufacturer's website.</span></span> <span data-ttu-id="cde51-208">請注意，使用 Win32 .inf 檔案時，不會填入這個屬性，而且僅適用于直接從製造商提供的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="cde51-208">Note that this property is not populated when the Win32.inf file is used, and is only applicable for drivers provided directly from the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="cde51-209">**已開始**</span><span class="sxs-lookup"><span data-stu-id="cde51-209">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-210">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cde51-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde51-212">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「已啟動」 ) </span><span class="sxs-lookup"><span data-stu-id="cde51-212">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="cde51-213">若 **為 TRUE**，則會啟動服務。</span><span class="sxs-lookup"><span data-stu-id="cde51-213">If **TRUE**, the service is started.</span></span> <span data-ttu-id="cde51-214">如果 **為 FALSE**，則表示服務已停止。</span><span class="sxs-lookup"><span data-stu-id="cde51-214">If **FALSE**, the service is stopped.</span></span>

<span data-ttu-id="cde51-215">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="cde51-215">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="cde51-216">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="cde51-216">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde51-219">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「啟動模式」 ) </span><span class="sxs-lookup"><span data-stu-id="cde51-219">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="cde51-220">服務的啟動模式會由作業系統自動啟動，或只在要求時啟動。</span><span class="sxs-lookup"><span data-stu-id="cde51-220">Start mode of the service is automatically started by an operating system, or only started when requested.</span></span>

<span data-ttu-id="cde51-221">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="cde51-221">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="cde51-222">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="cde51-222">The following are possible values:</span></span>

<dl> <dd><span data-ttu-id="cde51-223">自動</span><span class="sxs-lookup"><span data-stu-id="cde51-223">"Automatic"</span></span></dd> <dd><span data-ttu-id="cde51-224">》</span><span class="sxs-lookup"><span data-stu-id="cde51-224">"Manual"</span></span></dd> </dl>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="cde51-225">**自動** ( 「自動」 ) </span><span class="sxs-lookup"><span data-stu-id="cde51-225">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="cde51-226">**手動** ( 「手動」 ) </span><span class="sxs-lookup"><span data-stu-id="cde51-226">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cde51-227">**狀態**</span><span class="sxs-lookup"><span data-stu-id="cde51-227">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-228">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde51-230">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="cde51-230">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cde51-231">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="cde51-231">Current status of the object.</span></span> <span data-ttu-id="cde51-232">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="cde51-232">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="cde51-233">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="cde51-233">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="cde51-234">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="cde51-234">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cde51-235">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="cde51-235">The latter, "Service", can apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cde51-236">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="cde51-236">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cde51-237">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="cde51-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cde51-238">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="cde51-238">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cde51-239">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="cde51-239">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cde51-240">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="cde51-240">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cde51-241">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="cde51-241">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cde51-242">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="cde51-242">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cde51-243">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="cde51-243">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cde51-244">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="cde51-244">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cde51-245">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="cde51-245">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cde51-246">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="cde51-246">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cde51-247">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="cde51-247">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cde51-248">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="cde51-248">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cde51-249">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="cde51-249">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cde51-250">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="cde51-250">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cde51-251">**SupportedPlatform**</span><span class="sxs-lookup"><span data-stu-id="cde51-251">**SupportedPlatform**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-253">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cde51-253">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cde51-254">驅動程式適用的作業環境。</span><span class="sxs-lookup"><span data-stu-id="cde51-254">Operating environments that the driver is intended for.</span></span>

<span data-ttu-id="cde51-255">範例：「Windows NT x86」。</span><span class="sxs-lookup"><span data-stu-id="cde51-255">Example: "Windows NT x86".</span></span>

</dd> <dt>

<span data-ttu-id="cde51-256">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cde51-256">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde51-259">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Class Name ") </span><span class="sxs-lookup"><span data-stu-id="cde51-259">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="cde51-260">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="cde51-260">Scoping system's creation class name.</span></span>

<span data-ttu-id="cde51-261">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="cde51-261">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="cde51-262">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cde51-262">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-263">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cde51-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cde51-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde51-265">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**Name**") 、 [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Name ") </span><span class="sxs-lookup"><span data-stu-id="cde51-265">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="cde51-266">裝載此服務的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="cde51-266">Name of the system that hosts this service.</span></span>

<span data-ttu-id="cde51-267">這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="cde51-267">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="cde51-268">**版本**</span><span class="sxs-lookup"><span data-stu-id="cde51-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde51-269">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="cde51-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cde51-270">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cde51-270">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cde51-271">印表機驅動程式的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="cde51-271">Operating system version for the printer driver.</span></span>

<dt>

<span id="3"></span>

<span data-ttu-id="cde51-272"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="cde51-272"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="cde51-273">Win2k</span><span class="sxs-lookup"><span data-stu-id="cde51-273">Win2k</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cde51-274">備註</span><span class="sxs-lookup"><span data-stu-id="cde51-274">Remarks</span></span>

<span data-ttu-id="cde51-275">**Win32 \_ PrinterDriver** 類別衍生自 [**cim \_ 服務**](cim-service.md)，其衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="cde51-275">The **Win32\_PrinterDriver** class is derived from [**CIM\_Service**](cim-service.md) which derives from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="cde51-276">使用者可以藉由刪除此類別的對應實例來卸載印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="cde51-276">Users can uninstall a printer driver by deleting a corresponding instance of this class.</span></span> <span data-ttu-id="cde51-277">若要這樣做，呼叫進程必須設定 **SeLoadDriverPrivilege** 許可權，才能刪除這個類別的實例。</span><span class="sxs-lookup"><span data-stu-id="cde51-277">To do so, the calling process must have the **SeLoadDriverPrivilege** privilege set to delete an instance of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="cde51-278">範例</span><span class="sxs-lookup"><span data-stu-id="cde51-278">Examples</span></span>

<span data-ttu-id="cde51-279">[管理印表機和印表機驅動程式](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548)VBScript 範例會管理印表機驅動程式和印表機埠。</span><span class="sxs-lookup"><span data-stu-id="cde51-279">The [Manage Printer and Printer Drivers](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) VBScript sample manages printer drivers and printer ports.</span></span>

<span data-ttu-id="cde51-280">下列 [TechNet 論壇的討論](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) 內容說明如何建立印表機，並從伺服器上傳驅動程式。</span><span class="sxs-lookup"><span data-stu-id="cde51-280">The following [discussion on the TechNet forums](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) describes how to create a printer and upload drivers from a server.</span></span>

<span data-ttu-id="cde51-281">下列 VBScript 範例會列出所有已安裝在電腦上的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="cde51-281">The following VBScript sample lists all the printer drivers that have been installed on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrinterDriver") 
 
For each objPrinter in colInstalledPrinters 
    Wscript.Echo "Configuration File: " & objPrinter.ConfigFile 
    Wscript.Echo "Data File: " & objPrinter.DataFile 
    Wscript.Echo "Description: " & objPrinter.Description 
    Wscript.Echo "Driver Path: " & objPrinter.DriverPath 
    Wscript.Echo "File Path: " & objPrinter.FilePath 
    Wscript.Echo "Help File: " & objPrinter.HelpFile 
    Wscript.Echo "INF Name: " & objPrinter.InfName 
    Wscript.Echo "Monitor Name: " & objPrinter.MonitorName 
    Wscript.Echo "Name: " & objPrinter.Name 
    Wscript.Echo "OEM Url: " & objPrinter.OEMUrl 
    Wscript.Echo "Supported Platform: " & objPrinter.SupportedPlatform 
    Wscript.Echo "Version: " & objPrinter.Version 
Next 
```



## <a name="requirements"></a><span data-ttu-id="cde51-282">規格需求</span><span class="sxs-lookup"><span data-stu-id="cde51-282">Requirements</span></span>



| <span data-ttu-id="cde51-283">需求</span><span class="sxs-lookup"><span data-stu-id="cde51-283">Requirement</span></span> | <span data-ttu-id="cde51-284">值</span><span class="sxs-lookup"><span data-stu-id="cde51-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cde51-285">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cde51-285">Minimum supported client</span></span><br/> | <span data-ttu-id="cde51-286">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cde51-286">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="cde51-287">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cde51-287">Minimum supported server</span></span><br/> | <span data-ttu-id="cde51-288">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cde51-288">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="cde51-289">命名空間</span><span class="sxs-lookup"><span data-stu-id="cde51-289">Namespace</span></span><br/>                | <span data-ttu-id="cde51-290">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cde51-290">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="cde51-291">MOF</span><span class="sxs-lookup"><span data-stu-id="cde51-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cde51-292"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="cde51-292"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="cde51-293">DLL</span><span class="sxs-lookup"><span data-stu-id="cde51-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cde51-294"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cde51-294"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="cde51-295">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cde51-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde51-296">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="cde51-296">**CIM\_Service**</span></span>](./cim-service.md)
</dt> <dt>

[<span data-ttu-id="cde51-297">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="cde51-297">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
