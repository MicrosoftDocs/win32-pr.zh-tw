---
title: Win32_TSDeploymentLicensing 類別
description: 遠端桌面虛擬化 (RDV) 部署的授權設定。
ms.assetid: 78e95629-6580-4aa1-bcbd-a79af44ddb54
ms.tgt_platform: multiple
keywords:
- Win32_TSDeploymentLicensing 類別遠端桌面服務
- Win32_TSDeploymentLicensing 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSDeploymentLicensing
- Win32_TSDeploymentLicensing.Caption
- Win32_TSDeploymentLicensing.Description
- Win32_TSDeploymentLicensing.InstallDate
- Win32_TSDeploymentLicensing.Name
- Win32_TSDeploymentLicensing.Status
- Win32_TSDeploymentLicensing.UseCentralLicensingSettings
- Win32_TSDeploymentLicensing.LicenseServers
- Win32_TSDeploymentLicensing.LicensingType
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 952f58daa8a809e158265aac71b0094c0cd46fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970449"
---
# <a name="win32_tsdeploymentlicensing-class"></a><span data-ttu-id="01f5c-105">Win32 \_ TSDeploymentLicensing 類別</span><span class="sxs-lookup"><span data-stu-id="01f5c-105">Win32\_TSDeploymentLicensing class</span></span>

<span data-ttu-id="01f5c-106">遠端桌面虛擬化 (RDV) 部署的授權設定。</span><span class="sxs-lookup"><span data-stu-id="01f5c-106">Licensing Settings for the Remote Desktop Virtualization (RDV) deployment.</span></span>

<span data-ttu-id="01f5c-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="01f5c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="01f5c-108">語法</span><span class="sxs-lookup"><span data-stu-id="01f5c-108">Syntax</span></span>

``` syntax
class Win32_TSDeploymentLicensing : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  UseCentralLicensingSettings;
  String   LicenseServers[];
  uint32   LicensingType;
};
```

## <a name="members"></a><span data-ttu-id="01f5c-109">成員</span><span class="sxs-lookup"><span data-stu-id="01f5c-109">Members</span></span>

<span data-ttu-id="01f5c-110">**Win32 \_ TSDeploymentLicensing** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="01f5c-110">The **Win32\_TSDeploymentLicensing** class has these types of members:</span></span>

-   [<span data-ttu-id="01f5c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="01f5c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01f5c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="01f5c-112">Properties</span></span>

<span data-ttu-id="01f5c-113">**Win32 \_ TSDeploymentLicensing** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="01f5c-113">The **Win32\_TSDeploymentLicensing** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01f5c-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="01f5c-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f5c-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01f5c-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01f5c-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01f5c-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01f5c-117">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="01f5c-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="01f5c-118">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="01f5c-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="01f5c-119">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="01f5c-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01f5c-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="01f5c-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f5c-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01f5c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01f5c-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01f5c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01f5c-123">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="01f5c-123">Description of the object.</span></span>

<span data-ttu-id="01f5c-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="01f5c-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01f5c-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="01f5c-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f5c-126">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="01f5c-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="01f5c-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01f5c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01f5c-128">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="01f5c-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="01f5c-129">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="01f5c-129">The date the object was installed.</span></span> <span data-ttu-id="01f5c-130">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="01f5c-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="01f5c-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="01f5c-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01f5c-132">**LicenseServers**</span><span class="sxs-lookup"><span data-stu-id="01f5c-132">**LicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f5c-133">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="01f5c-133">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="01f5c-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="01f5c-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="01f5c-135">指定要使用的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="01f5c-135">Specifies the license servers to use.</span></span>

</dd> <dt>

<span data-ttu-id="01f5c-136">**LicensingType**</span><span class="sxs-lookup"><span data-stu-id="01f5c-136">**LicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f5c-137">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="01f5c-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01f5c-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="01f5c-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="01f5c-139">授權模式</span><span class="sxs-lookup"><span data-stu-id="01f5c-139">Licensing Mode</span></span>

<dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span data-ttu-id="01f5c-140">**每一裝置** (2) </span><span class="sxs-lookup"><span data-stu-id="01f5c-140">**Per Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="01f5c-141">**每位使用者** (4) </span><span class="sxs-lookup"><span data-stu-id="01f5c-141">**Per User** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Yet_Configured"></span><span id="not_yet_configured"></span><span id="NOT_YET_CONFIGURED"></span>

<span data-ttu-id="01f5c-142">**尚未設定** (5) </span><span class="sxs-lookup"><span data-stu-id="01f5c-142">**Not Yet Configured** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01f5c-143">**名稱**</span><span class="sxs-lookup"><span data-stu-id="01f5c-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f5c-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01f5c-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01f5c-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01f5c-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01f5c-146">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="01f5c-146">The name of the object.</span></span>

<span data-ttu-id="01f5c-147">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="01f5c-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01f5c-148">**狀態**</span><span class="sxs-lookup"><span data-stu-id="01f5c-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f5c-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01f5c-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01f5c-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01f5c-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01f5c-151">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="01f5c-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="01f5c-152">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="01f5c-152">Current status of the object.</span></span> <span data-ttu-id="01f5c-153">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="01f5c-153">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="01f5c-154">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="01f5c-154">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="01f5c-155">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="01f5c-155">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="01f5c-156">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="01f5c-156">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="01f5c-157">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="01f5c-157">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="01f5c-158">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="01f5c-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="01f5c-159"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="01f5c-159">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="01f5c-160"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="01f5c-160">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="01f5c-161"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="01f5c-161">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="01f5c-162"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="01f5c-162">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="01f5c-163"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="01f5c-163">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="01f5c-164"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="01f5c-164">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="01f5c-165"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="01f5c-165">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="01f5c-166"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="01f5c-166">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01f5c-167">**UseCentralLicensingSettings**</span><span class="sxs-lookup"><span data-stu-id="01f5c-167">**UseCentralLicensingSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f5c-168">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="01f5c-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01f5c-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="01f5c-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="01f5c-170">指定是否使用整個部署的授權設定。</span><span class="sxs-lookup"><span data-stu-id="01f5c-170">Specifies whether to use deployment-wide licensing settings.</span></span> <span data-ttu-id="01f5c-171">**True** 表示針對此部署中的所有伺服器使用這些設定。</span><span class="sxs-lookup"><span data-stu-id="01f5c-171">**True** to use these settings for all servers in this deployment.</span></span> <span data-ttu-id="01f5c-172">**false** 表示每一伺服器設定這些值。</span><span class="sxs-lookup"><span data-stu-id="01f5c-172">**false** to set them per-server.</span></span> <span data-ttu-id="01f5c-173">如果設定為 **false**，則會忽略所有其他授權設定。</span><span class="sxs-lookup"><span data-stu-id="01f5c-173">If this is set to **false**, all other licensing settings are ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01f5c-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="01f5c-174">Requirements</span></span>



| <span data-ttu-id="01f5c-175">需求</span><span class="sxs-lookup"><span data-stu-id="01f5c-175">Requirement</span></span> | <span data-ttu-id="01f5c-176">值</span><span class="sxs-lookup"><span data-stu-id="01f5c-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01f5c-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01f5c-177">Minimum supported client</span></span><br/> | <span data-ttu-id="01f5c-178">都不支援</span><span class="sxs-lookup"><span data-stu-id="01f5c-178">None supported</span></span><br/>                                                               |
| <span data-ttu-id="01f5c-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01f5c-179">Minimum supported server</span></span><br/> | <span data-ttu-id="01f5c-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="01f5c-180">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="01f5c-181">命名空間</span><span class="sxs-lookup"><span data-stu-id="01f5c-181">Namespace</span></span><br/>                | <span data-ttu-id="01f5c-182">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="01f5c-182">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="01f5c-183">MOF</span><span class="sxs-lookup"><span data-stu-id="01f5c-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01f5c-184"><dt>TsAllow mof</dt></span><span class="sxs-lookup"><span data-stu-id="01f5c-184"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="01f5c-185">DLL</span><span class="sxs-lookup"><span data-stu-id="01f5c-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01f5c-186"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01f5c-186"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

