---
title: Win32_TSCPubPlugin 類別
description: 表示已設定為透過 RemoteApp 和桌面連線管理服務使用的外掛程式。
ms.assetid: 0eebdeea-4bfb-4032-a28b-870df7103473
ms.tgt_platform: multiple
keywords:
- Win32_TSCPubPlugin 類別遠端桌面服務
- Win32_TSCPubPlugin 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSCPubPlugin
- Win32_TSCPubPlugin.Caption
- Win32_TSCPubPlugin.Description
- Win32_TSCPubPlugin.InstallDate
- Win32_TSCPubPlugin.Name
- Win32_TSCPubPlugin.Status
- Win32_TSCPubPlugin.CLSID
- Win32_TSCPubPlugin.IsEnabled
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0b4fcff8cadae32d59fe45c61c506e768782d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843464"
---
# <a name="win32_tscpubplugin-class"></a><span data-ttu-id="62078-105">Win32 \_ TSCPubPlugin 類別</span><span class="sxs-lookup"><span data-stu-id="62078-105">Win32\_TSCPubPlugin class</span></span>

<span data-ttu-id="62078-106">表示已設定為透過 RemoteApp 和桌面連線管理服務使用的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="62078-106">Represents a plug-in that is configured to be used through the RemoteApp and Desktop Connection Management Service.</span></span>

<span data-ttu-id="62078-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="62078-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="62078-108">語法</span><span class="sxs-lookup"><span data-stu-id="62078-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_TSCPubPlugin : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CLSID;
  boolean  IsEnabled;
};
```

## <a name="members"></a><span data-ttu-id="62078-109">成員</span><span class="sxs-lookup"><span data-stu-id="62078-109">Members</span></span>

<span data-ttu-id="62078-110">**Win32 \_ TSCPubPlugin** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="62078-110">The **Win32\_TSCPubPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="62078-111">屬性</span><span class="sxs-lookup"><span data-stu-id="62078-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62078-112">屬性</span><span class="sxs-lookup"><span data-stu-id="62078-112">Properties</span></span>

<span data-ttu-id="62078-113">**Win32 \_ TSCPubPlugin** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="62078-113">The **Win32\_TSCPubPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62078-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="62078-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62078-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="62078-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62078-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62078-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62078-117">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="62078-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="62078-118">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="62078-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="62078-119">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="62078-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62078-120">**Clsid**</span><span class="sxs-lookup"><span data-stu-id="62078-120">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62078-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="62078-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62078-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62078-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62078-123">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="62078-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="62078-124">外掛程式的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="62078-124">The CLSID of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="62078-125">**說明**</span><span class="sxs-lookup"><span data-stu-id="62078-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62078-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="62078-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62078-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62078-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62078-128">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="62078-128">Description of the object.</span></span>

<span data-ttu-id="62078-129">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="62078-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62078-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="62078-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62078-131">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="62078-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="62078-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62078-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62078-133">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="62078-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="62078-134">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="62078-134">The date the object was installed.</span></span> <span data-ttu-id="62078-135">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="62078-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="62078-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="62078-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62078-137">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="62078-137">**IsEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62078-138">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="62078-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62078-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="62078-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62078-140">指定是否啟用外掛程式。</span><span class="sxs-lookup"><span data-stu-id="62078-140">Specifies whether the plug-in is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="62078-141">**名稱**</span><span class="sxs-lookup"><span data-stu-id="62078-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62078-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="62078-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62078-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62078-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62078-144">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="62078-144">The name of the object.</span></span>

<span data-ttu-id="62078-145">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="62078-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62078-146">**狀態**</span><span class="sxs-lookup"><span data-stu-id="62078-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62078-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="62078-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62078-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62078-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62078-149">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="62078-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="62078-150">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="62078-150">Current status of the object.</span></span> <span data-ttu-id="62078-151">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="62078-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="62078-152">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="62078-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="62078-153">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="62078-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="62078-154">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="62078-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="62078-155">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="62078-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="62078-156">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="62078-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="62078-157"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="62078-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62078-158"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="62078-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62078-159"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="62078-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62078-160"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="62078-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62078-161"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="62078-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62078-162"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="62078-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62078-163"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="62078-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62078-164"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="62078-164">("Service")</span></span>


<span data-ttu-id="62078-165"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="62078-165"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="62078-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="62078-166">Requirements</span></span>



| <span data-ttu-id="62078-167">需求</span><span class="sxs-lookup"><span data-stu-id="62078-167">Requirement</span></span> | <span data-ttu-id="62078-168">值</span><span class="sxs-lookup"><span data-stu-id="62078-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62078-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62078-169">Minimum supported client</span></span><br/> | <span data-ttu-id="62078-170">都不支援</span><span class="sxs-lookup"><span data-stu-id="62078-170">None supported</span></span><br/>                                                                |
| <span data-ttu-id="62078-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62078-171">Minimum supported server</span></span><br/> | <span data-ttu-id="62078-172">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="62078-172">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="62078-173">命名空間</span><span class="sxs-lookup"><span data-stu-id="62078-173">Namespace</span></span><br/>                | <span data-ttu-id="62078-174">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="62078-174">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="62078-175">MOF</span><span class="sxs-lookup"><span data-stu-id="62078-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62078-176"><dt>TscPub mof</dt></span><span class="sxs-lookup"><span data-stu-id="62078-176"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="62078-177">DLL</span><span class="sxs-lookup"><span data-stu-id="62078-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62078-178"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62078-178"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

