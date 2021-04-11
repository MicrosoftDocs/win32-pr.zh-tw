---
title: 'IADsComputer 屬性方法 (Iads .h) '
description: IADsComputer 介面方法會讀取及寫入本主題中所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: c990b6bb-6256-4216-9435-c85c67db4d13
ms.tgt_platform: multiple
keywords:
- IADsComputer 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsComputer Property Methods
- IADsComputer.ComputerID
- IADsComputer.get_ComputerID
- IADsComputer.Department
- IADsComputer.get_Department
- IADsComputer.put_Department
- IADsComputer.Description
- IADsComputer.get_Description
- IADsComputer.put_Description
- IADsComputer.Division
- IADsComputer.get_Division
- IADsComputer.put_Division
- IADsComputer.Location
- IADsComputer.get_Location
- IADsComputer.put_Location
- IADsComputer.MemorySize
- IADsComputer.get_MemorySize
- IADsComputer.put_MemorySize
- IADsComputer.Model
- IADsComputer.get_Model
- IADsComputer.put_Model
- IADsComputer.NetAddresses
- IADsComputer.get_NetAddresses
- IADsComputer.put_NetAddresses
- IADsComputer.OperatingSystem
- IADsComputer.get_OperatingSystem
- IADsComputer.put_OperatingSystem
- IADsComputer.OperatingSystemVersion
- IADsComputer.get_OperatingSystemVersion
- IADsComputer.put_OperatingSystemVersion
- IADsComputer.Owner
- IADsComputer.get_Owner
- IADsComputer.put_Owner
- IADsComputer.PrimaryUser
- IADsComputer.get_PrimaryUser
- IADsComputer.put_PrimaryUser
- IADsComputer.Processor
- IADsComputer.get_Processor
- IADsComputer.put_Processor
- IADsComputer.ProcessorCount
- IADsComputer.get_ProcessorCount
- IADsComputer.put_ProcessorCount
- IADsComputer.Role
- IADsComputer.get_Role
- IADsComputer.put_Role
- IADsComputer.Site
- IADsComputer.get_Site
- IADsComputer.StorageCapacity
- IADsComputer.get_StorageCapacity
- IADsComputer.put_StorageCapacity
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2f3c455e2e43436627b62d142781bb6a605bef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844016"
---
# <a name="iadscomputer-property-methods"></a><span data-ttu-id="ae2ae-105">IADsComputer 屬性方法</span><span class="sxs-lookup"><span data-stu-id="ae2ae-105">IADsComputer Property Methods</span></span>

<span data-ttu-id="ae2ae-106">[**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)介面方法會讀取及寫入本主題中所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-106">The [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) interface methods read and write the properties described in this topic.</span></span> <span data-ttu-id="ae2ae-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ae2ae-108">屬性</span><span class="sxs-lookup"><span data-stu-id="ae2ae-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="ae2ae-109">**ComputerID**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-109">**ComputerID**</span></span>
<span data-ttu-id="ae2ae-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-111">指派給每部電腦的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-111">The globally unique identifier assigned to each computer.</span></span>

<dt>

<span data-ttu-id="ae2ae-112">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ae2ae-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-113">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerID(
  [out] BSTR* pbstrComputerID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-114">**部門**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-114">**Department**</span></span>
<span data-ttu-id="ae2ae-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-116">組織單位 (此電腦所屬的 OU) ，例如部門。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-116">The organizational unit (OU), such as department, that this computer belongs to.</span></span>

<dt>

<span data-ttu-id="ae2ae-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ae2ae-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Department(
  [out] BSTR* pbstrDepartment
);
HRESULT put_Department(
  [in] BSTR bstrDepartment
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-119">**說明**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-119">**Description**</span></span>
<span data-ttu-id="ae2ae-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-121">此電腦的描述。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-121">The description of this computer.</span></span>

<dt>

<span data-ttu-id="ae2ae-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ae2ae-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-123">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-124">**部門**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-124">**Division**</span></span>
<span data-ttu-id="ae2ae-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-126">此電腦所屬組織內的部門。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-126">The division, within an organization, that this computer belongs to.</span></span>

<dt>

<span data-ttu-id="ae2ae-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ae2ae-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-128">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Division(
  [out] BSTR* pbstrDivision
);
HRESULT put_Division(
  [in] BSTR bstrDivision
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-129">**位置**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-129">**Location**</span></span>
<span data-ttu-id="ae2ae-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-131">此電腦已指派的實體位置。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-131">The assigned physical location of this computer.</span></span>

<dt>

<span data-ttu-id="ae2ae-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ae2ae-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-133">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-134">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-134">**MemorySize**</span></span>
<span data-ttu-id="ae2ae-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-136">此電腦的隨機存取記憶體大小（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-136">The size, in megabytes, of random access memory for this computer.</span></span>

<dt>

<span data-ttu-id="ae2ae-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ae2ae-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-138">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MemorySize(
  [out] BSTR* pbstrMemorySize
);
HRESULT put_MemorySize(
  [in] BSTR bstrMemorySize
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-139">**型號**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-139">**Model**</span></span>
<span data-ttu-id="ae2ae-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-141">此電腦的製作和模型。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-141">The make and model of this computer.</span></span>

<dt>

<span data-ttu-id="ae2ae-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ae2ae-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-143">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-144">**NetAddresses**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-144">**NetAddresses**</span></span>
<span data-ttu-id="ae2ae-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-146">NetAddress 欄位的陣列，代表可達到此電腦的位址。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-146">An array of NetAddress fields that represent the addresses by which this computer can be reached.</span></span> <span data-ttu-id="ae2ae-147">NetAddress 是由兩個以冒號分隔的子字串所組成的提供者特定 **BSTR** (： ) 。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-147">NetAddress is a provider-specific **BSTR** composed of two substrings separated by a colon (:).</span></span> <span data-ttu-id="ae2ae-148">左邊的子字串表示網址類別型，右邊的子字串則是該類型位址的字串表示。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-148">The left substring indicates the address type, and the right substring is a string representation of an address of that type.</span></span> <span data-ttu-id="ae2ae-149">例如，TCP/IP 位址的格式如下： IP：100.201.301.45。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-149">For example, TCP/IP addresses are of the form: IP:100.201.301.45.</span></span> <span data-ttu-id="ae2ae-150">IPX 類型位址的格式為： IPX：10.123456.80。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-150">IPX type addresses are of the form: IPX:10.123456.80.</span></span>

<dt>

<span data-ttu-id="ae2ae-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ae2ae-151">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-152">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-152">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NetAddresses(
  [out] VARIANT* pvNetAddresses
);
HRESULT put_NetAddresses(
  [in] VARIANT vNetAddresses
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-153">**OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-153">**OperatingSystem**</span></span>
<span data-ttu-id="ae2ae-154"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-154"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-155">在這部電腦上使用的作業系統。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-155">The operating system used on this computer.</span></span>

<dt>

<span data-ttu-id="ae2ae-156">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ae2ae-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-157">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-157">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystem(
  [out] BSTR* pbstrOperatingSystem
);
HRESULT put_OperatingSystem(
  [in] BSTR bstrOperatingSystem
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-158">**OperatingSystemVersion**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-158">**OperatingSystemVersion**</span></span>
<span data-ttu-id="ae2ae-159"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-159"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-160">此電腦所使用的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-160">The version of the operating system used on this computer.</span></span>

<dt>

<span data-ttu-id="ae2ae-161">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ae2ae-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-162">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-162">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystemVersion(
  [out] BSTR* pbstrOperatingSystemVersion
);
HRESULT put_OperatingSystemVersion(
  [in] BSTR bstrOperatingSystemVersion
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-163">**擁有者**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-163">**Owner**</span></span>
<span data-ttu-id="ae2ae-164"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-164"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-165">指派這部電腦的人員。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-165">The person to whom this computer is assigned.</span></span> <span data-ttu-id="ae2ae-166">此人員也應該擁有執行已安裝軟體的授權。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-166">This person should also have a license to run the installed software.</span></span>

<dt>

<span data-ttu-id="ae2ae-167">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ae2ae-167">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-168">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-168">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwner
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-169">**PrimaryUser**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-169">**PrimaryUser**</span></span>
<span data-ttu-id="ae2ae-170"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-170"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-171">此電腦的連絡人人員名稱，例如系統管理員。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-171">The name of the contact person, such as an administrator, for this computer.</span></span>

<dt>

<span data-ttu-id="ae2ae-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ae2ae-172">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-173">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-173">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryUser(
  [out] BSTR* pbstrPrimaryUser
);
HRESULT put_PrimaryUser(
  [in] BSTR bstrPrimaryUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-174">**處理器**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-174">**Processor**</span></span>
<span data-ttu-id="ae2ae-175"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-175"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-176">處理器類型。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-176">The processor type.</span></span>

<dt>

<span data-ttu-id="ae2ae-177">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ae2ae-177">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-178">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-178">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Processor(
  [out] BSTR* pbstrProcessor
);
HRESULT put_Processor(
  [in] BSTR bstrProcessor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-179">**ProcessorCount**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-179">**ProcessorCount**</span></span>
<span data-ttu-id="ae2ae-180"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-180"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-181">已安裝的處理器數目。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-181">The number of installed processors.</span></span>

<dt>

<span data-ttu-id="ae2ae-182">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ae2ae-182">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-183">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-183">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProcessorCount(
  [out] BSTR* pbstrProcessorCount
);
HRESULT put_ProcessorCount(
  [in] BSTR bstrProcessorCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-184">**角色**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-184">**Role**</span></span>
<span data-ttu-id="ae2ae-185"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-185"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-186">這部電腦的角色，例如工作站、伺服器或網域控制站。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-186">The role of this computer, for example, workstation, server, or domain controller.</span></span>

<dt>

<span data-ttu-id="ae2ae-187">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ae2ae-187">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-188">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-188">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Role(
  [out] BSTR* pbstrRole
);
HRESULT put_Role(
  [in] BSTR bstrRole
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-189">**站台**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-189">**Site**</span></span>
<span data-ttu-id="ae2ae-190"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-190"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-191">全域唯一識別碼，識別這部電腦安裝所在的網站。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-191">The globally unique identifier that identifies the site that this computer was installed in.</span></span> <span data-ttu-id="ae2ae-192">網站是網路中良好連線能力的實體區域。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-192">A site is a physical region of good connectivity in a network.</span></span>

<dt>

<span data-ttu-id="ae2ae-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ae2ae-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-194">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-194">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Site(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ae-195">**StorageCapacity**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-195">**StorageCapacity**</span></span>
<span data-ttu-id="ae2ae-196"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ae2ae-196"></dt> <dd> <dl></span></span>

<span data-ttu-id="ae2ae-197">磁片的大小（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-197">The size, in megabytes, of the disk.</span></span>

<dt>

<span data-ttu-id="ae2ae-198">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ae2ae-198">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ae2ae-199">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-199">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StorageCapacity(
  [out] BSTR* pbstrStorageCapacity
);
HRESULT put_StorageCapacity(
  [in] BSTR bstrStorageCapacity
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="ae2ae-200">備註</span><span class="sxs-lookup"><span data-stu-id="ae2ae-200">Remarks</span></span>

<span data-ttu-id="ae2ae-201">不同的提供者可能會選擇公開電腦物件的不同屬性。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-201">Different providers may choose to expose different properties of a computer object.</span></span> <span data-ttu-id="ae2ae-202">如需詳細資訊，請參閱 [ADSI 系統提供者](adsi-system-providers.md)。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-202">For more information, see [ADSI System Providers](adsi-system-providers.md).</span></span>

<span data-ttu-id="ae2ae-203">您可以透過其架構類別檢查強制和選擇性屬性，以探索支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-203">You can discover what properties are supported by inspecting the mandatory and optional properties through its schema class.</span></span> <span data-ttu-id="ae2ae-204">如需詳細資訊，請參閱 [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) 介面。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-204">For more information, see the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface.</span></span>

<span data-ttu-id="ae2ae-205">若要檢查電腦的狀態，或在網路上執行關機操作，您必須使用 [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) 介面。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-205">To examine the status of a computer or to perform the shutdown operation across the network, you must use the [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="ae2ae-206">範例</span><span class="sxs-lookup"><span data-stu-id="ae2ae-206">Examples</span></span>

<span data-ttu-id="ae2ae-207">下列 Visual Basic 程式碼範例會檢查 ADSI WinNT 提供者所支援的電腦屬性。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-207">The following Visual Basic code example examines computer properties supported by the ADSI WinNT provider.</span></span>


```VB
Dim obj As IADs
On Error Resume Next

Set obj = GetObject("WinNT://myMachine,computer")
If (obj.Class = "Computer") Then
    MsgBox "Computer owner: " & obj.owner
    MsgBox "Computer division: " & obj.Division
    MsgBox "Computer operatingSystem: " & obj.OperatingSystem
    MsgBox "Computer operating System Version: " & obj.OperatingSystemVersion
    MsgBox "Computer processor: " & obj.Processor
    MsgBox "Computer processor Count: " & obj.ProcessorCount
End If
```



<span data-ttu-id="ae2ae-208">下列 c + + 程式碼範例會檢查 ADSI WinNT 提供者所支援的電腦屬性。</span><span class="sxs-lookup"><span data-stu-id="ae2ae-208">The following C++ code example examines computer properties supported by the ADSI WinNT provider.</span></span>


```C++
IADsComputer *pComp = NULL;
LPWSTR adspath = L"WinNT://jeffsmith1,computer";
HRESULT hr = S_OK;
BSTR bstr = NULL;

hr = ADsGetObject(adspath,IID_IADsComputer,(void**)&pComp);
if(FAILED(hr)) {goto Cleanup;}

hr = pComp->get_Owner(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Computer owner: %S\n",bstr);
SysFreeString(bstr);

hr = pComp->get_OperatingSystem(&bstr);
if(FAILED(hr)) {goto Cleanup;}
printf("Operating System: %S\n",bstr);
SysFreeString(bstr);

Cleanup:
    if(pComp) pComp->Release();
    if(bstr) SysFreeString(bstr);
    return hr;
```



## <a name="requirements"></a><span data-ttu-id="ae2ae-209">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae2ae-209">Requirements</span></span>



| <span data-ttu-id="ae2ae-210">需求</span><span class="sxs-lookup"><span data-stu-id="ae2ae-210">Requirement</span></span> | <span data-ttu-id="ae2ae-211">值</span><span class="sxs-lookup"><span data-stu-id="ae2ae-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2ae-212">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae2ae-212">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2ae-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae2ae-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae2ae-214">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae2ae-214">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2ae-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae2ae-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae2ae-216">標頭</span><span class="sxs-lookup"><span data-stu-id="ae2ae-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae2ae-217"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ae-217"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="ae2ae-218">DLL</span><span class="sxs-lookup"><span data-stu-id="ae2ae-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae2ae-219"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ae-219"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="ae2ae-220">IID</span><span class="sxs-lookup"><span data-stu-id="ae2ae-220">IID</span></span><br/>                      | <span data-ttu-id="ae2ae-221">IID \_ IADsComputer 定義為 EFE3CC70-1D9F-11CF-B1F3-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="ae2ae-221">IID\_IADsComputer is defined as EFE3CC70-1D9F-11CF-B1F3-02608C9E7553</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="ae2ae-222">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae2ae-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2ae-223">**IADsComputer**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-223">**IADsComputer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscomputer)
</dt> <dt>

[<span data-ttu-id="ae2ae-224">ADSI 系統提供者</span><span class="sxs-lookup"><span data-stu-id="ae2ae-224">ADSI System Providers</span></span>](adsi-system-providers.md)
</dt> <dt>

[<span data-ttu-id="ae2ae-225">**得到 iadsclass**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-225">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="ae2ae-226">**IADsComputerOperations**</span><span class="sxs-lookup"><span data-stu-id="ae2ae-226">**IADsComputerOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)
</dt> <dt>

[<span data-ttu-id="ae2ae-227">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="ae2ae-227">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





