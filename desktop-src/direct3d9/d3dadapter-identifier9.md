---
description: 包含可識別介面卡的資訊。
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: 'D3DADAPTER_IDENTIFIER9 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DADAPTER_IDENTIFIER9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 85401573956d29386b5ddabbd48711a7be140463
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129967"
---
# <a name="d3dadapter_identifier9-structure"></a><span data-ttu-id="7f08d-103">D3DADAPTER \_ IDENTIFIER9 結構</span><span class="sxs-lookup"><span data-stu-id="7f08d-103">D3DADAPTER\_IDENTIFIER9 structure</span></span>

<span data-ttu-id="7f08d-104">包含可識別介面卡的資訊。</span><span class="sxs-lookup"><span data-stu-id="7f08d-104">Contains information identifying the adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f08d-105">語法</span><span class="sxs-lookup"><span data-stu-id="7f08d-105">Syntax</span></span>


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
#ifdef _WIN32
  LARGE_INTEGER DriverVersion;
#else
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
#endif
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a><span data-ttu-id="7f08d-106">成員</span><span class="sxs-lookup"><span data-stu-id="7f08d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f08d-107">**驅動程式**</span><span class="sxs-lookup"><span data-stu-id="7f08d-107">**Driver**</span></span>
</dt> <dd>

<span data-ttu-id="7f08d-108">類型： **char**</span><span class="sxs-lookup"><span data-stu-id="7f08d-108">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="7f08d-109">用於呈現給使用者。</span><span class="sxs-lookup"><span data-stu-id="7f08d-109">Used for presentation to the user.</span></span> <span data-ttu-id="7f08d-110">這不應該用來識別特定的驅動程式，因為許多不同的字串可能與來自不同廠商的相同裝置和驅動程式相關聯。</span><span class="sxs-lookup"><span data-stu-id="7f08d-110">This should not be used to identify particular drivers, because many different strings might be associated with the same device and driver from different vendors.</span></span>

</dd> <dt>

<span data-ttu-id="7f08d-111">**說明**</span><span class="sxs-lookup"><span data-stu-id="7f08d-111">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7f08d-112">類型： **char**</span><span class="sxs-lookup"><span data-stu-id="7f08d-112">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="7f08d-113">用於呈現給使用者。</span><span class="sxs-lookup"><span data-stu-id="7f08d-113">Used for presentation to the user.</span></span>

</dd> <dt>

<span data-ttu-id="7f08d-114">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="7f08d-114">**DeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="7f08d-115">類型： **char**</span><span class="sxs-lookup"><span data-stu-id="7f08d-115">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="7f08d-116">GDI 的裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="7f08d-116">Device name for GDI.</span></span>

</dd> <dt>

<span data-ttu-id="7f08d-117">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="7f08d-117">**DriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7f08d-118">類型： **[**大型 \_ 整數**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="7f08d-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="7f08d-119">識別 Direct3D 驅動程式的版本。</span><span class="sxs-lookup"><span data-stu-id="7f08d-119">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="7f08d-120">在64位帶正負號的整數值上進行小於和大於比較是合法的。</span><span class="sxs-lookup"><span data-stu-id="7f08d-120">It is legal to do less than and greater than comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="7f08d-121">但是，如果您使用此元素來識別有問題的驅動程式，請務必小心。</span><span class="sxs-lookup"><span data-stu-id="7f08d-121">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="7f08d-122">相反地，您應該使用 DeviceIdentifier。</span><span class="sxs-lookup"><span data-stu-id="7f08d-122">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="7f08d-123">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="7f08d-123">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7f08d-124">**DriverVersionLowPart**</span><span class="sxs-lookup"><span data-stu-id="7f08d-124">**DriverVersionLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="7f08d-125">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f08d-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f08d-126">識別 Direct3D 驅動程式的版本。</span><span class="sxs-lookup"><span data-stu-id="7f08d-126">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="7f08d-127">針對64位帶正負號的整數值進行 < 和 > 比較是合法的。</span><span class="sxs-lookup"><span data-stu-id="7f08d-127">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="7f08d-128">但是，如果您使用此元素來識別有問題的驅動程式，請務必小心。</span><span class="sxs-lookup"><span data-stu-id="7f08d-128">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="7f08d-129">相反地，您應該使用 DeviceIdentifier。</span><span class="sxs-lookup"><span data-stu-id="7f08d-129">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="7f08d-130">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="7f08d-130">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7f08d-131">**DriverVersionHighPart**</span><span class="sxs-lookup"><span data-stu-id="7f08d-131">**DriverVersionHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="7f08d-132">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f08d-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f08d-133">識別 Direct3D 驅動程式的版本。</span><span class="sxs-lookup"><span data-stu-id="7f08d-133">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="7f08d-134">針對64位帶正負號的整數值進行 < 和 > 比較是合法的。</span><span class="sxs-lookup"><span data-stu-id="7f08d-134">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="7f08d-135">但是，如果您使用此元素來識別有問題的驅動程式，請務必小心。</span><span class="sxs-lookup"><span data-stu-id="7f08d-135">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="7f08d-136">相反地，您應該使用 DeviceIdentifier。</span><span class="sxs-lookup"><span data-stu-id="7f08d-136">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="7f08d-137">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="7f08d-137">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7f08d-138">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="7f08d-138">**VendorId**</span></span>
</dt> <dd>

<span data-ttu-id="7f08d-139">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f08d-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f08d-140">可以用來協助識別特定晶片集。</span><span class="sxs-lookup"><span data-stu-id="7f08d-140">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="7f08d-141">查詢此成員以識別製造商。</span><span class="sxs-lookup"><span data-stu-id="7f08d-141">Query this member to identify the manufacturer.</span></span> <span data-ttu-id="7f08d-142">如果不明，此值可以是零。</span><span class="sxs-lookup"><span data-stu-id="7f08d-142">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="7f08d-143">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="7f08d-143">**DeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="7f08d-144">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f08d-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f08d-145">可以用來協助識別特定晶片集。</span><span class="sxs-lookup"><span data-stu-id="7f08d-145">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="7f08d-146">查詢此成員以識別晶片集的類型。</span><span class="sxs-lookup"><span data-stu-id="7f08d-146">Query this member to identify the type of chip set.</span></span> <span data-ttu-id="7f08d-147">如果不明，此值可以是零。</span><span class="sxs-lookup"><span data-stu-id="7f08d-147">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="7f08d-148">**SubSysId**</span><span class="sxs-lookup"><span data-stu-id="7f08d-148">**SubSysId**</span></span>
</dt> <dd>

<span data-ttu-id="7f08d-149">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f08d-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f08d-150">可以用來協助識別特定晶片集。</span><span class="sxs-lookup"><span data-stu-id="7f08d-150">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="7f08d-151">查詢此成員以識別子系統，通常是特定的面板。</span><span class="sxs-lookup"><span data-stu-id="7f08d-151">Query this member to identify the subsystem, typically the particular board.</span></span> <span data-ttu-id="7f08d-152">如果不明，此值可以是零。</span><span class="sxs-lookup"><span data-stu-id="7f08d-152">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="7f08d-153">**修訂**</span><span class="sxs-lookup"><span data-stu-id="7f08d-153">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="7f08d-154">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f08d-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f08d-155">可以用來協助識別特定晶片集。</span><span class="sxs-lookup"><span data-stu-id="7f08d-155">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="7f08d-156">查詢此成員以識別晶片集的修訂層級。</span><span class="sxs-lookup"><span data-stu-id="7f08d-156">Query this member to identify the revision level of the chip set.</span></span> <span data-ttu-id="7f08d-157">如果不明，此值可以是零。</span><span class="sxs-lookup"><span data-stu-id="7f08d-157">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="7f08d-158">**DeviceIdentifier**</span><span class="sxs-lookup"><span data-stu-id="7f08d-158">**DeviceIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="7f08d-159">類型： **[ **GUID**](guid.md)**</span><span class="sxs-lookup"><span data-stu-id="7f08d-159">Type: **[**GUID**](guid.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f08d-160">可以查詢以檢查驅動程式和晶片集的變更。</span><span class="sxs-lookup"><span data-stu-id="7f08d-160">Can be queried to check changes in the driver and chip set.</span></span> <span data-ttu-id="7f08d-161">此 GUID 是驅動程式和晶片集配對的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="7f08d-161">This GUID is a unique identifier for the driver and chip set pair.</span></span> <span data-ttu-id="7f08d-162">查詢此成員以追蹤驅動程式和晶片集的變更，以便為圖形子系統產生新的設定檔。</span><span class="sxs-lookup"><span data-stu-id="7f08d-162">Query this member to track changes to the driver and chip set in order to generate a new profile for the graphics subsystem.</span></span> <span data-ttu-id="7f08d-163">DeviceIdentifier 也可用來識別特定有問題的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="7f08d-163">DeviceIdentifier can also be used to identify particular problematic drivers.</span></span>

</dd> <dt>

<span data-ttu-id="7f08d-164">**WHQLLevel**</span><span class="sxs-lookup"><span data-stu-id="7f08d-164">**WHQLLevel**</span></span>
</dt> <dd>

<span data-ttu-id="7f08d-165">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f08d-165">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f08d-166">用來判斷此驅動程式和裝置配對的 Windows 硬體品質實驗室 (WHQL) 驗證等級。</span><span class="sxs-lookup"><span data-stu-id="7f08d-166">Used to determine the Windows Hardware Quality Labs (WHQL) validation level for this driver and device pair.</span></span> <span data-ttu-id="7f08d-167">DWORD 是一種封裝日期結構，用來定義由驅動程式傳遞的最新 WHQL 測試的發行日期。</span><span class="sxs-lookup"><span data-stu-id="7f08d-167">The DWORD is a packed date structure defining the date of the release of the most recent WHQL test passed by the driver.</span></span> <span data-ttu-id="7f08d-168">對此值執行 < 和 > 作業是合法的。</span><span class="sxs-lookup"><span data-stu-id="7f08d-168">It is legal to perform < and > operations on this value.</span></span> <span data-ttu-id="7f08d-169">以下說明日期格式。</span><span class="sxs-lookup"><span data-stu-id="7f08d-169">The following illustrates the date format.</span></span>



| <span data-ttu-id="7f08d-170">Bits</span><span class="sxs-lookup"><span data-stu-id="7f08d-170">Bits</span></span>  |  <span data-ttu-id="7f08d-171">描述</span><span class="sxs-lookup"><span data-stu-id="7f08d-171">Description</span></span>                                             |
|-------|-----------------------------------------------|
| <span data-ttu-id="7f08d-172">31-16</span><span class="sxs-lookup"><span data-stu-id="7f08d-172">31-16</span></span> | <span data-ttu-id="7f08d-173">年份，從1999向上的十進位數。</span><span class="sxs-lookup"><span data-stu-id="7f08d-173">The year, a decimal number from 1999 upwards.</span></span> |
| <span data-ttu-id="7f08d-174">15-8</span><span class="sxs-lookup"><span data-stu-id="7f08d-174">15-8</span></span>  | <span data-ttu-id="7f08d-175">月份，介於1到12之間的十進位數。</span><span class="sxs-lookup"><span data-stu-id="7f08d-175">The month, a decimal number from 1 to 12.</span></span>     |
| <span data-ttu-id="7f08d-176">7-0</span><span class="sxs-lookup"><span data-stu-id="7f08d-176">7-0</span></span>   | <span data-ttu-id="7f08d-177">Day，介於1到31之間的十進位數。</span><span class="sxs-lookup"><span data-stu-id="7f08d-177">The day, a decimal number from 1 to 31.</span></span>       |



 

<span data-ttu-id="7f08d-178">也會使用下列值。</span><span class="sxs-lookup"><span data-stu-id="7f08d-178">The following values are also used.</span></span>



| <span data-ttu-id="7f08d-179">值</span><span class="sxs-lookup"><span data-stu-id="7f08d-179">Value</span></span>    |  <span data-ttu-id="7f08d-180">描述</span><span class="sxs-lookup"><span data-stu-id="7f08d-180">Description</span></span>                                                     |
|-----|-------------------------------------------------------|
| <span data-ttu-id="7f08d-181">0</span><span class="sxs-lookup"><span data-stu-id="7f08d-181">0</span></span>   | <span data-ttu-id="7f08d-182">未通過認證。</span><span class="sxs-lookup"><span data-stu-id="7f08d-182">Not certified.</span></span>                                        |
| <span data-ttu-id="7f08d-183">1</span><span class="sxs-lookup"><span data-stu-id="7f08d-183">1</span></span>   | <span data-ttu-id="7f08d-184">經 WHQL 驗證，但沒有可用的日期資訊。</span><span class="sxs-lookup"><span data-stu-id="7f08d-184">WHQL validated, but no date information is available.</span></span> |



 

<span data-ttu-id="7f08d-185">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="7f08d-185">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

<span data-ttu-id="7f08d-186">如果是在 Windows Vista、Windows Server 2008、Windows 7 和 Windows Server 2008 R2 上執行的 Direct3D9Ex (或更多目前的作業系統) ， [**IDirect3D9：： GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) 會為 WHQL 層級傳回1，而不會檢查驅動程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="7f08d-186">For Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) returns 1 for the WHQL level without checking the status of the driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f08d-187">備註</span><span class="sxs-lookup"><span data-stu-id="7f08d-187">Remarks</span></span>

<span data-ttu-id="7f08d-188">下列虛擬虛擬的範例說明在 DriverVersion、DriverVersionLowPart 和 DriverVersionHighPart 成員中編碼的版本格式。</span><span class="sxs-lookup"><span data-stu-id="7f08d-188">The following pseudocode example illustrates the version format encoded in the DriverVersion, DriverVersionLowPart, and DriverVersionHighPart members.</span></span>


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



<span data-ttu-id="7f08d-189">如需 HIWORD 宏、LOWORD 宏和大型整數結構的詳細資訊，請參閱 Platform SDK \_ 。</span><span class="sxs-lookup"><span data-stu-id="7f08d-189">See the Platform SDK for more information about the HIWORD macro, the LOWORD macro, and the LARGE\_INTEGER structure.</span></span>

<span data-ttu-id="7f08d-190">\_裝置 \_ 識別碼字串上限 \_ 是具有下列定義的常數。</span><span class="sxs-lookup"><span data-stu-id="7f08d-190">MAX\_DEVICE\_IDENTIFIER\_STRING is a constant with the following definition.</span></span>


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



<span data-ttu-id="7f08d-191">VendorId、DeviceId、SubSysId 和修訂成員可以串聯使用，以識別特定晶片集。</span><span class="sxs-lookup"><span data-stu-id="7f08d-191">The VendorId, DeviceId, SubSysId, and Revision members can be used in tandem to identify particular chip sets.</span></span> <span data-ttu-id="7f08d-192">不過，請小心使用這些成員。</span><span class="sxs-lookup"><span data-stu-id="7f08d-192">However, use these members with caution.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f08d-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f08d-193">Requirements</span></span>



| <span data-ttu-id="7f08d-194">需求</span><span class="sxs-lookup"><span data-stu-id="7f08d-194">Requirement</span></span> | <span data-ttu-id="7f08d-195">值</span><span class="sxs-lookup"><span data-stu-id="7f08d-195">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f08d-196">標頭</span><span class="sxs-lookup"><span data-stu-id="7f08d-196">Header</span></span><br/> | <dl> <span data-ttu-id="7f08d-197"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f08d-197"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f08d-198">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f08d-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f08d-199">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="7f08d-199">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
