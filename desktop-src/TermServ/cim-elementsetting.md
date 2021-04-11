---
title: 'CIM_ElementSetting 類別 (遠端桌面服務) '
description: 代表 managed 系統專案與其定義的設定類別之間的關聯。
ms.assetid: b74c2fef-0f3a-46b9-9dd8-11016a8f7b57
ms.tgt_platform: multiple
keywords:
- CIM_ElementSetting 類別遠端桌面服務
- CIM_ElementSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Caption
- CIM_ElementSetting.Description
- CIM_ElementSetting.InstallDate
- CIM_ElementSetting.Name
- CIM_ElementSetting.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9aff40961ddc8fa07de6c49d6c95aefe3d005d6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094052"
---
# <a name="cim_elementsetting-class-remote-desktop-services"></a><span data-ttu-id="d738b-105">CIM_ElementSetting 類別 (遠端桌面服務) </span><span class="sxs-lookup"><span data-stu-id="d738b-105">CIM_ElementSetting class (Remote Desktop Services)</span></span>

<span data-ttu-id="d738b-106">代表 managed 系統專案與其定義的設定類別之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="d738b-106">Represents the association between managed system elements and the setting class defined for them.</span></span>

<span data-ttu-id="d738b-107">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d738b-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d738b-108">語法</span><span class="sxs-lookup"><span data-stu-id="d738b-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="d738b-109">成員</span><span class="sxs-lookup"><span data-stu-id="d738b-109">Members</span></span>

<span data-ttu-id="d738b-110">**CIM \_ ElementSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d738b-110">The **CIM\_ElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="d738b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="d738b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d738b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="d738b-112">Properties</span></span>

<span data-ttu-id="d738b-113">**CIM \_ ElementSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d738b-113">The **CIM\_ElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d738b-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="d738b-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d738b-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d738b-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d738b-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d738b-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d738b-117">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="d738b-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d738b-118">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="d738b-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="d738b-119">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d738b-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d738b-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="d738b-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d738b-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d738b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d738b-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d738b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d738b-123">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="d738b-123">Description of the object.</span></span>

<span data-ttu-id="d738b-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d738b-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d738b-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d738b-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d738b-126">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d738b-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d738b-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d738b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d738b-128">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="d738b-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="d738b-129">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="d738b-129">The date the object was installed.</span></span> <span data-ttu-id="d738b-130">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="d738b-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d738b-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d738b-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d738b-132">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d738b-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d738b-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d738b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d738b-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d738b-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d738b-135">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="d738b-135">The name of the object.</span></span>

<span data-ttu-id="d738b-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d738b-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d738b-137">**狀態**</span><span class="sxs-lookup"><span data-stu-id="d738b-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d738b-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d738b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d738b-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d738b-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d738b-140">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="d738b-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="d738b-141">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d738b-141">Current status of the object.</span></span> <span data-ttu-id="d738b-142">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="d738b-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d738b-143">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="d738b-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d738b-144">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="d738b-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d738b-145">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="d738b-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d738b-146">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="d738b-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d738b-147">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d738b-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="d738b-148"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="d738b-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d738b-149"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="d738b-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d738b-150"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="d738b-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d738b-151"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="d738b-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d738b-152"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="d738b-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d738b-153"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="d738b-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d738b-154"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="d738b-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d738b-155"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="d738b-155">("Service")</span></span>


<span data-ttu-id="d738b-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d738b-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d738b-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="d738b-157">Requirements</span></span>



| <span data-ttu-id="d738b-158">需求</span><span class="sxs-lookup"><span data-stu-id="d738b-158">Requirement</span></span> | <span data-ttu-id="d738b-159">值</span><span class="sxs-lookup"><span data-stu-id="d738b-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d738b-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d738b-160">Minimum supported client</span></span><br/> | <span data-ttu-id="d738b-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d738b-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d738b-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d738b-162">Minimum supported server</span></span><br/> | <span data-ttu-id="d738b-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d738b-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d738b-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="d738b-164">Namespace</span></span><br/>                | <span data-ttu-id="d738b-165">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="d738b-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d738b-166">MOF</span><span class="sxs-lookup"><span data-stu-id="d738b-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d738b-167"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="d738b-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d738b-168">DLL</span><span class="sxs-lookup"><span data-stu-id="d738b-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d738b-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d738b-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d738b-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d738b-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d738b-171">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="d738b-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

