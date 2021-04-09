---
description: CIM \_ NFS 類別代表從電腦系統使用網路檔案系統 (NFS) 通訊協定掛接的遠端檔案系統。
ms.assetid: 24eba28f-fbd5-4aa3-a7c7-a611269d55ac
ms.tgt_platform: multiple
title: CIM_NFS 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NFS
- CIM_NFS.AttributeCaching
- CIM_NFS.AttributeCachingForDirectoriesMax
- CIM_NFS.AttributeCachingForDirectoriesMin
- CIM_NFS.AttributeCachingForRegularFilesMax
- CIM_NFS.AttributeCachingForRegularFilesMin
- CIM_NFS.AvailableSpace
- CIM_NFS.BlockSize
- CIM_NFS.Caption
- CIM_NFS.CasePreserved
- CIM_NFS.CaseSensitive
- CIM_NFS.CodeSet
- CIM_NFS.CompressionMethod
- CIM_NFS.CreationClassName
- CIM_NFS.CSCreationClassName
- CIM_NFS.CSName
- CIM_NFS.Description
- CIM_NFS.EncryptionMethod
- CIM_NFS.FileSystemSize
- CIM_NFS.ForegroundMount
- CIM_NFS.HardMount
- CIM_NFS.InstallDate
- CIM_NFS.Interrupt
- CIM_NFS.MaxFileNameLength
- CIM_NFS.MountFailureRetries
- CIM_NFS.Name
- CIM_NFS.ReadBufferSize
- CIM_NFS.ReadOnly
- CIM_NFS.RetransmissionAttempts
- CIM_NFS.RetransmissionTimeout
- CIM_NFS.Root
- CIM_NFS.ServerCommunicationPort
- CIM_NFS.Status
- CIM_NFS.WriteBufferSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0dcfb44fdcd035ca47cbe3056da2a081ef2ae07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688971"
---
# <a name="cim_nfs-class"></a><span data-ttu-id="4de20-103">CIM \_ NFS 類別</span><span class="sxs-lookup"><span data-stu-id="4de20-103">CIM\_NFS class</span></span>

<span data-ttu-id="4de20-104">**CIM \_ NFS** 類別代表從電腦系統使用網路檔案系統 (NFS) 通訊協定掛接的遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="4de20-104">The **CIM\_NFS** class represents a remote file system that is mounted, using the network file system (NFS) protocol, from a computer system.</span></span> <span data-ttu-id="4de20-105">NFS 物件的屬性會對應至掛接的操作方面，並代表 NFS 存取的用戶端設定。</span><span class="sxs-lookup"><span data-stu-id="4de20-105">The properties of the NFS object correspond to the operational aspects of the mount and represent the client-side configuration for NFS access.</span></span> <span data-ttu-id="4de20-106">檔案系統類型應該設定為指出檔案系統出現在用戶端的類型。</span><span class="sxs-lookup"><span data-stu-id="4de20-106">The file system type should be set to indicate the type of file system as it appears to the client.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4de20-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="4de20-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4de20-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="4de20-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4de20-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4de20-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4de20-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="4de20-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4de20-111">語法</span><span class="sxs-lookup"><span data-stu-id="4de20-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4FB-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_NFS : CIM_RemoteFileSystem
{
  boolean  AttributeCaching;
  uint16   AttributeCachingForDirectoriesMax;
  uint16   AttributeCachingForDirectoriesMin;
  uint16   AttributeCachingForRegularFilesMax;
  uint16   AttributeCachingForRegularFilesMin;
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
  boolean  ForegroundMount;
  boolean  HardMount;
  datetime InstallDate;
  boolean  Interrupt;
  uint32   MaxFileNameLength;
  uint16   MountFailureRetries;
  string   Name;
  uint64   ReadBufferSize;
  boolean  ReadOnly;
  uint16   RetransmissionAttempts;
  uint32   RetransmissionTimeout;
  string   Root;
  uint32   ServerCommunicationPort;
  string   Status;
  uint64   WriteBufferSize;
};
```

## <a name="members"></a><span data-ttu-id="4de20-112">成員</span><span class="sxs-lookup"><span data-stu-id="4de20-112">Members</span></span>

<span data-ttu-id="4de20-113">**CIM \_ NFS** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4de20-113">The **CIM\_NFS** class has these types of members:</span></span>

-   [<span data-ttu-id="4de20-114">屬性</span><span class="sxs-lookup"><span data-stu-id="4de20-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4de20-115">屬性</span><span class="sxs-lookup"><span data-stu-id="4de20-115">Properties</span></span>

<span data-ttu-id="4de20-116">**CIM \_ NFS** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4de20-116">The **CIM\_NFS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4de20-117">**AttributeCaching**</span><span class="sxs-lookup"><span data-stu-id="4de20-117">**AttributeCaching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-118">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4de20-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4de20-120">若 **為 TRUE**，則會啟用控制項屬性快取。</span><span class="sxs-lookup"><span data-stu-id="4de20-120">If **TRUE**, control attribute caching is enabled.</span></span> <span data-ttu-id="4de20-121">如果 **為 FALSE**，則會停用控制項屬性快取。</span><span class="sxs-lookup"><span data-stu-id="4de20-121">If **FALSE**, control attribute caching is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="4de20-122">**AttributeCachingForDirectoriesMax**</span><span class="sxs-lookup"><span data-stu-id="4de20-122">**AttributeCachingForDirectoriesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-123">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4de20-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-125">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「秒」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-126">目錄更新後保存快取屬性的最大秒數。</span><span class="sxs-lookup"><span data-stu-id="4de20-126">Maximum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="4de20-127">**AttributeCachingForDirectoriesMin**</span><span class="sxs-lookup"><span data-stu-id="4de20-127">**AttributeCachingForDirectoriesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-128">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4de20-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-130">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「秒」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-131">目錄更新後保存快取屬性的最小秒數。</span><span class="sxs-lookup"><span data-stu-id="4de20-131">Minimum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="4de20-132">**AttributeCachingForRegularFilesMax**</span><span class="sxs-lookup"><span data-stu-id="4de20-132">**AttributeCachingForRegularFilesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-133">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4de20-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-135">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「秒」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-136">檔案修改後保存快取屬性的最大秒數。</span><span class="sxs-lookup"><span data-stu-id="4de20-136">Maximum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="4de20-137">**AttributeCachingForRegularFilesMin**</span><span class="sxs-lookup"><span data-stu-id="4de20-137">**AttributeCachingForRegularFilesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-138">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4de20-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-140">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「秒」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-141">檔案修改後保存快取屬性的最小秒數。</span><span class="sxs-lookup"><span data-stu-id="4de20-141">Minimum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="4de20-142">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="4de20-142">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-143">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4de20-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-145">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 分割區 \| 002.4 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="4de20-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-146">檔案系統的可用空間總量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4de20-146">Total amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="4de20-147">如果不明，請輸入0。</span><span class="sxs-lookup"><span data-stu-id="4de20-147">If unknown, enter 0.</span></span>

<span data-ttu-id="4de20-148">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-148">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="4de20-149">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4de20-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-150">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="4de20-150">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-151">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4de20-151">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-153">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="4de20-153">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-154">檔案系統可以讀取或寫入個別于基礎儲存範圍之外定義之區塊中的資料。</span><span class="sxs-lookup"><span data-stu-id="4de20-154">File systems can read or write data in blocks that are defined independently of the underlying storage extents.</span></span> <span data-ttu-id="4de20-155">這個屬性會針對資料儲存和抓取來捕捉檔案系統的區塊大小。</span><span class="sxs-lookup"><span data-stu-id="4de20-155">This property captures the file system's block size for data storage and retrieval.</span></span>

<span data-ttu-id="4de20-156">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-156">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="4de20-157">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4de20-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-158">**標題**</span><span class="sxs-lookup"><span data-stu-id="4de20-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4de20-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-161">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="4de20-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-162">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="4de20-162">Short textual description of the object.</span></span>

<span data-ttu-id="4de20-163">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-164">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="4de20-164">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-165">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4de20-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4de20-167">若 **為 TRUE**，則會保留檔案名的大小寫。</span><span class="sxs-lookup"><span data-stu-id="4de20-167">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="4de20-168">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-168">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-169">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="4de20-169">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-170">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4de20-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4de20-172">若 **為 TRUE**，則支援區分大小寫的檔案名。</span><span class="sxs-lookup"><span data-stu-id="4de20-172">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="4de20-173">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-173">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-174">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="4de20-174">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-175">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="4de20-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4de20-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4de20-177">檔案系統支援的字元集或編碼。</span><span class="sxs-lookup"><span data-stu-id="4de20-177">Character sets or encoding supported by the file system.</span></span>

<span data-ttu-id="4de20-178">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-178">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4de20-179">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4de20-179">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4de20-180">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4de20-180">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="4de20-181">**ASCII** (2) </span><span class="sxs-lookup"><span data-stu-id="4de20-181">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="4de20-182">**Unicode** (3) </span><span class="sxs-lookup"><span data-stu-id="4de20-182">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="4de20-183">**ISO2022** (4) </span><span class="sxs-lookup"><span data-stu-id="4de20-183">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="4de20-184">**ISO8859** (5) </span><span class="sxs-lookup"><span data-stu-id="4de20-184">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="4de20-185">**擴充的 UNIX 程式碼** (6) </span><span class="sxs-lookup"><span data-stu-id="4de20-185">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="4de20-186">**Utf-8** (7) </span><span class="sxs-lookup"><span data-stu-id="4de20-186">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="4de20-187">**UCS-2** (8) </span><span class="sxs-lookup"><span data-stu-id="4de20-187">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4de20-188">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="4de20-188">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4de20-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-191">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 分割區 \| 002.7」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-191">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-192">自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="4de20-192">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="4de20-193">如果壓縮配置未知或未描述，請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="4de20-193">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="4de20-194">如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="4de20-194">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="4de20-195">如果邏輯檔案未壓縮，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="4de20-195">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="4de20-196">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-196">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-197">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4de20-197">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4de20-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-200">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="4de20-200">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4de20-201">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="4de20-201">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4de20-202">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="4de20-202">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4de20-203">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-203">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-204">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4de20-204">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-205">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4de20-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-207">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未產生」。**CreationClassName**") </span><span class="sxs-lookup"><span data-stu-id="4de20-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-208">設定電腦系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="4de20-208">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="4de20-209">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-209">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-210">**CSName**</span><span class="sxs-lookup"><span data-stu-id="4de20-210">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-211">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4de20-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-213">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未產生」。**名稱**") </span><span class="sxs-lookup"><span data-stu-id="4de20-213">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-214">設定電腦系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="4de20-214">Scoping computer system's name.</span></span>

<span data-ttu-id="4de20-215">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-215">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-216">**說明**</span><span class="sxs-lookup"><span data-stu-id="4de20-216">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4de20-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-219">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="4de20-219">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-220">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="4de20-220">Textual description of the object.</span></span>

<span data-ttu-id="4de20-221">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-222">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="4de20-222">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4de20-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-225">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 分割區 \| 002.8」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-226">識別用來加密邏輯檔案之演算法或工具的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="4de20-226">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="4de20-227">如果未 indulged 加密配置 (基於安全性理由（例如) ），請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="4de20-227">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="4de20-228">如果檔案已加密，但其加密配置不明或未洩漏，請使用「加密」。</span><span class="sxs-lookup"><span data-stu-id="4de20-228">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="4de20-229">如果邏輯檔案未加密，請使用「未加密」。</span><span class="sxs-lookup"><span data-stu-id="4de20-229">If the logical file is not encrypted, use "Not Encrypted".</span></span> <span data-ttu-id="4de20-230">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-230">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-231">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="4de20-231">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-232">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4de20-232">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-234">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="4de20-234">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-235">檔案系統的大小總計（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4de20-235">Total size of the file system, in bytes.</span></span> <span data-ttu-id="4de20-236">如果不明，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="4de20-236">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="4de20-237">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-237">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="4de20-238">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4de20-238">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-239">**ForegroundMount**</span><span class="sxs-lookup"><span data-stu-id="4de20-239">**ForegroundMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-240">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4de20-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4de20-242">若 **為 TRUE**，則會在前景中執行重試。</span><span class="sxs-lookup"><span data-stu-id="4de20-242">If **TRUE**, retries are performed in the foreground.</span></span> <span data-ttu-id="4de20-243">如果 **為 FALSE**，且第一次掛接嘗試失敗，則會在背景中執行重試。</span><span class="sxs-lookup"><span data-stu-id="4de20-243">If **FALSE**, and the first mount attempt fails, retries are performed in the background.</span></span>

</dd> <dt>

<span data-ttu-id="4de20-244">**HardMount**</span><span class="sxs-lookup"><span data-stu-id="4de20-244">**HardMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-245">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4de20-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4de20-247">若 **為 TRUE**，裝載檔案系統之後，就會重試 NFS 要求，直到主機系統回應為止。</span><span class="sxs-lookup"><span data-stu-id="4de20-247">If **TRUE**, after the file system is mounted, NFS requests are retried until the hosting system responds.</span></span> <span data-ttu-id="4de20-248">如果 **為 FALSE**，則掛接檔案系統之後，如果裝載系統沒有回應，就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4de20-248">If **FALSE**, after the file system is mounted, an error is returned if the hosting system does not respond.</span></span>

</dd> <dt>

<span data-ttu-id="4de20-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4de20-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-250">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4de20-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-252">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="4de20-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-253">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="4de20-253">Date and time the object was installed.</span></span> <span data-ttu-id="4de20-254">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="4de20-254">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4de20-255">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-255">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-256">**中斷**</span><span class="sxs-lookup"><span data-stu-id="4de20-256">**Interrupt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-257">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4de20-257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4de20-259">若為 **TRUE**，則允許進行硬掛接的中斷。</span><span class="sxs-lookup"><span data-stu-id="4de20-259">If **TRUE**, interrupts are permitted for hard mounts.</span></span> <span data-ttu-id="4de20-260">如果 **為 FALSE**，則會忽略硬掛接的中斷。</span><span class="sxs-lookup"><span data-stu-id="4de20-260">If **FALSE**, interrupts are ignored for hard mounts.</span></span>

</dd> <dt>

<span data-ttu-id="4de20-261">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="4de20-261">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-262">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4de20-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4de20-264">檔案系統內檔案名的最大長度。</span><span class="sxs-lookup"><span data-stu-id="4de20-264">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="4de20-265">值為 0 (零) 表示檔案名的長度沒有限制。</span><span class="sxs-lookup"><span data-stu-id="4de20-265">A value of 0 (zero)indicates that there is no limit for file name length.</span></span>

<span data-ttu-id="4de20-266">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-266">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-267">**MountFailureRetries**</span><span class="sxs-lookup"><span data-stu-id="4de20-267">**MountFailureRetries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-268">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4de20-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4de20-270">允許的掛接失敗重試次數上限。</span><span class="sxs-lookup"><span data-stu-id="4de20-270">Maximum number of mount failure retries that are allowed.</span></span>

</dd> <dt>

<span data-ttu-id="4de20-271">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4de20-271">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-272">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4de20-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-273">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-274">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="4de20-274">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-275">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="4de20-275">Label by which the object is known.</span></span> <span data-ttu-id="4de20-276">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="4de20-276">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4de20-277">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-277">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-278">**ReadBufferSize**</span><span class="sxs-lookup"><span data-stu-id="4de20-278">**ReadBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-279">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4de20-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-281">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="4de20-281">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-282">讀取緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4de20-282">Read buffer size, in bytes.</span></span>

<span data-ttu-id="4de20-283">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4de20-283">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-284">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="4de20-284">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-285">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4de20-285">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-287">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrFSAccess ") </span><span class="sxs-lookup"><span data-stu-id="4de20-287">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-288">若 **為 TRUE**，則會將檔案系統指定為唯讀。</span><span class="sxs-lookup"><span data-stu-id="4de20-288">If **TRUE**, the file system is designated as read-only.</span></span>

<span data-ttu-id="4de20-289">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-289">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-290">**RetransmissionAttempts**</span><span class="sxs-lookup"><span data-stu-id="4de20-290">**RetransmissionAttempts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-291">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4de20-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4de20-293">允許的 NFS 重新傳輸數目上限。</span><span class="sxs-lookup"><span data-stu-id="4de20-293">Maximum number of NFS retransmissions allowed.</span></span>

</dd> <dt>

<span data-ttu-id="4de20-294">**RetransmissionTimeout**</span><span class="sxs-lookup"><span data-stu-id="4de20-294">**RetransmissionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-295">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4de20-295">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-297">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「十分之一秒」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-297">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of seconds")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-298">NFS 超時，以十分之一秒為限。</span><span class="sxs-lookup"><span data-stu-id="4de20-298">NFS time-out, in tenths of a second.</span></span>

</dd> <dt>

<span data-ttu-id="4de20-299">**根**</span><span class="sxs-lookup"><span data-stu-id="4de20-299">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4de20-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-302">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrFSMountPoint ") </span><span class="sxs-lookup"><span data-stu-id="4de20-302">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-303">定義檔案系統根目錄的路徑名稱或其他資訊。</span><span class="sxs-lookup"><span data-stu-id="4de20-303">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="4de20-304">這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-304">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4de20-305">**ServerCommunicationPort**</span><span class="sxs-lookup"><span data-stu-id="4de20-305">**ServerCommunicationPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-306">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4de20-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4de20-308">遠端電腦系統的 UDP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="4de20-308">Remote computer system's UDP port number.</span></span>

</dd> <dt>

<span data-ttu-id="4de20-309">**狀態**</span><span class="sxs-lookup"><span data-stu-id="4de20-309">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-310">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4de20-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-312">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="4de20-312">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-313">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4de20-313">Current status of the object.</span></span>

<span data-ttu-id="4de20-314">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4de20-315">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="4de20-315">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4de20-316">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="4de20-316">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4de20-317">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-317">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4de20-318">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-318">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4de20-319">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-319">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4de20-320">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-320">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4de20-321">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-321">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4de20-322">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-322">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4de20-323">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-323">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4de20-324">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-324">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4de20-325">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="4de20-325">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4de20-326">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-326">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4de20-327">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="4de20-327">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4de20-328">**WriteBufferSize**</span><span class="sxs-lookup"><span data-stu-id="4de20-328">**WriteBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de20-329">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4de20-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4de20-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4de20-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de20-331">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="4de20-331">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4de20-332">寫入緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4de20-332">Write buffer size, in bytes.</span></span>

<span data-ttu-id="4de20-333">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4de20-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4de20-334">備註</span><span class="sxs-lookup"><span data-stu-id="4de20-334">Remarks</span></span>

<span data-ttu-id="4de20-335">**Cim \_ NFS** 類別衍生自 [**cim \_ RemoteFileSystem**](cim-remotefilesystem.md)。</span><span class="sxs-lookup"><span data-stu-id="4de20-335">The **CIM\_NFS** class is derived from [**CIM\_RemoteFileSystem**](cim-remotefilesystem.md).</span></span>

<span data-ttu-id="4de20-336">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="4de20-336">WMI does not implement this class.</span></span>

<span data-ttu-id="4de20-337">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="4de20-337">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4de20-338">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4de20-338">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4de20-339">規格需求</span><span class="sxs-lookup"><span data-stu-id="4de20-339">Requirements</span></span>



| <span data-ttu-id="4de20-340">需求</span><span class="sxs-lookup"><span data-stu-id="4de20-340">Requirement</span></span> | <span data-ttu-id="4de20-341">值</span><span class="sxs-lookup"><span data-stu-id="4de20-341">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4de20-342">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4de20-342">Minimum supported client</span></span><br/> | <span data-ttu-id="4de20-343">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4de20-343">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4de20-344">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4de20-344">Minimum supported server</span></span><br/> | <span data-ttu-id="4de20-345">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4de20-345">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4de20-346">命名空間</span><span class="sxs-lookup"><span data-stu-id="4de20-346">Namespace</span></span><br/>                | <span data-ttu-id="4de20-347">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4de20-347">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4de20-348">MOF</span><span class="sxs-lookup"><span data-stu-id="4de20-348">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4de20-349"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4de20-349"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4de20-350">DLL</span><span class="sxs-lookup"><span data-stu-id="4de20-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4de20-351"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4de20-351"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4de20-352">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4de20-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4de20-353">**CIM \_ RemoteFileSystem**</span><span class="sxs-lookup"><span data-stu-id="4de20-353">**CIM\_RemoteFileSystem**</span></span>](cim-remotefilesystem.md)
</dt> </dl>

 

