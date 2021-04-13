---
title: 'CIM_LogicalElement 類別 (遠端桌面服務) '
description: 代表抽象系統元件的所有系統元件的基類，例如設定檔、進程或系統功能（以邏輯裝置的形式）。
ms.assetid: 21e4a2ba-7bc5-4e33-a888-198299137da6
ms.tgt_platform: multiple
keywords:
- CIM_LogicalElement 類別遠端桌面服務
- CIM_LogicalElement 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- CIM_LogicalElement
- CIM_LogicalElement.Caption
- CIM_LogicalElement.Description
- CIM_LogicalElement.InstallDate
- CIM_LogicalElement.Name
- CIM_LogicalElement.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f7e58fe64f3b9dbb76a11d308aadbe6ce50331f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384086"
---
# <a name="cim_logicalelement-class-remote-desktop-services"></a><span data-ttu-id="816c0-105">CIM_LogicalElement 類別 (遠端桌面服務) </span><span class="sxs-lookup"><span data-stu-id="816c0-105">CIM_LogicalElement class (Remote Desktop Services)</span></span>

<span data-ttu-id="816c0-106">代表抽象系統元件的所有系統元件的基類，例如設定檔、進程或系統功能（以邏輯裝置的形式）。</span><span class="sxs-lookup"><span data-stu-id="816c0-106">The base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

<span data-ttu-id="816c0-107">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="816c0-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="816c0-108">語法</span><span class="sxs-lookup"><span data-stu-id="816c0-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalElement : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="816c0-109">成員</span><span class="sxs-lookup"><span data-stu-id="816c0-109">Members</span></span>

<span data-ttu-id="816c0-110">**CIM \_ LogicalElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="816c0-110">The **CIM\_LogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="816c0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="816c0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="816c0-112">屬性</span><span class="sxs-lookup"><span data-stu-id="816c0-112">Properties</span></span>

<span data-ttu-id="816c0-113">**CIM \_ LogicalElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="816c0-113">The **CIM\_LogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="816c0-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="816c0-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="816c0-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="816c0-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="816c0-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="816c0-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="816c0-117">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="816c0-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="816c0-118">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="816c0-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="816c0-119">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="816c0-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="816c0-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="816c0-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="816c0-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="816c0-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="816c0-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="816c0-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="816c0-123">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="816c0-123">Description of the object.</span></span>

<span data-ttu-id="816c0-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="816c0-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="816c0-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="816c0-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="816c0-126">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="816c0-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="816c0-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="816c0-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="816c0-128">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="816c0-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="816c0-129">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="816c0-129">The date the object was installed.</span></span> <span data-ttu-id="816c0-130">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="816c0-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="816c0-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="816c0-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="816c0-132">**名稱**</span><span class="sxs-lookup"><span data-stu-id="816c0-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="816c0-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="816c0-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="816c0-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="816c0-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="816c0-135">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="816c0-135">The name of the object.</span></span>

<span data-ttu-id="816c0-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="816c0-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="816c0-137">**狀態**</span><span class="sxs-lookup"><span data-stu-id="816c0-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="816c0-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="816c0-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="816c0-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="816c0-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="816c0-140">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="816c0-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="816c0-141">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="816c0-141">Current status of the object.</span></span> <span data-ttu-id="816c0-142">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="816c0-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="816c0-143">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="816c0-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="816c0-144">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="816c0-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="816c0-145">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="816c0-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="816c0-146">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="816c0-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="816c0-147">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="816c0-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="816c0-148"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="816c0-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="816c0-149"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="816c0-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="816c0-150"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="816c0-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="816c0-151"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="816c0-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="816c0-152"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="816c0-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="816c0-153"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="816c0-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="816c0-154"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="816c0-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="816c0-155"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="816c0-155">("Service")</span></span>


<span data-ttu-id="816c0-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="816c0-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="816c0-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="816c0-157">Requirements</span></span>



| <span data-ttu-id="816c0-158">需求</span><span class="sxs-lookup"><span data-stu-id="816c0-158">Requirement</span></span> | <span data-ttu-id="816c0-159">值</span><span class="sxs-lookup"><span data-stu-id="816c0-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="816c0-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="816c0-160">Minimum supported client</span></span><br/> | <span data-ttu-id="816c0-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="816c0-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="816c0-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="816c0-162">Minimum supported server</span></span><br/> | <span data-ttu-id="816c0-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="816c0-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="816c0-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="816c0-164">Namespace</span></span><br/>                | <span data-ttu-id="816c0-165">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="816c0-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="816c0-166">MOF</span><span class="sxs-lookup"><span data-stu-id="816c0-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="816c0-167"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="816c0-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="816c0-168">DLL</span><span class="sxs-lookup"><span data-stu-id="816c0-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="816c0-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="816c0-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="816c0-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="816c0-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="816c0-171">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="816c0-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

