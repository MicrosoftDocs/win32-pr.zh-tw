---
title: Win32_RDMSCollectionProperties 類別
description: 管理虛擬桌面集合的屬性。
ms.assetid: 8c533284-aa7b-4c47-b0a3-33307c4c805b
ms.tgt_platform: multiple
keywords:
- Win32_RDMSCollectionProperties 類別遠端桌面服務
- Win32_RDMSCollectionProperties 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties.Alias
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopMachineName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopHost
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopGuid
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopOsversion
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRamsizeMB
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopArchitecture
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRemoteFX
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopAdapters
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7397ccc1afd350689ac1eeb984a62177140f50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384449"
---
# <a name="win32_rdmscollectionproperties-class"></a><span data-ttu-id="681c0-105">Win32 \_ RDMSCollectionProperties 類別</span><span class="sxs-lookup"><span data-stu-id="681c0-105">Win32\_RDMSCollectionProperties class</span></span>

<span data-ttu-id="681c0-106">管理虛擬桌面集合的屬性。</span><span class="sxs-lookup"><span data-stu-id="681c0-106">Manages the properties of a virtual desktop collection.</span></span>

<span data-ttu-id="681c0-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="681c0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="681c0-108">語法</span><span class="sxs-lookup"><span data-stu-id="681c0-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSCollectionProperties
{
  string  Alias;
  string  ReferenceVirtualDesktopName;
  string  ReferenceVirtualDesktopMachineName;
  string  ReferenceVirtualDesktopHost;
  string  ReferenceVirtualDesktopGuid;
  string  ReferenceVirtualDesktopOsversion;
  uint32  ReferenceVirtualDesktopRamsizeMB;
  string  ReferenceVirtualDesktopArchitecture;
  boolean ReferenceVirtualDesktopRemoteFX = false;
  string  ReferenceVirtualDesktopAdapters[];
};
```

## <a name="members"></a><span data-ttu-id="681c0-109">成員</span><span class="sxs-lookup"><span data-stu-id="681c0-109">Members</span></span>

<span data-ttu-id="681c0-110">**Win32 \_ RDMSCollectionProperties** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="681c0-110">The **Win32\_RDMSCollectionProperties** class has these types of members:</span></span>

-   [<span data-ttu-id="681c0-111">方法</span><span class="sxs-lookup"><span data-stu-id="681c0-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="681c0-112">屬性</span><span class="sxs-lookup"><span data-stu-id="681c0-112">Properties</span></span>](/windows)

### <a name="methods"></a><span data-ttu-id="681c0-113">方法</span><span class="sxs-lookup"><span data-stu-id="681c0-113">Methods</span></span>

<span data-ttu-id="681c0-114">**Win32 \_ RDMSCollectionProperties** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="681c0-114">The **Win32\_RDMSCollectionProperties** class has these methods.</span></span>



| <span data-ttu-id="681c0-115">方法</span><span class="sxs-lookup"><span data-stu-id="681c0-115">Method</span></span>                                                                                        | <span data-ttu-id="681c0-116">描述</span><span class="sxs-lookup"><span data-stu-id="681c0-116">Description</span></span>                                                                         |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="681c0-117">**GetProvisioningProperties**</span><span class="sxs-lookup"><span data-stu-id="681c0-117">**GetProvisioningProperties**</span></span>](getprovisioningproperties-win32-rdmscollectionproperties.md) | <span data-ttu-id="681c0-118">抓取虛擬桌面集合的布建屬性。</span><span class="sxs-lookup"><span data-stu-id="681c0-118">Retrieves the provisioning properties of the virtual desktop collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="681c0-119">屬性</span><span class="sxs-lookup"><span data-stu-id="681c0-119">Properties</span></span>

<span data-ttu-id="681c0-120">**Win32 \_ RDMSCollectionProperties** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="681c0-120">The **Win32\_RDMSCollectionProperties** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="681c0-121">**別名**</span><span class="sxs-lookup"><span data-stu-id="681c0-121">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="681c0-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="681c0-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="681c0-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="681c0-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="681c0-124">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="681c0-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="681c0-125">取得集合的別名。</span><span class="sxs-lookup"><span data-stu-id="681c0-125">Gets the alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="681c0-126">**ReferenceVirtualDesktopAdapters**</span><span class="sxs-lookup"><span data-stu-id="681c0-126">**ReferenceVirtualDesktopAdapters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="681c0-127">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="681c0-127">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="681c0-128">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="681c0-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="681c0-129">取得和設定主要 VM 的虛擬網路介面卡名稱。</span><span class="sxs-lookup"><span data-stu-id="681c0-129">Gets and sets the names of the virtual network adapters of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="681c0-130">**ReferenceVirtualDesktopArchitecture**</span><span class="sxs-lookup"><span data-stu-id="681c0-130">**ReferenceVirtualDesktopArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="681c0-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="681c0-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="681c0-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="681c0-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="681c0-133">取得和設定主要 VM 的處理器架構。</span><span class="sxs-lookup"><span data-stu-id="681c0-133">Gets and sets the processor architecture of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="681c0-134">**ReferenceVirtualDesktopGuid**</span><span class="sxs-lookup"><span data-stu-id="681c0-134">**ReferenceVirtualDesktopGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="681c0-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="681c0-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="681c0-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="681c0-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="681c0-137">取得和設定主要 VM 的 GUID。</span><span class="sxs-lookup"><span data-stu-id="681c0-137">Gets and sets the GUID of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="681c0-138">**ReferenceVirtualDesktopHost**</span><span class="sxs-lookup"><span data-stu-id="681c0-138">**ReferenceVirtualDesktopHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="681c0-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="681c0-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="681c0-140">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="681c0-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="681c0-141">取得和設定主要 VM 的主機伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="681c0-141">Gets and sets the host server name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="681c0-142">**ReferenceVirtualDesktopMachineName**</span><span class="sxs-lookup"><span data-stu-id="681c0-142">**ReferenceVirtualDesktopMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="681c0-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="681c0-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="681c0-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="681c0-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="681c0-145">取得和設定主要 VM 的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="681c0-145">Gets and sets the machine name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="681c0-146">**ReferenceVirtualDesktopName**</span><span class="sxs-lookup"><span data-stu-id="681c0-146">**ReferenceVirtualDesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="681c0-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="681c0-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="681c0-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="681c0-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="681c0-149">取得和設定主要 VM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="681c0-149">Gets and sets the name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="681c0-150">**ReferenceVirtualDesktopOsversion**</span><span class="sxs-lookup"><span data-stu-id="681c0-150">**ReferenceVirtualDesktopOsversion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="681c0-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="681c0-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="681c0-152">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="681c0-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="681c0-153">取得和設定主要 VM 的 OS 版本。</span><span class="sxs-lookup"><span data-stu-id="681c0-153">Gets and sets the OS version of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="681c0-154">**ReferenceVirtualDesktopRamsizeMB**</span><span class="sxs-lookup"><span data-stu-id="681c0-154">**ReferenceVirtualDesktopRamsizeMB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="681c0-155">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="681c0-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="681c0-156">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="681c0-156">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="681c0-157">取得和設定主要 VM 的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="681c0-157">Gets and sets the memory size of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="681c0-158">**ReferenceVirtualDesktopRemoteFX**</span><span class="sxs-lookup"><span data-stu-id="681c0-158">**ReferenceVirtualDesktopRemoteFX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="681c0-159">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="681c0-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="681c0-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="681c0-160">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="681c0-161">取得和設定值，這個值會指出是否已為主要 VM 啟用 RemoteFX。</span><span class="sxs-lookup"><span data-stu-id="681c0-161">Gets and sets a value that indicates whether RemoteFX is enabled for the master VM.</span></span> <span data-ttu-id="681c0-162">如果已啟用 RemoteFX，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="681c0-162">**TRUE** if RemoteFX is enabled; otherwise, **FALSE**.</span></span> <span data-ttu-id="681c0-163">這個屬性的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="681c0-163">The default value for this property is **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="681c0-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="681c0-164">Requirements</span></span>



| <span data-ttu-id="681c0-165">需求</span><span class="sxs-lookup"><span data-stu-id="681c0-165">Requirement</span></span> | <span data-ttu-id="681c0-166">值</span><span class="sxs-lookup"><span data-stu-id="681c0-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="681c0-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="681c0-167">Minimum supported client</span></span><br/> | <span data-ttu-id="681c0-168">都不支援</span><span class="sxs-lookup"><span data-stu-id="681c0-168">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="681c0-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="681c0-169">Minimum supported server</span></span><br/> | <span data-ttu-id="681c0-170">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="681c0-170">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="681c0-171">命名空間</span><span class="sxs-lookup"><span data-stu-id="681c0-171">Namespace</span></span><br/>                | <span data-ttu-id="681c0-172">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="681c0-172">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="681c0-173">MOF</span><span class="sxs-lookup"><span data-stu-id="681c0-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="681c0-174"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="681c0-174"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="681c0-175">DLL</span><span class="sxs-lookup"><span data-stu-id="681c0-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="681c0-176"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="681c0-176"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="681c0-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="681c0-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="681c0-178">遠端桌面管理服務提供者</span><span class="sxs-lookup"><span data-stu-id="681c0-178">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

