---
title: Win32_TSGetIcon 類別
description: 傳回檔案路徑和索引所指定的圖示內容。
ms.assetid: c0ab50f1-f5a9-4f5e-8280-40c638f09e1c
ms.tgt_platform: multiple
keywords:
- Win32_TSGetIcon 類別遠端桌面服務
- Win32_TSGetIcon 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGetIcon
- Win32_TSGetIcon.Caption
- Win32_TSGetIcon.Description
- Win32_TSGetIcon.InstallDate
- Win32_TSGetIcon.Name
- Win32_TSGetIcon.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0186e158f025be8e8a5e6cf3e87f3ad5d8b296
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934474"
---
# <a name="win32_tsgeticon-class"></a><span data-ttu-id="f3a6b-105">Win32 \_ TSGetIcon 類別</span><span class="sxs-lookup"><span data-stu-id="f3a6b-105">Win32\_TSGetIcon class</span></span>

<span data-ttu-id="f3a6b-106">傳回檔案路徑和索引所指定之圖示的內容</span><span class="sxs-lookup"><span data-stu-id="f3a6b-106">Returns the contents of the icon specified by file path and index</span></span>

<span data-ttu-id="f3a6b-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a6b-108">語法</span><span class="sxs-lookup"><span data-stu-id="f3a6b-108">Syntax</span></span>

``` syntax
class Win32_TSGetIcon : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="f3a6b-109">成員</span><span class="sxs-lookup"><span data-stu-id="f3a6b-109">Members</span></span>

<span data-ttu-id="f3a6b-110">**Win32 \_ TSGetIcon** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f3a6b-110">The **Win32\_TSGetIcon** class has these types of members:</span></span>

-   [<span data-ttu-id="f3a6b-111">方法</span><span class="sxs-lookup"><span data-stu-id="f3a6b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f3a6b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="f3a6b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f3a6b-113">方法</span><span class="sxs-lookup"><span data-stu-id="f3a6b-113">Methods</span></span>

<span data-ttu-id="f3a6b-114">**Win32 \_ TSGetIcon** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-114">The **Win32\_TSGetIcon** class has these methods.</span></span>



| <span data-ttu-id="f3a6b-115">方法</span><span class="sxs-lookup"><span data-stu-id="f3a6b-115">Method</span></span>                                     | <span data-ttu-id="f3a6b-116">描述</span><span class="sxs-lookup"><span data-stu-id="f3a6b-116">Description</span></span>                                            |
|:-------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="f3a6b-117">**GetIcon**</span><span class="sxs-lookup"><span data-stu-id="f3a6b-117">**GetIcon**</span></span>](geticon-win32-tsgeticon.md) | <span data-ttu-id="f3a6b-118">傳回指定之圖示的內容。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-118">Returns the contents of the specified icon.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f3a6b-119">屬性</span><span class="sxs-lookup"><span data-stu-id="f3a6b-119">Properties</span></span>

<span data-ttu-id="f3a6b-120">**Win32 \_ TSGetIcon** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-120">The **Win32\_TSGetIcon** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3a6b-121">**標題**</span><span class="sxs-lookup"><span data-stu-id="f3a6b-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3a6b-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f3a6b-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3a6b-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3a6b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3a6b-124">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="f3a6b-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f3a6b-125">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-125">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f3a6b-126">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3a6b-127">**說明**</span><span class="sxs-lookup"><span data-stu-id="f3a6b-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3a6b-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f3a6b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3a6b-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3a6b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3a6b-130">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-130">Description of the object.</span></span>

<span data-ttu-id="f3a6b-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3a6b-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f3a6b-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3a6b-133">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f3a6b-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f3a6b-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3a6b-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3a6b-135">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="f3a6b-135">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f3a6b-136">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-136">The date the object was installed.</span></span> <span data-ttu-id="f3a6b-137">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-137">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f3a6b-138">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3a6b-139">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f3a6b-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3a6b-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f3a6b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3a6b-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3a6b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3a6b-142">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-142">The name of the object.</span></span>

<span data-ttu-id="f3a6b-143">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3a6b-144">**狀態**</span><span class="sxs-lookup"><span data-stu-id="f3a6b-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3a6b-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f3a6b-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3a6b-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3a6b-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3a6b-147">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="f3a6b-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f3a6b-148">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-148">Current status of the object.</span></span> <span data-ttu-id="f3a6b-149">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-149">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f3a6b-150">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-150">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f3a6b-151">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-151">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f3a6b-152">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-152">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f3a6b-153">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-153">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f3a6b-154">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f3a6b-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f3a6b-155"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="f3a6b-155">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3a6b-156"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="f3a6b-156">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3a6b-157"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="f3a6b-157">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3a6b-158"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="f3a6b-158">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3a6b-159"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="f3a6b-159">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3a6b-160"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="f3a6b-160">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3a6b-161"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="f3a6b-161">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3a6b-162"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="f3a6b-162">("Service")</span></span>


<span data-ttu-id="f3a6b-163"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f3a6b-163"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="f3a6b-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3a6b-164">Requirements</span></span>



| <span data-ttu-id="f3a6b-165">需求</span><span class="sxs-lookup"><span data-stu-id="f3a6b-165">Requirement</span></span> | <span data-ttu-id="f3a6b-166">值</span><span class="sxs-lookup"><span data-stu-id="f3a6b-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a6b-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3a6b-167">Minimum supported client</span></span><br/> | <span data-ttu-id="f3a6b-168">都不支援</span><span class="sxs-lookup"><span data-stu-id="f3a6b-168">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f3a6b-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3a6b-169">Minimum supported server</span></span><br/> | <span data-ttu-id="f3a6b-170">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3a6b-170">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="f3a6b-171">命名空間</span><span class="sxs-lookup"><span data-stu-id="f3a6b-171">Namespace</span></span><br/>                | <span data-ttu-id="f3a6b-172">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="f3a6b-172">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f3a6b-173">MOF</span><span class="sxs-lookup"><span data-stu-id="f3a6b-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3a6b-174"><dt>TsAllow mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3a6b-174"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="f3a6b-175">DLL</span><span class="sxs-lookup"><span data-stu-id="f3a6b-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3a6b-176"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3a6b-176"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

