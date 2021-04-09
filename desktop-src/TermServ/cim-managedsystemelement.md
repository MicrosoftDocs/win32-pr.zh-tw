---
title: 'CIM_ManagedSystemElement 類別 (遠端桌面服務) '
description: System 元素階層的基類。
ms.assetid: c71c0441-381f-4a46-864c-9206c43a27d0
ms.tgt_platform: multiple
keywords:
- CIM_ManagedSystemElement 類別遠端桌面服務
- CIM_ManagedSystemElement 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.Caption
- CIM_ManagedSystemElement.Description
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b242369df24724fdcc31ce925a229dba5bb515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094051"
---
# <a name="cim_managedsystemelement-class-remote-desktop-services"></a><span data-ttu-id="a94d2-105">CIM_ManagedSystemElement 類別 (遠端桌面服務) </span><span class="sxs-lookup"><span data-stu-id="a94d2-105">CIM_ManagedSystemElement class (Remote Desktop Services)</span></span>

<span data-ttu-id="a94d2-106">System 元素階層的基類。</span><span class="sxs-lookup"><span data-stu-id="a94d2-106">The base class for the system element hierarchy.</span></span>

<span data-ttu-id="a94d2-107">任何可辨別的系統元件都是包含在這個類別中的候選。</span><span class="sxs-lookup"><span data-stu-id="a94d2-107">Any distinguishable system component is a candidate for inclusion in this class.</span></span> <span data-ttu-id="a94d2-108">範例包括軟體元件，例如檔案;裝置，例如磁片磁碟機和控制器;和實體元件，例如晶片和卡片</span><span class="sxs-lookup"><span data-stu-id="a94d2-108">Examples include software components, such as files; devices, such as disk drives and controllers; and physical components, such as chips and cards</span></span>

<span data-ttu-id="a94d2-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a94d2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a94d2-110">語法</span><span class="sxs-lookup"><span data-stu-id="a94d2-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C517-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="a94d2-111">成員</span><span class="sxs-lookup"><span data-stu-id="a94d2-111">Members</span></span>

<span data-ttu-id="a94d2-112">**CIM \_ ManagedSystemElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a94d2-112">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="a94d2-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a94d2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a94d2-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a94d2-114">Properties</span></span>

<span data-ttu-id="a94d2-115">**CIM \_ ManagedSystemElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a94d2-115">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a94d2-116">**標題**</span><span class="sxs-lookup"><span data-stu-id="a94d2-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a94d2-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a94d2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a94d2-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a94d2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a94d2-119">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="a94d2-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a94d2-120">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="a94d2-120">Short description (one-line string) of the object.</span></span>

</dd> <dt>

<span data-ttu-id="a94d2-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="a94d2-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a94d2-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a94d2-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a94d2-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a94d2-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a94d2-124">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="a94d2-124">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="a94d2-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a94d2-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a94d2-126">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="a94d2-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a94d2-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a94d2-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a94d2-128">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="a94d2-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="a94d2-129">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="a94d2-129">The date the object was installed.</span></span> <span data-ttu-id="a94d2-130">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="a94d2-130">A lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="a94d2-131">**名稱**</span><span class="sxs-lookup"><span data-stu-id="a94d2-131">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a94d2-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a94d2-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a94d2-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a94d2-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a94d2-134">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="a94d2-134">The name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="a94d2-135">**狀態**</span><span class="sxs-lookup"><span data-stu-id="a94d2-135">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a94d2-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a94d2-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a94d2-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a94d2-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a94d2-138">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="a94d2-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="a94d2-139">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="a94d2-139">Current status of the object.</span></span> <span data-ttu-id="a94d2-140">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="a94d2-140">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a94d2-141">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="a94d2-141">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a94d2-142">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="a94d2-142">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a94d2-143">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="a94d2-143">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a94d2-144">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="a94d2-144">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<dt>



 <span data-ttu-id="a94d2-145"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="a94d2-145">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a94d2-146"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="a94d2-146">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a94d2-147"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="a94d2-147">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a94d2-148"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="a94d2-148">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a94d2-149"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="a94d2-149">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a94d2-150"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="a94d2-150">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a94d2-151"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="a94d2-151">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a94d2-152"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="a94d2-152">("Service")</span></span>


<span data-ttu-id="a94d2-153"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a94d2-153"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a94d2-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="a94d2-154">Requirements</span></span>



| <span data-ttu-id="a94d2-155">需求</span><span class="sxs-lookup"><span data-stu-id="a94d2-155">Requirement</span></span> | <span data-ttu-id="a94d2-156">值</span><span class="sxs-lookup"><span data-stu-id="a94d2-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a94d2-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a94d2-157">Minimum supported client</span></span><br/> | <span data-ttu-id="a94d2-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a94d2-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a94d2-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a94d2-159">Minimum supported server</span></span><br/> | <span data-ttu-id="a94d2-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a94d2-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a94d2-161">命名空間</span><span class="sxs-lookup"><span data-stu-id="a94d2-161">Namespace</span></span><br/>                | <span data-ttu-id="a94d2-162">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="a94d2-162">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a94d2-163">MOF</span><span class="sxs-lookup"><span data-stu-id="a94d2-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a94d2-164"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="a94d2-164"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a94d2-165">DLL</span><span class="sxs-lookup"><span data-stu-id="a94d2-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a94d2-166"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a94d2-166"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

