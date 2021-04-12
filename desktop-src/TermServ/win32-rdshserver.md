---
title: Win32_RDSHServer 類別
description: 管理遠端桌面工作階段主機 (RDSH) 伺服器。
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Win32_RDSHServer 類別遠端桌面服務
- Win32_RDSHServer 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDSHServer
- Win32_RDSHServer.Name
- Win32_RDSHServer.ConnectionBroker
- Win32_RDSHServer.CollectionAlias
- Win32_RDSHServer.ServerState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6434a4dfe6bc1a79fdaf4576a89ef552cebd5e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317264"
---
# <a name="win32_rdshserver-class"></a><span data-ttu-id="857b4-105">Win32 \_ RDSHServer 類別</span><span class="sxs-lookup"><span data-stu-id="857b4-105">Win32\_RDSHServer class</span></span>

<span data-ttu-id="857b4-106">管理遠端桌面工作階段主機 (RDSH) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="857b4-106">Manages a Remote Desktop Session Host (RDSH) server.</span></span>

<span data-ttu-id="857b4-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="857b4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="857b4-108">語法</span><span class="sxs-lookup"><span data-stu-id="857b4-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHServer
{
  string Name;
  string ConnectionBroker;
  string CollectionAlias;
  uint32 ServerState;
};
```

## <a name="members"></a><span data-ttu-id="857b4-109">成員</span><span class="sxs-lookup"><span data-stu-id="857b4-109">Members</span></span>

<span data-ttu-id="857b4-110">**Win32 \_ RDSHServer** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="857b4-110">The **Win32\_RDSHServer** class has these types of members:</span></span>

-   [<span data-ttu-id="857b4-111">方法</span><span class="sxs-lookup"><span data-stu-id="857b4-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="857b4-112">屬性</span><span class="sxs-lookup"><span data-stu-id="857b4-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="857b4-113">方法</span><span class="sxs-lookup"><span data-stu-id="857b4-113">Methods</span></span>

<span data-ttu-id="857b4-114">**Win32 \_ RDSHServer** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="857b4-114">The **Win32\_RDSHServer** class has these methods.</span></span>



| <span data-ttu-id="857b4-115">方法</span><span class="sxs-lookup"><span data-stu-id="857b4-115">Method</span></span>                                                                          | <span data-ttu-id="857b4-116">描述</span><span class="sxs-lookup"><span data-stu-id="857b4-116">Description</span></span>                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="857b4-117">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="857b4-117">**GetInt32Property**</span></span>](getint32property-win32-rdshserver.md)                   | <span data-ttu-id="857b4-118">抓取 **Win32 \_ RDSHServer** 物件的整數屬性值。</span><span class="sxs-lookup"><span data-stu-id="857b4-118">Retrieves an integer property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="857b4-119">**GetPendingStartServerList**</span><span class="sxs-lookup"><span data-stu-id="857b4-119">**GetPendingStartServerList**</span></span>](win32-rdshserver-getpendingstartserverlist.md) | <span data-ttu-id="857b4-120">抓取等候啟動的伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="857b4-120">Retrieves a list of server waiting to start.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="857b4-121">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="857b4-121">**GetStringProperty**</span></span>](getstringproperty-win32-rdshserver.md)                 | <span data-ttu-id="857b4-122">抓取 **Win32 \_ RDSHServer** 物件的字串屬性值。</span><span class="sxs-lookup"><span data-stu-id="857b4-122">Retrieves a string property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="857b4-123">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="857b4-123">**SetInt32Property**</span></span>](setint32property-win32-rdshserver.md)                   | <span data-ttu-id="857b4-124">更新 **Win32 \_ RDSHServer** 物件的整數屬性值。</span><span class="sxs-lookup"><span data-stu-id="857b4-124">Updates an integer property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="857b4-125">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="857b4-125">**SetStringProperty**</span></span>](setstringproperty-win32-rdshserver.md)                 | <span data-ttu-id="857b4-126">更新 **Win32 \_ RDSHServer** 物件的字串屬性值。</span><span class="sxs-lookup"><span data-stu-id="857b4-126">Updates a string property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="857b4-127">**TestAndSetState**</span><span class="sxs-lookup"><span data-stu-id="857b4-127">**TestAndSetState**</span></span>](win32-rdshserver-testandsetstate.md)                     | <span data-ttu-id="857b4-128">比較目前的狀態與指定的比較元;如果兩者相符，則狀態會設定為新的值。</span><span class="sxs-lookup"><span data-stu-id="857b4-128">Compares the current state to the specified comparand; if the two match, the state is set to a new value.</span></span> <span data-ttu-id="857b4-129">不論相符的結果為何，也會傳回目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="857b4-129">Regardless of the match, the current state is also returned.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="857b4-130">屬性</span><span class="sxs-lookup"><span data-stu-id="857b4-130">Properties</span></span>

<span data-ttu-id="857b4-131">**Win32 \_ RDSHServer** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="857b4-131">The **Win32\_RDSHServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="857b4-132">**CollectionAlias**</span><span class="sxs-lookup"><span data-stu-id="857b4-132">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857b4-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="857b4-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857b4-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="857b4-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="857b4-135">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="857b4-135">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="857b4-136">取得並設定指派給 RDSH 伺服器之 RDSH 集合的別名。</span><span class="sxs-lookup"><span data-stu-id="857b4-136">Gets and sets the alias to the RDSH collection to which the RDSH server is assigned.</span></span>

</dd> <dt>

<span data-ttu-id="857b4-137">**ConnectionBroker**</span><span class="sxs-lookup"><span data-stu-id="857b4-137">**ConnectionBroker**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857b4-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="857b4-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857b4-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="857b4-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="857b4-140">取得和設定管理使用者對 RDSH 伺服器之存取權的遠端桌面連線代理人 (RDCB) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="857b4-140">Gets and sets the name of the Remote Desktop Connection Broker (RDCB) that manages user access to the RDSH server.</span></span>

</dd> <dt>

<span data-ttu-id="857b4-141">**名稱**</span><span class="sxs-lookup"><span data-stu-id="857b4-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857b4-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="857b4-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857b4-143">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="857b4-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="857b4-144">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="857b4-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="857b4-145">取得和設定 RDSH 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="857b4-145">Gets and sets the name of the RDSH server.</span></span>

</dd> <dt>

<span data-ttu-id="857b4-146">**ServerState**</span><span class="sxs-lookup"><span data-stu-id="857b4-146">**ServerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857b4-147">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="857b4-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="857b4-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="857b4-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857b4-149">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="857b4-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="857b4-150">描述伺服器的狀態。</span><span class="sxs-lookup"><span data-stu-id="857b4-150">Describes the state of the server.</span></span> <span data-ttu-id="857b4-151">執行 (3) **的 \_ 目標** 以外的任何值都是保留的，而且應該視為不正確狀態。</span><span class="sxs-lookup"><span data-stu-id="857b4-151">Any value other than **TARGET\_RUNNING** (3) is reserved and should be consider an invalid state.</span></span>

<span data-ttu-id="857b4-152">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="857b4-152">The possible values are.</span></span>

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

<span data-ttu-id="857b4-153">**目標 \_未知** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="857b4-153">**TARGET\_UNKNOWN** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

<span data-ttu-id="857b4-154">**目標 \_正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="857b4-154">**TARGET\_RUNNING** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

<span data-ttu-id="857b4-155">**目標 \_無效** 的 (8) </span><span class="sxs-lookup"><span data-stu-id="857b4-155">**TARGET\_INVALID** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

<span data-ttu-id="857b4-156">**目標 \_開始** (9) </span><span class="sxs-lookup"><span data-stu-id="857b4-156">**TARGET\_STARTING** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

<span data-ttu-id="857b4-157">**目標 \_停止** (10) </span><span class="sxs-lookup"><span data-stu-id="857b4-157">**TARGET\_STOPPING** (10)</span></span>


<span data-ttu-id="857b4-158"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="857b4-158"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="857b4-159">**Windows server 2012 R2 和 Windows server 2012：** 此屬性在 Windows Server 2016 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="857b4-159">**Windows Server 2012 R2 and Windows Server 2012:** This property is unavailable prior to Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="857b4-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="857b4-160">Requirements</span></span>



| <span data-ttu-id="857b4-161">需求</span><span class="sxs-lookup"><span data-stu-id="857b4-161">Requirement</span></span> | <span data-ttu-id="857b4-162">值</span><span class="sxs-lookup"><span data-stu-id="857b4-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="857b4-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="857b4-163">Minimum supported client</span></span><br/> | <span data-ttu-id="857b4-164">都不支援</span><span class="sxs-lookup"><span data-stu-id="857b4-164">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="857b4-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="857b4-165">Minimum supported server</span></span><br/> | <span data-ttu-id="857b4-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="857b4-166">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="857b4-167">命名空間</span><span class="sxs-lookup"><span data-stu-id="857b4-167">Namespace</span></span><br/>                | <span data-ttu-id="857b4-168">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="857b4-168">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="857b4-169">MOF</span><span class="sxs-lookup"><span data-stu-id="857b4-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="857b4-170"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="857b4-170"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="857b4-171">DLL</span><span class="sxs-lookup"><span data-stu-id="857b4-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="857b4-172"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="857b4-172"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="857b4-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="857b4-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="857b4-174">遠端桌面管理服務提供者</span><span class="sxs-lookup"><span data-stu-id="857b4-174">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

