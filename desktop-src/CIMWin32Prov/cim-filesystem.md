---
description: CIM \_ FileSystem 類別代表電腦系統本機的檔案或資料集，或從檔案伺服器遠端掛接的檔案或資料集。
ms.assetid: 5a54ab35-b9b6-49e6-96a8-cb2820b054eb
ms.tgt_platform: multiple
title: CIM_FileSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSystem
- CIM_FileSystem.Caption
- CIM_FileSystem.Description
- CIM_FileSystem.InstallDate
- CIM_FileSystem.Name
- CIM_FileSystem.Status
- CIM_FileSystem.AvailableSpace
- CIM_FileSystem.BlockSize
- CIM_FileSystem.CasePreserved
- CIM_FileSystem.CaseSensitive
- CIM_FileSystem.CodeSet
- CIM_FileSystem.CompressionMethod
- CIM_FileSystem.CreationClassName
- CIM_FileSystem.CSCreationClassName
- CIM_FileSystem.CSName
- CIM_FileSystem.EncryptionMethod
- CIM_FileSystem.FileSystemSize
- CIM_FileSystem.MaxFileNameLength
- CIM_FileSystem.ReadOnly
- CIM_FileSystem.Root
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2795e76c686e8f2bb4079aee376dae397b36f510
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847359"
---
# <a name="cim_filesystem-class"></a><span data-ttu-id="24e3a-103">CIM \_ FileSystem 類別</span><span class="sxs-lookup"><span data-stu-id="24e3a-103">CIM\_FileSystem class</span></span>

<span data-ttu-id="24e3a-104">**CIM \_ FileSystem** 類別代表電腦系統本機的檔案或資料集，或從檔案伺服器遠端掛接的檔案或資料集。</span><span class="sxs-lookup"><span data-stu-id="24e3a-104">The **CIM\_FileSystem** class represents a file or data set local to a computer system or remotely mounted from a file server.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="24e3a-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="24e3a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="24e3a-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="24e3a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="24e3a-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="24e3a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="24e3a-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="24e3a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="24e3a-109">語法</span><span class="sxs-lookup"><span data-stu-id="24e3a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4DA18760-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_FileSystem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint64   AvailableSpace;
  uint64   BlockSize;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  uint32   MaxFileNameLength;
  boolean  ReadOnly;
  string   Root;
};
```

## <a name="members"></a><span data-ttu-id="24e3a-110">成員</span><span class="sxs-lookup"><span data-stu-id="24e3a-110">Members</span></span>

<span data-ttu-id="24e3a-111">**CIM \_ FileSystem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="24e3a-111">The **CIM\_FileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="24e3a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="24e3a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="24e3a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="24e3a-113">Properties</span></span>

<span data-ttu-id="24e3a-114">**CIM \_ FileSystem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="24e3a-114">The **CIM\_FileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24e3a-115">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="24e3a-115">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-116">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="24e3a-116">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-118">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 分割區 \| 002.4 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="24e3a-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-119">檔案系統的可用空間量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="24e3a-119">Amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="24e3a-120">如果不明，請輸入0。</span><span class="sxs-lookup"><span data-stu-id="24e3a-120">If unknown, enter 0.</span></span>

<span data-ttu-id="24e3a-121">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="24e3a-121">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-122">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="24e3a-122">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-123">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="24e3a-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-125">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-126">區塊儲存和抓取檔案系統的大小。</span><span class="sxs-lookup"><span data-stu-id="24e3a-126">Block size of the file system for data storage and retrieval.</span></span>

<span data-ttu-id="24e3a-127">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="24e3a-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-128">**標題**</span><span class="sxs-lookup"><span data-stu-id="24e3a-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24e3a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-131">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-132">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="24e3a-132">A short textual description of the object.</span></span>

<span data-ttu-id="24e3a-133">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24e3a-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-134">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="24e3a-134">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-135">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="24e3a-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-137">若 **為 TRUE**，則會保留檔案名的大小寫。</span><span class="sxs-lookup"><span data-stu-id="24e3a-137">If **TRUE**, the case of file names are preserved.</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-138">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="24e3a-138">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-139">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="24e3a-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-141">若 **為 TRUE**，則支援區分大小寫的檔案名。</span><span class="sxs-lookup"><span data-stu-id="24e3a-141">If **TRUE**, case-sensitive file names are supported.</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-142">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="24e3a-142">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-143">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="24e3a-143">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-145">定義檔案系統所支援之字元集或編碼方式的陣列。</span><span class="sxs-lookup"><span data-stu-id="24e3a-145">Array that defines the character sets or encoding supported by the file system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24e3a-146">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="24e3a-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="24e3a-147">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="24e3a-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="24e3a-148">**ASCII** (2) </span><span class="sxs-lookup"><span data-stu-id="24e3a-148">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="24e3a-149">**Unicode** (3) </span><span class="sxs-lookup"><span data-stu-id="24e3a-149">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="24e3a-150">**ISO2022** (4) </span><span class="sxs-lookup"><span data-stu-id="24e3a-150">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="24e3a-151">**ISO8859** (5) </span><span class="sxs-lookup"><span data-stu-id="24e3a-151">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="24e3a-152">**擴充的 UNIX 程式碼** (6) </span><span class="sxs-lookup"><span data-stu-id="24e3a-152">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="24e3a-153">**Utf-8** (7) </span><span class="sxs-lookup"><span data-stu-id="24e3a-153">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="24e3a-154">**UCS-2** (8) </span><span class="sxs-lookup"><span data-stu-id="24e3a-154">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24e3a-155">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="24e3a-155">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24e3a-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-158">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 分割區 \| 002.7」 ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-159">自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="24e3a-159">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="24e3a-160">如果壓縮配置未知或未描述，請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="24e3a-160">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="24e3a-161">如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="24e3a-161">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="24e3a-162">如果邏輯檔案未壓縮，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="24e3a-162">If the logical file is not compressed, use "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-163">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="24e3a-163">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24e3a-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-166">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="24e3a-166">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-167">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="24e3a-167">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="24e3a-168">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="24e3a-168">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-169">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="24e3a-169">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24e3a-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-172">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未產生」。**CreationClassName**") </span><span class="sxs-lookup"><span data-stu-id="24e3a-172">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-173">設定電腦系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="24e3a-173">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-174">**CSName**</span><span class="sxs-lookup"><span data-stu-id="24e3a-174">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24e3a-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-177">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未產生」。**名稱**") </span><span class="sxs-lookup"><span data-stu-id="24e3a-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-178">設定電腦系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="24e3a-178">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-179">**說明**</span><span class="sxs-lookup"><span data-stu-id="24e3a-179">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24e3a-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-182">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-182">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-183">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="24e3a-183">A textual description of the object.</span></span>

<span data-ttu-id="24e3a-184">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24e3a-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-185">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="24e3a-185">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24e3a-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-188">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 分割區 \| 002.8」 ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-189">識別用來加密邏輯檔案之演算法或工具的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="24e3a-189">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="24e3a-190">如果未 indulged 加密配置 (基於安全性理由（例如) ），請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="24e3a-190">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="24e3a-191">如果檔案已加密，但其加密配置不明或未洩漏，請使用「加密」。</span><span class="sxs-lookup"><span data-stu-id="24e3a-191">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="24e3a-192">如果邏輯檔案未加密，請使用「未加密」。</span><span class="sxs-lookup"><span data-stu-id="24e3a-192">If the logical file is not encrypted, use "Not Encrypted".</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-193">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="24e3a-193">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-194">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="24e3a-194">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-196">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-196">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-197">檔案系統的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="24e3a-197">Size of the file system, in bytes.</span></span> <span data-ttu-id="24e3a-198">如果不明，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="24e3a-198">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="24e3a-199">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="24e3a-199">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-200">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="24e3a-200">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-201">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="24e3a-201">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-203">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="24e3a-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-204">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="24e3a-204">Indicates when the object was installed.</span></span> <span data-ttu-id="24e3a-205">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="24e3a-205">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="24e3a-206">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24e3a-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-207">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="24e3a-207">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-208">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="24e3a-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-210">檔案系統內檔案名的最大長度。</span><span class="sxs-lookup"><span data-stu-id="24e3a-210">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="24e3a-211">值為 0 (零) 表示檔案名的長度沒有限制。</span><span class="sxs-lookup"><span data-stu-id="24e3a-211">A value of 0 (zero) indicates that there is no limit to the file name length.</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-212">**名稱**</span><span class="sxs-lookup"><span data-stu-id="24e3a-212">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24e3a-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-215">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-215">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-216">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="24e3a-216">Label by which the object is known.</span></span> <span data-ttu-id="24e3a-217">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="24e3a-217">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="24e3a-218">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24e3a-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-219">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="24e3a-219">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-220">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="24e3a-220">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-222">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrFSAccess ") </span><span class="sxs-lookup"><span data-stu-id="24e3a-222">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-223">若 **為 TRUE**，則會將檔案系統指定為唯讀。</span><span class="sxs-lookup"><span data-stu-id="24e3a-223">If **TRUE**, the file system is designated as read only.</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-224">**根**</span><span class="sxs-lookup"><span data-stu-id="24e3a-224">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24e3a-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-227">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrFSMountPoint ") </span><span class="sxs-lookup"><span data-stu-id="24e3a-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-228">定義檔案系統根目錄的路徑名稱或其他資訊。</span><span class="sxs-lookup"><span data-stu-id="24e3a-228">Path name or other information that defines the root of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="24e3a-229">**狀態**</span><span class="sxs-lookup"><span data-stu-id="24e3a-229">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24e3a-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24e3a-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24e3a-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24e3a-232">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="24e3a-233">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="24e3a-233">String that indicates the current status of the object.</span></span> <span data-ttu-id="24e3a-234">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="24e3a-234">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="24e3a-235">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="24e3a-235">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="24e3a-236">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="24e3a-236">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="24e3a-237">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="24e3a-237">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="24e3a-238">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="24e3a-238">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="24e3a-239">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="24e3a-239">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="24e3a-240">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24e3a-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="24e3a-241">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="24e3a-241">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="24e3a-242">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-242">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="24e3a-243">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-243">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="24e3a-244">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-244">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24e3a-245">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-245">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="24e3a-246">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-246">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="24e3a-247">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-247">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="24e3a-248">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-248">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="24e3a-249">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-249">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="24e3a-250">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-250">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="24e3a-251">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-251">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="24e3a-252">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-252">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="24e3a-253">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="24e3a-253">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="24e3a-254"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="24e3a-254"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="24e3a-255">備註</span><span class="sxs-lookup"><span data-stu-id="24e3a-255">Remarks</span></span>

<span data-ttu-id="24e3a-256">**Cim \_ FileSystem** 類別衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24e3a-256">The **CIM\_FileSystem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="24e3a-257">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="24e3a-257">WMI does not implement this class.</span></span>

<span data-ttu-id="24e3a-258">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="24e3a-258">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="24e3a-259">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="24e3a-259">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="24e3a-260">規格需求</span><span class="sxs-lookup"><span data-stu-id="24e3a-260">Requirements</span></span>



| <span data-ttu-id="24e3a-261">需求</span><span class="sxs-lookup"><span data-stu-id="24e3a-261">Requirement</span></span> | <span data-ttu-id="24e3a-262">值</span><span class="sxs-lookup"><span data-stu-id="24e3a-262">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24e3a-263">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24e3a-263">Minimum supported client</span></span><br/> | <span data-ttu-id="24e3a-264">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24e3a-264">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24e3a-265">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24e3a-265">Minimum supported server</span></span><br/> | <span data-ttu-id="24e3a-266">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24e3a-266">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24e3a-267">命名空間</span><span class="sxs-lookup"><span data-stu-id="24e3a-267">Namespace</span></span><br/>                | <span data-ttu-id="24e3a-268">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="24e3a-268">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="24e3a-269">MOF</span><span class="sxs-lookup"><span data-stu-id="24e3a-269">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24e3a-270"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="24e3a-270"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="24e3a-271">DLL</span><span class="sxs-lookup"><span data-stu-id="24e3a-271">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24e3a-272"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24e3a-272"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24e3a-273">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24e3a-273">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24e3a-274">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="24e3a-274">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

