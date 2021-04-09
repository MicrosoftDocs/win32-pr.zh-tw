---
description: CIM \_ RemoteFileSystem 類別代表透過網路相關服務來存取的遠端檔案系統。 在此情況下，檔案存放區是由電腦主控，作為檔案伺服器。
ms.assetid: 932970a8-0ab3-45d8-912d-c4ba7cf433b5
ms.tgt_platform: multiple
title: CIM_RemoteFileSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoteFileSystem
- CIM_RemoteFileSystem.AvailableSpace
- CIM_RemoteFileSystem.BlockSize
- CIM_RemoteFileSystem.Caption
- CIM_RemoteFileSystem.CasePreserved
- CIM_RemoteFileSystem.CaseSensitive
- CIM_RemoteFileSystem.CodeSet
- CIM_RemoteFileSystem.CompressionMethod
- CIM_RemoteFileSystem.CreationClassName
- CIM_RemoteFileSystem.CSCreationClassName
- CIM_RemoteFileSystem.CSName
- CIM_RemoteFileSystem.Description
- CIM_RemoteFileSystem.EncryptionMethod
- CIM_RemoteFileSystem.FileSystemSize
- CIM_RemoteFileSystem.InstallDate
- CIM_RemoteFileSystem.MaxFileNameLength
- CIM_RemoteFileSystem.Name
- CIM_RemoteFileSystem.ReadOnly
- CIM_RemoteFileSystem.Root
- CIM_RemoteFileSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c29e0212ba55b37abd734fb149d118ccc693908
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110257"
---
# <a name="cim_remotefilesystem-class"></a><span data-ttu-id="cfb1e-104">CIM \_ RemoteFileSystem 類別</span><span class="sxs-lookup"><span data-stu-id="cfb1e-104">CIM\_RemoteFileSystem class</span></span>

<span data-ttu-id="cfb1e-105">**CIM \_ RemoteFileSystem** 類別代表透過網路相關服務來存取的遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-105">The **CIM\_RemoteFileSystem** class represents a remote file system that is accessed by way of a network-related service.</span></span> <span data-ttu-id="cfb1e-106">在此情況下，檔案存放區是由電腦主控，作為檔案伺服器。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-106">In this case, the file store is hosted by a computer, which acts as a file server.</span></span> <span data-ttu-id="cfb1e-107">例如，NFS 檔案系統的檔案存放區通常不在電腦系統的本機控制媒體上，也不是透過設備磁碟機直接存取。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-107">For example, the file store for an NFS file system is typically not on a computer system's locally controlled media, nor is it directly accessed through a device driver.</span></span> <span data-ttu-id="cfb1e-108">**CIM \_ RemoteFileSystem** 的子類別包含與檔案系統存取相關的用戶端設定資訊。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-108">Subclasses of **CIM\_RemoteFileSystem** contain client-side configuration information related to the access of the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cfb1e-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cfb1e-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cfb1e-111">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="cfb1e-112">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb1e-113">語法</span><span class="sxs-lookup"><span data-stu-id="cfb1e-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4F9-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_RemoteFileSystem : CIM_FileSystem
{
  uint64   AvailableSpace;
  uint64   BlockSize;
  string   Caption;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  datetime InstallDate;
  uint32   MaxFileNameLength;
  string   Name;
  boolean  ReadOnly;
  string   Root;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="cfb1e-114">成員</span><span class="sxs-lookup"><span data-stu-id="cfb1e-114">Members</span></span>

<span data-ttu-id="cfb1e-115">**CIM \_ RemoteFileSystem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cfb1e-115">The **CIM\_RemoteFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="cfb1e-116">屬性</span><span class="sxs-lookup"><span data-stu-id="cfb1e-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cfb1e-117">屬性</span><span class="sxs-lookup"><span data-stu-id="cfb1e-117">Properties</span></span>

<span data-ttu-id="cfb1e-118">**CIM \_ RemoteFileSystem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-118">The **CIM\_RemoteFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cfb1e-119">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-119">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-120">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-122">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 分割區 \| 002.4 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="cfb1e-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-123">檔案系統的可用空間量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-123">Amount of free space for the file system, in bytes.</span></span> <span data-ttu-id="cfb1e-124">如果不明，請輸入0。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-124">If unknown, enter 0.</span></span>

<span data-ttu-id="cfb1e-125">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-125">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="cfb1e-126">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-127">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-127">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-128">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-130">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-131">形成儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-131">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="cfb1e-132">如果未知，或如果區塊概念無效， (例如，針對匯總範圍、記憶體或邏輯磁片) ，請輸入 1 (一個) 。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-132">If unknown, or if a block concept is not valid, (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="cfb1e-133">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-133">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="cfb1e-134">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-135">**標題**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-135">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-138">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-139">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-139">Textual description of the object.</span></span>

<span data-ttu-id="cfb1e-140">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-141">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-141">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-142">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-144">若 **為 TRUE**，則會保留檔案名的大小寫。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-144">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="cfb1e-145">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-145">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-146">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-146">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-147">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-149">若 **為 TRUE**，則支援區分大小寫的檔案名。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-149">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="cfb1e-150">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-150">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-151">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-151">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-152">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="cfb1e-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-154">檔案系統支援的字元集或編碼。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-154">Character sets or encoding supported by the file system.</span></span> <span data-ttu-id="cfb1e-155">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-155">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cfb1e-156">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-156">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cfb1e-157">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-157">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="cfb1e-158">**ASCII** (2) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-158">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="cfb1e-159">**Unicode** (3) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-159">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="cfb1e-160">**ISO2022** (4) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-160">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="cfb1e-161">**ISO8859** (5) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-161">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="cfb1e-162">**擴充的 UNIX 程式碼** (6) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-162">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="cfb1e-163">**Utf-8** (7) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-163">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="cfb1e-164">**UCS-2** (8) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-164">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cfb1e-165">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-165">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-168">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 分割區 \| 002.7」 ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-169">自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-169">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="cfb1e-170">如果壓縮配置未知或未描述，請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-170">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="cfb1e-171">如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-171">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="cfb1e-172">如果邏輯檔案未壓縮，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-172">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="cfb1e-173">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-173">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-174">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-174">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-177">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-178">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-178">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cfb1e-179">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-179">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cfb1e-180">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-180">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-181">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-181">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-184">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未產生」。**CreationClassName**") </span><span class="sxs-lookup"><span data-stu-id="cfb1e-184">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-185">設定電腦系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-185">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="cfb1e-186">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-186">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-187">**CSName**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-187">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-190">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未產生」。**名稱**") </span><span class="sxs-lookup"><span data-stu-id="cfb1e-190">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-191">設定電腦系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-191">Scoping computer system's name.</span></span>

<span data-ttu-id="cfb1e-192">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-192">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-193">**說明**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-193">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-196">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-196">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-197">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-197">Textual description of the object.</span></span>

<span data-ttu-id="cfb1e-198">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-199">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-199">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-200">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-202">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 分割區 \| 002.8」 ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-203">識別用來加密邏輯檔案之演算法或工具的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-203">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="cfb1e-204">如果未 indulged 加密配置 (基於安全性理由（例如) ），請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-204">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="cfb1e-205">如果檔案已加密，但其加密配置不明或未洩漏，請使用「加密」。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-205">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="cfb1e-206">如果邏輯檔案未加密，請使用「未加密」。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-206">If the logical file is not encrypted, use "Not Encrypted".</span></span> <span data-ttu-id="cfb1e-207">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-207">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-208">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-208">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-209">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-209">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-211">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-211">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-212">檔案系統的大小總計（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-212">Total size of the file system, in bytes.</span></span> <span data-ttu-id="cfb1e-213">如果不明，請輸入0。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-213">If unknown, enter 0.</span></span>

<span data-ttu-id="cfb1e-214">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-214">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="cfb1e-215">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-215">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-216">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-216">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-217">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-217">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-219">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="cfb1e-219">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-220">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-220">Date and time the object was installed.</span></span> <span data-ttu-id="cfb1e-221">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-221">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="cfb1e-222">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-223">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-223">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-224">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-226">檔案系統內檔案名的最大長度。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-226">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="cfb1e-227">值為0表示檔案名為無限制。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-227">A value of 0 indicates that file name length is unlimited.</span></span>

<span data-ttu-id="cfb1e-228">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-228">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-229">**名稱**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-229">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-232">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-232">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-233">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-233">Label by which the object is known.</span></span> <span data-ttu-id="cfb1e-234">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-234">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="cfb1e-235">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-235">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-236">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-236">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-237">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-239">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrFSAccess ") </span><span class="sxs-lookup"><span data-stu-id="cfb1e-239">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-240">若 **為 TRUE**，則會將檔案系統指定為唯讀。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-240">If **TRUE**, the file system is designated as read-only.</span></span>

<span data-ttu-id="cfb1e-241">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-241">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-242">**根**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-242">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-245">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrFSMountPoint ") </span><span class="sxs-lookup"><span data-stu-id="cfb1e-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-246">定義檔案系統根目錄的路徑名稱或其他資訊。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-246">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="cfb1e-247">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-247">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfb1e-248">**狀態**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-248">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfb1e-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cfb1e-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfb1e-251">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-251">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cfb1e-252">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-252">Current status of the object.</span></span>

<span data-ttu-id="cfb1e-253">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-253">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cfb1e-254">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="cfb1e-254">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cfb1e-255">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-255">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cfb1e-256">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-256">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cfb1e-257">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-257">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cfb1e-258">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-258">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cfb1e-259">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-259">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cfb1e-260">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-260">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cfb1e-261">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-261">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cfb1e-262">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-262">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cfb1e-263">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-263">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cfb1e-264">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-264">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cfb1e-265">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-265">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cfb1e-266">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="cfb1e-266">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="cfb1e-267"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cfb1e-267"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="cfb1e-268">備註</span><span class="sxs-lookup"><span data-stu-id="cfb1e-268">Remarks</span></span>

<span data-ttu-id="cfb1e-269">**Cim \_ RemoteFileSystem** 類別衍生自 [**cim \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-269">The **CIM\_RemoteFileSystem** class is derived from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="cfb1e-270">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-270">WMI does not implement this class.</span></span>

<span data-ttu-id="cfb1e-271">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-271">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cfb1e-272">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="cfb1e-272">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfb1e-273">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfb1e-273">Requirements</span></span>



| <span data-ttu-id="cfb1e-274">需求</span><span class="sxs-lookup"><span data-stu-id="cfb1e-274">Requirement</span></span> | <span data-ttu-id="cfb1e-275">值</span><span class="sxs-lookup"><span data-stu-id="cfb1e-275">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb1e-276">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cfb1e-276">Minimum supported client</span></span><br/> | <span data-ttu-id="cfb1e-277">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cfb1e-277">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cfb1e-278">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cfb1e-278">Minimum supported server</span></span><br/> | <span data-ttu-id="cfb1e-279">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfb1e-279">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cfb1e-280">命名空間</span><span class="sxs-lookup"><span data-stu-id="cfb1e-280">Namespace</span></span><br/>                | <span data-ttu-id="cfb1e-281">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cfb1e-281">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cfb1e-282">MOF</span><span class="sxs-lookup"><span data-stu-id="cfb1e-282">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfb1e-283"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="cfb1e-283"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfb1e-284">DLL</span><span class="sxs-lookup"><span data-stu-id="cfb1e-284">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfb1e-285"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfb1e-285"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfb1e-286">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfb1e-286">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfb1e-287">**CIM \_ 檔案系統**</span><span class="sxs-lookup"><span data-stu-id="cfb1e-287">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> </dl>

 

