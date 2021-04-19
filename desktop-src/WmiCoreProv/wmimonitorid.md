---
description: 代表影片監視器的識別資訊，例如製造商名稱、製造年份或序號。
ms.assetid: 85c8c4b1-20e2-4c0b-9209-a3724509a2f0
title: WmiMonitorID 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorID
- WmiMonitorID.Active
- WmiMonitorID.InstanceName
- WmiMonitorID.ManufacturerName
- WmiMonitorID.ManufacturerNameLength
- WmiMonitorID.ProductCodeID
- WmiMonitorID.SerialNumberID
- WmiMonitorID.WeekOfManufacture
- WmiMonitorID.YearOfManufacture
- WmiMonitorID.UserFriendlyName
- WmiMonitorID.UserFriendlyNameLength
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.custom: project-verbatim
ms.openlocfilehash: 485b42a86ca67d15ec00be13992c17b31ed51608
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "106984282"
---
# <a name="wmimonitorid-class"></a><span data-ttu-id="66d65-103">WmiMonitorID 類別</span><span class="sxs-lookup"><span data-stu-id="66d65-103">WmiMonitorID class</span></span>

<span data-ttu-id="66d65-104">**WmiMonitorID** WMI 類別代表影片監視器的識別資訊，例如製造商名稱、製造年份或序號。</span><span class="sxs-lookup"><span data-stu-id="66d65-104">The **WmiMonitorID** WMI class represents the identifying information about a video monitor, such as manufacturer name, year of manufacture, or serial number.</span></span> <span data-ttu-id="66d65-105">此類別中的資料會對應至視頻電子產品標準關聯之影片輸入定義的廠商/產品識別區塊中的資料 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 標準。</span><span class="sxs-lookup"><span data-stu-id="66d65-105">The data in this class correspond to data in the Vendor/Product Identification block of Video Input Definition of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="66d65-106">語法</span><span class="sxs-lookup"><span data-stu-id="66d65-106">Syntax</span></span>

``` syntax
class WmiMonitorID : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint16  ManufacturerName[];
  uint16  ManufacturerNameLength;
  uint16  ProductCodeID[];
  uint16  SerialNumberID[];
  uint8   WeekOfManufacture;
  uint16  YearOfManufacture;
  uint16  UserFriendlyName[];
  uint16  UserFriendlyNameLength;
};
```

## <a name="members"></a><span data-ttu-id="66d65-107">成員</span><span class="sxs-lookup"><span data-stu-id="66d65-107">Members</span></span>

<span data-ttu-id="66d65-108">**WmiMonitorID** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="66d65-108">The **WmiMonitorID** class has these types of members:</span></span>

-   [<span data-ttu-id="66d65-109">屬性</span><span class="sxs-lookup"><span data-stu-id="66d65-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66d65-110">屬性</span><span class="sxs-lookup"><span data-stu-id="66d65-110">Properties</span></span>

<span data-ttu-id="66d65-111">**WmiMonitorID** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="66d65-111">The **WmiMonitorID** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66d65-112">**使用中**</span><span class="sxs-lookup"><span data-stu-id="66d65-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66d65-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="66d65-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66d65-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="66d65-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66d65-115">表示使用中的監視器。</span><span class="sxs-lookup"><span data-stu-id="66d65-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="66d65-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="66d65-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66d65-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="66d65-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66d65-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="66d65-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66d65-119">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="66d65-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="66d65-120">特定監視實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="66d65-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="66d65-121">**ManufacturerName**</span><span class="sxs-lookup"><span data-stu-id="66d65-121">**ManufacturerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66d65-122">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="66d65-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="66d65-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="66d65-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66d65-124">製造商的名稱。</span><span class="sxs-lookup"><span data-stu-id="66d65-124">Name of manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="66d65-125">**ManufacturerNameLength**</span><span class="sxs-lookup"><span data-stu-id="66d65-125">**ManufacturerNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66d65-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="66d65-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66d65-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="66d65-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66d65-128">位於 **ManufacturerName** 屬性中的製造商名稱長度。</span><span class="sxs-lookup"><span data-stu-id="66d65-128">Length of manufacturer name located in the **ManufacturerName** property.</span></span>

</dd> <dt>

<span data-ttu-id="66d65-129">**ProductCodeID**</span><span class="sxs-lookup"><span data-stu-id="66d65-129">**ProductCodeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66d65-130">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="66d65-130">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="66d65-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="66d65-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66d65-132">廠商指派的產品代碼識別碼。</span><span class="sxs-lookup"><span data-stu-id="66d65-132">Vendor assigned product code ID.</span></span>

</dd> <dt>

<span data-ttu-id="66d65-133">**SerialNumberID**</span><span class="sxs-lookup"><span data-stu-id="66d65-133">**SerialNumberID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66d65-134">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="66d65-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="66d65-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="66d65-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66d65-136">序號。</span><span class="sxs-lookup"><span data-stu-id="66d65-136">Serial number.</span></span>

</dd> <dt>

<span data-ttu-id="66d65-137">UserFriendlyName</span><span class="sxs-lookup"><span data-stu-id="66d65-137">UserFriendlyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66d65-138">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="66d65-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="66d65-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="66d65-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66d65-140">監視器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="66d65-140">The friendly name of the monitor.</span></span> <span data-ttu-id="66d65-141">名稱的大小是由 UserFriendlyNameLength 屬性所指定的長度。</span><span class="sxs-lookup"><span data-stu-id="66d65-141">The size of the name is the length specified by the UserFriendlyNameLength property.</span></span>

</dd> <dt>

<span data-ttu-id="66d65-142">UserFriendlyNameLength</span><span class="sxs-lookup"><span data-stu-id="66d65-142">UserFriendlyNameLength</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66d65-143">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="66d65-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66d65-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="66d65-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66d65-145">名稱位於 UserFriendlyName 屬性中的字元數。</span><span class="sxs-lookup"><span data-stu-id="66d65-145">Number of characters in the name located in the UserFriendlyName property.</span></span>

</dd> <dt>

<span data-ttu-id="66d65-146">**WeekOfManufacture**</span><span class="sxs-lookup"><span data-stu-id="66d65-146">**WeekOfManufacture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66d65-147">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="66d65-147">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="66d65-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="66d65-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66d65-149">依周數的製造周數。</span><span class="sxs-lookup"><span data-stu-id="66d65-149">Week of manufacture by week number.</span></span> <span data-ttu-id="66d65-150">範圍是從1到53。</span><span class="sxs-lookup"><span data-stu-id="66d65-150">The range is from 1 through 53.</span></span> <span data-ttu-id="66d65-151">未定義零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="66d65-151">Zero (0) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="66d65-152">**YearOfManufacture**</span><span class="sxs-lookup"><span data-stu-id="66d65-152">**YearOfManufacture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66d65-153">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="66d65-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66d65-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="66d65-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66d65-155">製造的年。</span><span class="sxs-lookup"><span data-stu-id="66d65-155">Year of manufacture.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66d65-156">備註</span><span class="sxs-lookup"><span data-stu-id="66d65-156">Remarks</span></span>

<span data-ttu-id="66d65-157">如需如何轉譯儲存序號識別碼之陣列的討論，請參閱設定管理員 blog 文章中的 [報告監視器資訊](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) 。</span><span class="sxs-lookup"><span data-stu-id="66d65-157">For a discussion on how to translate the arrays that store serial number ID's, see the [Reporting Monitor information with Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) blog article.</span></span>

## <a name="examples"></a><span data-ttu-id="66d65-158">範例</span><span class="sxs-lookup"><span data-stu-id="66d65-158">Examples</span></span>

<span data-ttu-id="66d65-159">下列 PowerShell 範例會取出多個監視的序號。</span><span class="sxs-lookup"><span data-stu-id="66d65-159">The following PowerShell example retrieves the serial number of multiple monitors.</span></span>


```PowerShell
gwmi WmiMonitorID -Namespace root\wmi | ForEach-Object {($_.UserFriendlyName -ne 0 | foreach {[char]$_}) -join ""; ($_.SerialNumberID -ne 0 | foreach {[char]$_}) -join ""}
```



<span data-ttu-id="66d65-160">下列 VBScript 程式碼也會從系統中取出監視器識別碼資訊。</span><span class="sxs-lookup"><span data-stu-id="66d65-160">The following VBScript code also retrieves monitor ID information from a system.</span></span>


```VB
Option Explicit

Dim strComputer, objWMIService, colItems, objItem

strComputer = "MyComputer"

Set objWMIService = GetObject("winmgmts:" _ 
  & "{impersonationLevel=impersonate,authenticationLevel=Pkt}!\\" _ 
  & strComputer & "\root\wmi") 

Set colItems = objWMIService.ExecQuery _
  ("SELECT * FROM WMIMonitorID")

For Each objItem In colItems
  Wscript.Echo objItem.InstanceName
Next
```



## <a name="requirements"></a><span data-ttu-id="66d65-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="66d65-161">Requirements</span></span>



| <span data-ttu-id="66d65-162">需求</span><span class="sxs-lookup"><span data-stu-id="66d65-162">Requirement</span></span> | <span data-ttu-id="66d65-163">值</span><span class="sxs-lookup"><span data-stu-id="66d65-163">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66d65-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66d65-164">Minimum supported client</span></span><br/> | <span data-ttu-id="66d65-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66d65-165">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="66d65-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66d65-166">Minimum supported server</span></span><br/> | <span data-ttu-id="66d65-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66d65-167">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="66d65-168">命名空間</span><span class="sxs-lookup"><span data-stu-id="66d65-168">Namespace</span></span><br/>                | <span data-ttu-id="66d65-169">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="66d65-169">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="66d65-170">MOF</span><span class="sxs-lookup"><span data-stu-id="66d65-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66d65-171"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="66d65-171"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="66d65-172">DLL</span><span class="sxs-lookup"><span data-stu-id="66d65-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66d65-173"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66d65-173"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66d65-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66d65-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d65-175">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="66d65-175">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

