---
description: CIM \_ LocalFileSystem 類別代表由電腦系統透過本機所控制的檔案存放區，例如 (直接裝置驅動程式存取) 。
ms.assetid: eab52a25-ca24-4a69-b030-091603d3582c
ms.tgt_platform: multiple
title: CIM_LocalFileSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LocalFileSystem
- CIM_LocalFileSystem.Caption
- CIM_LocalFileSystem.Description
- CIM_LocalFileSystem.InstallDate
- CIM_LocalFileSystem.Name
- CIM_LocalFileSystem.Status
- CIM_LocalFileSystem.AvailableSpace
- CIM_LocalFileSystem.BlockSize
- CIM_LocalFileSystem.CasePreserved
- CIM_LocalFileSystem.CaseSensitive
- CIM_LocalFileSystem.CodeSet
- CIM_LocalFileSystem.CompressionMethod
- CIM_LocalFileSystem.CreationClassName
- CIM_LocalFileSystem.CSCreationClassName
- CIM_LocalFileSystem.CSName
- CIM_LocalFileSystem.EncryptionMethod
- CIM_LocalFileSystem.FileSystemSize
- CIM_LocalFileSystem.MaxFileNameLength
- CIM_LocalFileSystem.ReadOnly
- CIM_LocalFileSystem.Root
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a4a45541a651c92b45baba70828ba99c911d59a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847350"
---
# <a name="cim_localfilesystem-class"></a><span data-ttu-id="03f1b-103">CIM \_ LocalFileSystem 類別</span><span class="sxs-lookup"><span data-stu-id="03f1b-103">CIM\_LocalFileSystem class</span></span>

<span data-ttu-id="03f1b-104">**CIM \_ LocalFileSystem** 類別代表由電腦系統透過本機所控制的檔案存放區，例如 (直接裝置驅動程式存取) 。</span><span class="sxs-lookup"><span data-stu-id="03f1b-104">The **CIM\_LocalFileSystem** class represents the file store controlled by a computer system through local means (for example, direct device-driver access).</span></span> <span data-ttu-id="03f1b-105">檔案存放區可以直接由電腦系統管理，而不需要另一部電腦作為檔案伺服器。</span><span class="sxs-lookup"><span data-stu-id="03f1b-105">The file store can be managed directly by the computer system, without the need for another computer to act as a file server.</span></span> <span data-ttu-id="03f1b-106">但是針對叢集檔案系統，檔案系統是本機的，因此會延遲到叢集。</span><span class="sxs-lookup"><span data-stu-id="03f1b-106">For a clustered file system, however, the file system is local and, therefore, defers to the cluster.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03f1b-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="03f1b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="03f1b-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="03f1b-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="03f1b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="03f1b-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="03f1b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="03f1b-111">語法</span><span class="sxs-lookup"><span data-stu-id="03f1b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{5B6C820A-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LocalFileSystem : CIM_FileSystem
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

## <a name="members"></a><span data-ttu-id="03f1b-112">成員</span><span class="sxs-lookup"><span data-stu-id="03f1b-112">Members</span></span>

<span data-ttu-id="03f1b-113">**CIM \_ LocalFileSystem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="03f1b-113">The **CIM\_LocalFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="03f1b-114">屬性</span><span class="sxs-lookup"><span data-stu-id="03f1b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03f1b-115">屬性</span><span class="sxs-lookup"><span data-stu-id="03f1b-115">Properties</span></span>

<span data-ttu-id="03f1b-116">**CIM \_ LocalFileSystem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="03f1b-116">The **CIM\_LocalFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03f1b-117">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="03f1b-117">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-118">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="03f1b-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-120">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 分割區 \| 002.4 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="03f1b-120">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-121">檔案系統的可用空間量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="03f1b-121">Amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="03f1b-122">如果不明，請輸入0。</span><span class="sxs-lookup"><span data-stu-id="03f1b-122">If unknown, enter 0.</span></span>

<span data-ttu-id="03f1b-123">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-123">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="03f1b-124">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-124">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-125">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="03f1b-125">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-126">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="03f1b-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-128">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-129">區塊儲存和抓取檔案系統的大小。</span><span class="sxs-lookup"><span data-stu-id="03f1b-129">Block size of the file system for data storage and retrieval.</span></span>

<span data-ttu-id="03f1b-130">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="03f1b-131">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-131">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-132">**標題**</span><span class="sxs-lookup"><span data-stu-id="03f1b-132">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="03f1b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-135">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-136">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="03f1b-136">A short textual description of the object.</span></span>

<span data-ttu-id="03f1b-137">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-138">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="03f1b-138">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-139">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="03f1b-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-141">若 **為 TRUE**，則會保留檔案名的大小寫。</span><span class="sxs-lookup"><span data-stu-id="03f1b-141">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="03f1b-142">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-142">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-143">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="03f1b-143">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-144">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="03f1b-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-146">若 **為 TRUE**，則支援區分大小寫的檔案名。</span><span class="sxs-lookup"><span data-stu-id="03f1b-146">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="03f1b-147">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-147">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-148">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="03f1b-148">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-149">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="03f1b-149">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-151">定義檔案系統所支援之字元集或編碼方式的陣列。</span><span class="sxs-lookup"><span data-stu-id="03f1b-151">Array that defines the character sets or encoding supported by the file system.</span></span>

<span data-ttu-id="03f1b-152">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-152">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03f1b-153">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="03f1b-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="03f1b-154">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="03f1b-154">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="03f1b-155">**ASCII** (2) </span><span class="sxs-lookup"><span data-stu-id="03f1b-155">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="03f1b-156">**Unicode** (3) </span><span class="sxs-lookup"><span data-stu-id="03f1b-156">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="03f1b-157">**ISO2022** (4) </span><span class="sxs-lookup"><span data-stu-id="03f1b-157">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="03f1b-158">**ISO8859** (5) </span><span class="sxs-lookup"><span data-stu-id="03f1b-158">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="03f1b-159">**擴充的 UNIX 程式碼** (6) </span><span class="sxs-lookup"><span data-stu-id="03f1b-159">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="03f1b-160">**Utf-8** (7) </span><span class="sxs-lookup"><span data-stu-id="03f1b-160">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="03f1b-161">**UCS-2** (8) </span><span class="sxs-lookup"><span data-stu-id="03f1b-161">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03f1b-162">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="03f1b-162">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="03f1b-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-165">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 分割區 \| 002.7」 ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-165">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-166">自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="03f1b-166">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="03f1b-167">如果壓縮配置未知或未描述，請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="03f1b-167">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="03f1b-168">如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="03f1b-168">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="03f1b-169">如果邏輯檔案未壓縮，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="03f1b-169">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="03f1b-170">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-170">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="03f1b-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="03f1b-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-174">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="03f1b-174">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-175">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="03f1b-175">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="03f1b-176">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="03f1b-176">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="03f1b-177">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-177">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-178">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="03f1b-178">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="03f1b-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-181">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未產生」。**CreationClassName**") </span><span class="sxs-lookup"><span data-stu-id="03f1b-181">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-182">設定電腦系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="03f1b-182">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="03f1b-183">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-183">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-184">**CSName**</span><span class="sxs-lookup"><span data-stu-id="03f1b-184">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="03f1b-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-187">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未產生」。**名稱**") </span><span class="sxs-lookup"><span data-stu-id="03f1b-187">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-188">設定電腦系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="03f1b-188">Scoping computer system's name.</span></span>

<span data-ttu-id="03f1b-189">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-189">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-190">**說明**</span><span class="sxs-lookup"><span data-stu-id="03f1b-190">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="03f1b-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-193">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-193">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-194">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="03f1b-194">A textual description of the object.</span></span>

<span data-ttu-id="03f1b-195">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-196">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="03f1b-196">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="03f1b-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-199">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 分割區 \| 002.8」 ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-200">識別用來加密邏輯檔案之演算法或工具的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="03f1b-200">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="03f1b-201">如果未 indulged 加密配置 (基於安全性理由（例如) ），請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="03f1b-201">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="03f1b-202">如果檔案已加密，但其加密配置不明或未洩漏，請使用「加密」。</span><span class="sxs-lookup"><span data-stu-id="03f1b-202">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="03f1b-203">如果邏輯檔案未加密，請使用「未加密」。</span><span class="sxs-lookup"><span data-stu-id="03f1b-203">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="03f1b-204">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-204">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-205">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="03f1b-205">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-206">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="03f1b-206">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-208">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-208">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-209">檔案系統的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="03f1b-209">Size of the file system, in bytes.</span></span> <span data-ttu-id="03f1b-210">如果不明，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="03f1b-210">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="03f1b-211">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-211">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="03f1b-212">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-212">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-213">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="03f1b-213">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-214">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="03f1b-214">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-216">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="03f1b-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-217">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="03f1b-217">Indicates when the object was installed.</span></span> <span data-ttu-id="03f1b-218">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="03f1b-218">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="03f1b-219">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-219">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-220">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="03f1b-220">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-221">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="03f1b-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-223">檔案系統內檔案名的最大長度。</span><span class="sxs-lookup"><span data-stu-id="03f1b-223">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="03f1b-224">值為 0 (零) 表示檔案名的長度沒有限制。</span><span class="sxs-lookup"><span data-stu-id="03f1b-224">A value of 0 (zero) indicates that there is no limit to the file name length.</span></span>

<span data-ttu-id="03f1b-225">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-225">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-226">**名稱**</span><span class="sxs-lookup"><span data-stu-id="03f1b-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="03f1b-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-229">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-229">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-230">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="03f1b-230">Label by which the object is known.</span></span> <span data-ttu-id="03f1b-231">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="03f1b-231">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="03f1b-232">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-232">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-233">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="03f1b-233">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-234">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="03f1b-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-236">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrFSAccess ") </span><span class="sxs-lookup"><span data-stu-id="03f1b-236">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-237">若 **為 TRUE**，則會將檔案系統指定為唯讀。</span><span class="sxs-lookup"><span data-stu-id="03f1b-237">If **TRUE**, the file system is designated as read only.</span></span>

<span data-ttu-id="03f1b-238">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-238">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-239">**根**</span><span class="sxs-lookup"><span data-stu-id="03f1b-239">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="03f1b-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-242">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrFSMountPoint ") </span><span class="sxs-lookup"><span data-stu-id="03f1b-242">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-243">定義檔案系統根目錄的路徑名稱或其他資訊。</span><span class="sxs-lookup"><span data-stu-id="03f1b-243">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="03f1b-244">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-244">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f1b-245">**狀態**</span><span class="sxs-lookup"><span data-stu-id="03f1b-245">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f1b-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="03f1b-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03f1b-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f1b-248">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-248">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="03f1b-249">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="03f1b-249">String that indicates the current status of the object.</span></span> <span data-ttu-id="03f1b-250">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="03f1b-250">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="03f1b-251">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="03f1b-251">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="03f1b-252">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="03f1b-252">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="03f1b-253">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="03f1b-253">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="03f1b-254">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="03f1b-254">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="03f1b-255">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="03f1b-255">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="03f1b-256">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-256">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="03f1b-257">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="03f1b-257">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="03f1b-258">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-258">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="03f1b-259">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-259">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="03f1b-260">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-260">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03f1b-261">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-261">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="03f1b-262">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-262">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="03f1b-263">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-263">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="03f1b-264">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-264">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="03f1b-265">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-265">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="03f1b-266">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-266">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="03f1b-267">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-267">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="03f1b-268">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-268">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="03f1b-269">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="03f1b-269">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="03f1b-270"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="03f1b-270"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="03f1b-271">備註</span><span class="sxs-lookup"><span data-stu-id="03f1b-271">Remarks</span></span>

<span data-ttu-id="03f1b-272">**Cim \_ LocalFileSystem** 類別衍生自 [**cim \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="03f1b-272">The **CIM\_LocalFileSystem** class is derived from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="03f1b-273">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="03f1b-273">WMI does not implement this class.</span></span>

<span data-ttu-id="03f1b-274">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="03f1b-274">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="03f1b-275">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="03f1b-275">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="03f1b-276">規格需求</span><span class="sxs-lookup"><span data-stu-id="03f1b-276">Requirements</span></span>



| <span data-ttu-id="03f1b-277">需求</span><span class="sxs-lookup"><span data-stu-id="03f1b-277">Requirement</span></span> | <span data-ttu-id="03f1b-278">值</span><span class="sxs-lookup"><span data-stu-id="03f1b-278">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03f1b-279">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03f1b-279">Minimum supported client</span></span><br/> | <span data-ttu-id="03f1b-280">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03f1b-280">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03f1b-281">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03f1b-281">Minimum supported server</span></span><br/> | <span data-ttu-id="03f1b-282">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03f1b-282">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03f1b-283">命名空間</span><span class="sxs-lookup"><span data-stu-id="03f1b-283">Namespace</span></span><br/>                | <span data-ttu-id="03f1b-284">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="03f1b-284">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03f1b-285">MOF</span><span class="sxs-lookup"><span data-stu-id="03f1b-285">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03f1b-286"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="03f1b-286"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03f1b-287">DLL</span><span class="sxs-lookup"><span data-stu-id="03f1b-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03f1b-288"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03f1b-288"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03f1b-289">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03f1b-289">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f1b-290">**CIM \_ 檔案系統**</span><span class="sxs-lookup"><span data-stu-id="03f1b-290">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> </dl>

 

