---
description: 表示以 Windows 為基礎的環境中的使用中網路連接。
ms.assetid: e16e5f13-ea28-4d75-9978-4ff2ef5e5506
ms.tgt_platform: multiple
title: Win32_NetworkConnection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkConnection
- Win32_NetworkConnection.Caption
- Win32_NetworkConnection.Description
- Win32_NetworkConnection.InstallDate
- Win32_NetworkConnection.Status
- Win32_NetworkConnection.AccessMask
- Win32_NetworkConnection.Comment
- Win32_NetworkConnection.ConnectionState
- Win32_NetworkConnection.ConnectionType
- Win32_NetworkConnection.DisplayType
- Win32_NetworkConnection.LocalName
- Win32_NetworkConnection.Name
- Win32_NetworkConnection.Persistent
- Win32_NetworkConnection.ProviderName
- Win32_NetworkConnection.RemoteName
- Win32_NetworkConnection.RemotePath
- Win32_NetworkConnection.ResourceType
- Win32_NetworkConnection.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96d91008ff8ad2f947e6c9957d16c4f007d15e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689132"
---
# <a name="win32_networkconnection-class"></a><span data-ttu-id="0a88c-103">Win32 \_ NetworkConnection 類別</span><span class="sxs-lookup"><span data-stu-id="0a88c-103">Win32\_NetworkConnection class</span></span>

<span data-ttu-id="0a88c-104">**Win32 \_ NetworkConnection** [WMI 類別](../wmisdk/retrieving-a-class.md)代表以 Windows 為基礎的環境中的作用中網路連接。</span><span class="sxs-lookup"><span data-stu-id="0a88c-104">The **Win32\_NetworkConnection** [WMI class](../wmisdk/retrieving-a-class.md)represents an active network connection in a Windows-based environment.</span></span>

<span data-ttu-id="0a88c-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0a88c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0a88c-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="0a88c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a88c-107">語法</span><span class="sxs-lookup"><span data-stu-id="0a88c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkConnection : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  string   Comment;
  string   ConnectionState;
  string   ConnectionType;
  string   DisplayType;
  string   LocalName;
  string   Name;
  boolean  Persistent;
  string   ProviderName;
  string   RemoteName;
  string   RemotePath;
  string   ResourceType;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="0a88c-108">成員</span><span class="sxs-lookup"><span data-stu-id="0a88c-108">Members</span></span>

<span data-ttu-id="0a88c-109">**Win32 \_ NetworkConnection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0a88c-109">The **Win32\_NetworkConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="0a88c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="0a88c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a88c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="0a88c-111">Properties</span></span>

<span data-ttu-id="0a88c-112">**Win32 \_ NetworkConnection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0a88c-112">The **Win32\_NetworkConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0a88c-113">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="0a88c-113">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0a88c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-116">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-116">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-117">由使用者或群組所持有之指定檔案或目錄的存取權限清單，而該檔案是由其傳回的實例。</span><span class="sxs-lookup"><span data-stu-id="0a88c-117">List of access rights to the given file or directory held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="0a88c-118">在 FAT 磁片區上，會改為傳回 [ **完整 \_ 存取** ] 值，表示物件上未設定任何安全性。</span><span class="sxs-lookup"><span data-stu-id="0a88c-118">On FAT volumes, the **FULL\_ACCESS** value is returned instead, indicating no security has been set on the object.</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="0a88c-119"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**檔案 \_讀取 \_ 資料 (檔) 或檔案 \_ 清單 \_ 目錄 (目錄)** (1) </span><span class="sxs-lookup"><span data-stu-id="0a88c-119"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0a88c-120">授與從檔案讀取資料的許可權。</span><span class="sxs-lookup"><span data-stu-id="0a88c-120">Grants the right to read data from the file.</span></span> <span data-ttu-id="0a88c-121">若為目錄，此值會授與許可權來列出目錄的內容。</span><span class="sxs-lookup"><span data-stu-id="0a88c-121">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="0a88c-122"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**檔案 \_寫入 \_ 資料 (檔案) 或檔案 \_ 新增檔案 \_ (目錄)** (2) </span><span class="sxs-lookup"><span data-stu-id="0a88c-122"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0a88c-123">授與將資料寫入檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="0a88c-123">Grants the right to write data to the file.</span></span> <span data-ttu-id="0a88c-124">若為目錄，此值會授與在目錄中建立檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="0a88c-124">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span data-ttu-id="0a88c-125"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**檔案 \_\_將資料附加)  (檔案，或 \_ 將檔案新增 \_ 子目錄** (4) </span><span class="sxs-lookup"><span data-stu-id="0a88c-125"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0a88c-126">授與將資料附加至檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="0a88c-126">Grants the right to append data to the file.</span></span> <span data-ttu-id="0a88c-127">若為目錄，此值會授與建立子目錄的許可權。</span><span class="sxs-lookup"><span data-stu-id="0a88c-127">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="0a88c-128"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**檔案 \_讀取 \_ EA** (8) </span><span class="sxs-lookup"><span data-stu-id="0a88c-128"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="0a88c-129">授與讀取擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="0a88c-129">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="0a88c-130"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**檔案 \_將 \_ EA 寫入** (16) </span><span class="sxs-lookup"><span data-stu-id="0a88c-130"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="0a88c-131">授予寫入擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="0a88c-131">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="0a88c-132"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**檔案 \_執行 (檔案) 或檔案往返 \_ (目錄)** (32) </span><span class="sxs-lookup"><span data-stu-id="0a88c-132"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="0a88c-133">授與許可權來執行檔案。</span><span class="sxs-lookup"><span data-stu-id="0a88c-133">Grants the right to execute a file.</span></span> <span data-ttu-id="0a88c-134">若為目錄，可以進行目錄的往返。</span><span class="sxs-lookup"><span data-stu-id="0a88c-134">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="0a88c-135"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**檔案 \_刪除 \_ 子 (目錄)** (64) </span><span class="sxs-lookup"><span data-stu-id="0a88c-135"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="0a88c-136">授與刪除目錄的許可權，以及它所包含的所有檔案 (其子) ，即使檔案是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="0a88c-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="0a88c-137"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**檔案 \_讀取 \_ 屬性** (128) </span><span class="sxs-lookup"><span data-stu-id="0a88c-137"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="0a88c-138">授與讀取檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="0a88c-138">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="0a88c-139"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**檔案 \_將 \_ 屬性寫入** (256) </span><span class="sxs-lookup"><span data-stu-id="0a88c-139"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="0a88c-140">授與變更檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="0a88c-140">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="0a88c-141"><span id="DELETE"></span><span id="delete"></span>**刪除** (65536) </span><span class="sxs-lookup"><span data-stu-id="0a88c-141"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="0a88c-142">授與刪除存取權。</span><span class="sxs-lookup"><span data-stu-id="0a88c-142">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="0a88c-143"><span id="READ_CONTROL"></span><span id="read_control"></span>**讀取 \_控制** (131072) </span><span class="sxs-lookup"><span data-stu-id="0a88c-143"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="0a88c-144">授與安全描述項和擁有者的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="0a88c-144">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="0a88c-145"><span id="WRITE_DAC"></span><span id="write_dac"></span>**寫入 \_DAC** (262144) </span><span class="sxs-lookup"><span data-stu-id="0a88c-145"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="0a88c-146">授與任意存取控制清單 (DACL) 的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="0a88c-146">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="0a88c-147"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**寫入 \_擁有** 者 (524288) </span><span class="sxs-lookup"><span data-stu-id="0a88c-147"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="0a88c-148">指派寫入擁有者。</span><span class="sxs-lookup"><span data-stu-id="0a88c-148">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="0a88c-149"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**同步處理** (1048576) </span><span class="sxs-lookup"><span data-stu-id="0a88c-149"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="0a88c-150">同步存取，並允許進程等候物件進入已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="0a88c-150">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0a88c-151">**標題**</span><span class="sxs-lookup"><span data-stu-id="0a88c-151">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0a88c-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-154">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-154">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-155">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="0a88c-155">A short textual description of the object.</span></span>

<span data-ttu-id="0a88c-156">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0a88c-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a88c-157">**註解**</span><span class="sxs-lookup"><span data-stu-id="0a88c-157">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0a88c-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-160">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Windows 網路結構 \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| *lpComment*" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|*lpComment*")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-161">網路提供者所提供的批註。</span><span class="sxs-lookup"><span data-stu-id="0a88c-161">Comment supplied by the network provider.</span></span>

</dd> <dt>

<span data-ttu-id="0a88c-162">**ConnectionState**</span><span class="sxs-lookup"><span data-stu-id="0a88c-162">**ConnectionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0a88c-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-165">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (20) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 網路管理結構 \| [**使用 \_ INFO \_ 1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1) \| **ui1 \_ status**" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-165">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (20), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USE\_INFO\_1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1)\|**ui1\_status**")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-166">網路連接的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0a88c-166">Current state of the network connection.</span></span>

<dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

<span data-ttu-id="0a88c-167">**連接** 的 ( 「已連線」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-167">**Connected** ("Connected")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0a88c-168">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-168">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0a88c-169">**暫停** ( 「已暫停」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-169">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

<span data-ttu-id="0a88c-170">**中斷** 連線 ( 「已中斷連線」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-170">**Disconnected** ("Disconnected")</span></span>


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

<span data-ttu-id="0a88c-171">**連接** ( 「正在連接」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-171">**Connecting** ("Connecting")</span></span>


</dt> <dd></dd> <dt>

<span id="Reconnecting"></span><span id="reconnecting"></span><span id="RECONNECTING"></span>

<span data-ttu-id="0a88c-172">重新 **連接** ( 「重新連接」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-172">**Reconnecting** ("Reconnecting")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0a88c-173">**ConnectionType**</span><span class="sxs-lookup"><span data-stu-id="0a88c-173">**ConnectionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0a88c-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-176">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Windows 網路結構 \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwScope**" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwScope**")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-177">用來連線到網路之連接的持續性類型。</span><span class="sxs-lookup"><span data-stu-id="0a88c-177">Persistence type of the connection used for connecting to the network.</span></span>

<dt>

<span id="Current_Connection"></span><span id="current_connection"></span><span id="CURRENT_CONNECTION"></span>

<span data-ttu-id="0a88c-178">**目前的連接** ( 目前的連線」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-178">**Current Connection** ("Current Connection")</span></span>


</dt> <dd></dd> <dt>

<span id="Persistent_Connection"></span><span id="persistent_connection"></span><span id="PERSISTENT_CONNECTION"></span>

<span data-ttu-id="0a88c-179">**持續** 連線 ( 「持續連線」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-179">**Persistent Connection** ("Persistent Connection")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0a88c-180">**說明**</span><span class="sxs-lookup"><span data-stu-id="0a88c-180">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0a88c-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-183">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-183">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-184">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="0a88c-184">A textual description of the object.</span></span>

<span data-ttu-id="0a88c-185">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0a88c-185">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a88c-186">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="0a88c-186">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0a88c-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-189">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Windows 網路結構 \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwDisplayType**" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwDisplayType**")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-190">網路物件應顯示在網路流覽使用者介面中。</span><span class="sxs-lookup"><span data-stu-id="0a88c-190">Network object should be displayed in a network browsing user interface.</span></span>

<dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>

<span data-ttu-id="0a88c-191">**網域** ( "domain" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-191">**Domain** ("Domain")</span></span>


</dt> <dd></dd> <dt>

<span id="Generic"></span><span id="generic"></span><span id="GENERIC"></span>

<span data-ttu-id="0a88c-192">**泛型** ( "generic" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-192">**Generic** ("Generic")</span></span>


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="0a88c-193">**伺服器** ( "server" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-193">**Server** ("Server")</span></span>


</dt> <dd></dd> <dt>

<span id="Share"></span><span id="share"></span><span id="SHARE"></span>

<span data-ttu-id="0a88c-194">**共用** ( 「共用」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-194">**Share** ("Share")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0a88c-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0a88c-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-196">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0a88c-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-198">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="0a88c-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-199">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="0a88c-199">Indicates when the object was installed.</span></span> <span data-ttu-id="0a88c-200">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="0a88c-200">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0a88c-201">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0a88c-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a88c-202">**LocalName**</span><span class="sxs-lookup"><span data-stu-id="0a88c-202">**LocalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0a88c-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-205">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Windows 網路結構 \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpLocalName**" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpLocalName**")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-206">已連線網路裝置的本機名稱。</span><span class="sxs-lookup"><span data-stu-id="0a88c-206">Local name of the connected network device.</span></span>

<span data-ttu-id="0a88c-207">範例： "c： \\ public"</span><span class="sxs-lookup"><span data-stu-id="0a88c-207">Example: "c:\\public"</span></span>

</dd> <dt>

<span data-ttu-id="0a88c-208">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0a88c-208">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-209">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0a88c-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-211">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Name" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Windows 網路結構 \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-211">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-212">目前網路連接的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a88c-212">Name of the current network connection.</span></span> <span data-ttu-id="0a88c-213">它是 **RemoteName** 和 **LocalName** 中的值組合。</span><span class="sxs-lookup"><span data-stu-id="0a88c-213">It is the combination of the values in **RemoteName** and **LocalName**.</span></span>

<span data-ttu-id="0a88c-214">範例： " \\ \\ NTRELEASE (c： \\ public) "</span><span class="sxs-lookup"><span data-stu-id="0a88c-214">Example: "\\\\NTRELEASE (c:\\public)"</span></span>

</dd> <dt>

<span data-ttu-id="0a88c-215">**持續**</span><span class="sxs-lookup"><span data-stu-id="0a88c-215">**Persistent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-216">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0a88c-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-218">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Windows 網路功能 \| [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Functions\|[**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-219">作業系統會在下一次登入時自動重新連接連線。</span><span class="sxs-lookup"><span data-stu-id="0a88c-219">Connection will be reconnected automatically by the operating system on the next logon.</span></span>

</dd> <dt>

<span data-ttu-id="0a88c-220">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="0a88c-220">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-221">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0a88c-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-223">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Windows 網路結構 \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpProvider**" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpProvider**")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-224">擁有資源的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="0a88c-224">Name of the provider that owns the resource.</span></span> <span data-ttu-id="0a88c-225">如果提供者名稱未知，則這個屬性可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="0a88c-225">This property can be **NULL** if the provider name is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="0a88c-226">**RemoteName**</span><span class="sxs-lookup"><span data-stu-id="0a88c-226">**RemoteName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0a88c-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-229">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Windows 網路結構 \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpRemoteName**")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-230">網路資源的遠端網路資源名稱。</span><span class="sxs-lookup"><span data-stu-id="0a88c-230">Remote network resource name for a network resource.</span></span> <span data-ttu-id="0a88c-231">若為目前或持續連線， **RemoteName** 會在 **LocalName** 屬性中包含與值名稱相關聯的網路名稱。</span><span class="sxs-lookup"><span data-stu-id="0a88c-231">For a current or persistent connection, **RemoteName** contains the network name associated with the name of the value in the **LocalName** property.</span></span> <span data-ttu-id="0a88c-232">**RemoteName** 中的名稱必須遵循網路提供者的命名慣例。</span><span class="sxs-lookup"><span data-stu-id="0a88c-232">The name in **RemoteName** must follow the network provider's naming conventions.</span></span>

<span data-ttu-id="0a88c-233">範例： " \\ \\ NTRELEASE"</span><span class="sxs-lookup"><span data-stu-id="0a88c-233">Example: "\\\\NTRELEASE"</span></span>

</dd> <dt>

<span data-ttu-id="0a88c-234">**[RemotePath]**</span><span class="sxs-lookup"><span data-stu-id="0a88c-234">**RemotePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-235">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0a88c-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-237">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Windows 網路結構 \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-237">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpRemoteName**")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-238">網路資源的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="0a88c-238">Full path to the network resource.</span></span>

<span data-ttu-id="0a88c-239">範例： " \\ \\ infosrv1 \\ public"</span><span class="sxs-lookup"><span data-stu-id="0a88c-239">Example: "\\\\infosrv1\\public"</span></span>

</dd> <dt>

<span data-ttu-id="0a88c-240">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="0a88c-240">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-241">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0a88c-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-243">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Windows 網路結構 \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwType**" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-243">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwType**")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-244">要列舉或連接的資源類型。</span><span class="sxs-lookup"><span data-stu-id="0a88c-244">Type of resource to enumerate or connect to.</span></span>

<dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>

<span data-ttu-id="0a88c-245">**磁片** ( 「磁片」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-245">**Disk** ("Disk")</span></span>


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="0a88c-246">**列印** ( "print" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-246">**Print** ("Print")</span></span>


</dt> <dd></dd> <dt>

<span id="Any"></span><span id="any"></span><span id="ANY"></span>

<span data-ttu-id="0a88c-247">**任何** ( 「任何」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-247">**Any** ("Any")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0a88c-248">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0a88c-248">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0a88c-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-251">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-251">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-252">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="0a88c-252">String that indicates the current status of the object.</span></span> <span data-ttu-id="0a88c-253">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="0a88c-253">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0a88c-254">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="0a88c-254">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0a88c-255">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="0a88c-255">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0a88c-256">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="0a88c-256">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0a88c-257">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="0a88c-257">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0a88c-258">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="0a88c-258">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0a88c-259">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0a88c-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0a88c-260">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="0a88c-260">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0a88c-261">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-261">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0a88c-262">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-262">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0a88c-263">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-263">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0a88c-264">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-264">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0a88c-265">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-265">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0a88c-266">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-266">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0a88c-267">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-267">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0a88c-268">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-268">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0a88c-269">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-269">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0a88c-270">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-270">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0a88c-271">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-271">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0a88c-272">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-272">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0a88c-273">**使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="0a88c-273">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a88c-274">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0a88c-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0a88c-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a88c-276">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Windows 網路功能 \| [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)" ) </span><span class="sxs-lookup"><span data-stu-id="0a88c-276">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Functions\|[**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)")</span></span>
</dt> </dl>

<span data-ttu-id="0a88c-277">用來建立網路連線的使用者名稱或預設使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="0a88c-277">User name or the default user name used to establish a network connection.</span></span>

<span data-ttu-id="0a88c-278">範例： "SYSTEM"</span><span class="sxs-lookup"><span data-stu-id="0a88c-278">Example: "SYSTEM"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a88c-279">備註</span><span class="sxs-lookup"><span data-stu-id="0a88c-279">Remarks</span></span>

<span data-ttu-id="0a88c-280">**Win32 \_ NetworkConnection** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0a88c-280">The **Win32\_NetworkConnection** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0a88c-281">範例</span><span class="sxs-lookup"><span data-stu-id="0a88c-281">Examples</span></span>

<span data-ttu-id="0a88c-282">下列 VBScript 程式碼範例會抓取局域網路連接的資訊。</span><span class="sxs-lookup"><span data-stu-id="0a88c-282">The following VBScript code sample retrieves information on the local network connection.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\Root\CIMv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_NetworkConnection",,48)
For Each objItem in colItems
    Wscript.Echo "AccessMask: " & objItem.AccessMask
    Wscript.Echo "Caption: " & objItem.Caption
    Wscript.Echo "Comment: " & objItem.Comment
    Wscript.Echo "ConnectionState: " & objItem.ConnectionState
    Wscript.Echo "ConnectionType: " & objItem.ConnectionType
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo "DisplayType: " & objItem.DisplayType
    Wscript.Echo "InstallDate: " & objItem.InstallDate
    Wscript.Echo "LocalName: " & objItem.LocalName
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Persistent: " & objItem.Persistent
    Wscript.Echo "ProviderName: " & objItem.ProviderName
    Wscript.Echo "RemoteName: " & objItem.RemoteName
    Wscript.Echo "RemotePath: " & objItem.RemotePath
    Wscript.Echo "ResourceType: " & objItem.ResourceType
    Wscript.Echo "Status: " & objItem.Status
    Wscript.Echo "UserName: " & objItem.UserName
Next
```



## <a name="requirements"></a><span data-ttu-id="0a88c-283">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a88c-283">Requirements</span></span>



| <span data-ttu-id="0a88c-284">需求</span><span class="sxs-lookup"><span data-stu-id="0a88c-284">Requirement</span></span> | <span data-ttu-id="0a88c-285">值</span><span class="sxs-lookup"><span data-stu-id="0a88c-285">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a88c-286">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a88c-286">Minimum supported client</span></span><br/> | <span data-ttu-id="0a88c-287">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a88c-287">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0a88c-288">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a88c-288">Minimum supported server</span></span><br/> | <span data-ttu-id="0a88c-289">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a88c-289">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0a88c-290">命名空間</span><span class="sxs-lookup"><span data-stu-id="0a88c-290">Namespace</span></span><br/>                | <span data-ttu-id="0a88c-291">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0a88c-291">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0a88c-292">MOF</span><span class="sxs-lookup"><span data-stu-id="0a88c-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a88c-293"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a88c-293"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a88c-294">DLL</span><span class="sxs-lookup"><span data-stu-id="0a88c-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a88c-295"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a88c-295"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a88c-296">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a88c-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a88c-297">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="0a88c-297">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="0a88c-298">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="0a88c-298">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
