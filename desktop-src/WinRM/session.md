---
title: 'Session 物件 (WSManDisp) '
description: 定義作業和會話設定。
ms.assetid: b98ca759-71cb-492e-8645-8766b202eb36
ms.tgt_platform: multiple
keywords:
- 會話物件 Windows 遠端管理
- 會話物件 Windows 遠端管理，說明
topic_type:
- apiref
api_name:
- Session
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e47658ad8a89af5adb2135b86cc2ad9b6ef438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935128"
---
# <a name="session-object-wsmandisph"></a><span data-ttu-id="84e7c-105">Session 物件 (WSManDisp) </span><span class="sxs-lookup"><span data-stu-id="84e7c-105">Session object (WSManDisp.h)</span></span>

<span data-ttu-id="84e7c-106">定義作業和會話設定。</span><span class="sxs-lookup"><span data-stu-id="84e7c-106">Defines operations and session settings.</span></span> <span data-ttu-id="84e7c-107">任何 Windows 遠端管理作業都需要建立連接至遠端電腦、[*基礎管理控制器*](windows-remote-management-glossary.md) (BMC) 或本機電腦的 **會話**。</span><span class="sxs-lookup"><span data-stu-id="84e7c-107">Any Windows Remote Management operations require creation of a **Session** that connects to a remote computer, [*base management controller*](windows-remote-management-glossary.md) (BMC), or the local computer.</span></span> <span data-ttu-id="84e7c-108">WinRM 網路作業包括取得、寫入或列舉資料，或叫用方法。</span><span class="sxs-lookup"><span data-stu-id="84e7c-108">WinRM network operations include getting, writing, or enumerating data, or invoking methods.</span></span> <span data-ttu-id="84e7c-109">**Session** 物件的方法會鏡像 WS-Management 通訊協定中定義的基本作業。</span><span class="sxs-lookup"><span data-stu-id="84e7c-109">The methods of the **Session** object mirror the basic operations defined in the WS-Management protocol.</span></span>

## <a name="members"></a><span data-ttu-id="84e7c-110">成員</span><span class="sxs-lookup"><span data-stu-id="84e7c-110">Members</span></span>

<span data-ttu-id="84e7c-111">**Session** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="84e7c-111">The **Session** object has these types of members:</span></span>

-   [<span data-ttu-id="84e7c-112">方法</span><span class="sxs-lookup"><span data-stu-id="84e7c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="84e7c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="84e7c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="84e7c-114">方法</span><span class="sxs-lookup"><span data-stu-id="84e7c-114">Methods</span></span>

<span data-ttu-id="84e7c-115">**Session** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="84e7c-115">The **Session** object has these methods.</span></span>



| <span data-ttu-id="84e7c-116">方法</span><span class="sxs-lookup"><span data-stu-id="84e7c-116">Method</span></span>                                 | <span data-ttu-id="84e7c-117">描述</span><span class="sxs-lookup"><span data-stu-id="84e7c-117">Description</span></span>                                                                                                                 |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84e7c-118">**創建**</span><span class="sxs-lookup"><span data-stu-id="84e7c-118">**Create**</span></span>](session-create.md)       | <span data-ttu-id="84e7c-119">建立資源的新實例，並傳回新物件的 URI。</span><span class="sxs-lookup"><span data-stu-id="84e7c-119">Creates a new instance of a resource and returns the URI of the new object.</span></span><br/>                                      |
| [<span data-ttu-id="84e7c-120">**刪除**</span><span class="sxs-lookup"><span data-stu-id="84e7c-120">**Delete**</span></span>](session-delete.md)       | <span data-ttu-id="84e7c-121">刪除資源 URI 中指定的資源。</span><span class="sxs-lookup"><span data-stu-id="84e7c-121">Deletes the resource specified in the resource URI.</span></span><br/>                                                              |
| [<span data-ttu-id="84e7c-122">**列舉**</span><span class="sxs-lookup"><span data-stu-id="84e7c-122">**Enumerate**</span></span>](session-enumerate.md) | <span data-ttu-id="84e7c-123">列舉集合、資料表或訊息記錄資源。</span><span class="sxs-lookup"><span data-stu-id="84e7c-123">Enumerates a collection, table, or message log resource.</span></span><br/>                                                         |
| [<span data-ttu-id="84e7c-124">**Get**</span><span class="sxs-lookup"><span data-stu-id="84e7c-124">**Get**</span></span>](session-get.md)             | <span data-ttu-id="84e7c-125">從服務抓取資源，並傳回目前資源實例的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="84e7c-125">Retrieves a resource from the service and returns an XML representation of the current instance of the resource.</span></span><br/> |
| [<span data-ttu-id="84e7c-126">**識別**</span><span class="sxs-lookup"><span data-stu-id="84e7c-126">**Identify**</span></span>](session-identify.md)   | <span data-ttu-id="84e7c-127">查詢遠端電腦，以判斷它是否支援 WS-Management 的通訊協定</span><span class="sxs-lookup"><span data-stu-id="84e7c-127">Queries a remote computer to determine if it supports the WS-Management protocol</span></span><br/>                                 |
| [<span data-ttu-id="84e7c-128">**調用**</span><span class="sxs-lookup"><span data-stu-id="84e7c-128">**Invoke**</span></span>](session-invoke.md)       | <span data-ttu-id="84e7c-129">叫用方法，這個方法會傳回方法呼叫的結果。</span><span class="sxs-lookup"><span data-stu-id="84e7c-129">Invokes a method that returns the results of the method call.</span></span><br/>                                                    |
| [<span data-ttu-id="84e7c-130">**把**</span><span class="sxs-lookup"><span data-stu-id="84e7c-130">**Put**</span></span>](session-put.md)             | <span data-ttu-id="84e7c-131">更新資源。</span><span class="sxs-lookup"><span data-stu-id="84e7c-131">Updates a resource.</span></span><br/>                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="84e7c-132">屬性</span><span class="sxs-lookup"><span data-stu-id="84e7c-132">Properties</span></span>

<span data-ttu-id="84e7c-133">**Session** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="84e7c-133">The **Session** object has these properties.</span></span>



| <span data-ttu-id="84e7c-134">屬性</span><span class="sxs-lookup"><span data-stu-id="84e7c-134">Property</span></span>                                            | <span data-ttu-id="84e7c-135">存取類型</span><span class="sxs-lookup"><span data-stu-id="84e7c-135">Access type</span></span>           | <span data-ttu-id="84e7c-136">Description</span><span class="sxs-lookup"><span data-stu-id="84e7c-136">Description</span></span>                                                                                                                                                                                                                 |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84e7c-137">**BatchItems**</span><span class="sxs-lookup"><span data-stu-id="84e7c-137">**BatchItems**</span></span>](session-batchitems.md)<br/> | <span data-ttu-id="84e7c-138">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="84e7c-138">Read/write</span></span><br/> | <span data-ttu-id="84e7c-139">設定並取得每個列舉批次中的專案數。</span><span class="sxs-lookup"><span data-stu-id="84e7c-139">Sets and gets the number of items in each enumeration batch.</span></span> <span data-ttu-id="84e7c-140">列舉期間無法變更此值。</span><span class="sxs-lookup"><span data-stu-id="84e7c-140">This value cannot be changed during an enumeration.</span></span> <span data-ttu-id="84e7c-141">依預設，預設為不限數目的專案。</span><span class="sxs-lookup"><span data-stu-id="84e7c-141">By default, the default is an unlimited number of items.</span></span> <span data-ttu-id="84e7c-142">資源提供者可能會設定限制。</span><span class="sxs-lookup"><span data-stu-id="84e7c-142">The resource provider may set a limit.</span></span><br/> |
| [<span data-ttu-id="84e7c-143">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="84e7c-143">**Error**</span></span>](session-error.md)<br/>           | <span data-ttu-id="84e7c-144">唯讀</span><span class="sxs-lookup"><span data-stu-id="84e7c-144">Read-only</span></span><br/>  | <span data-ttu-id="84e7c-145">取得 XML 資料流程中的其他錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="84e7c-145">Gets additional error information in an XML stream.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="84e7c-146">**超時**</span><span class="sxs-lookup"><span data-stu-id="84e7c-146">**Timeout**</span></span>](session-timeout.md)<br/>       | <span data-ttu-id="84e7c-147">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="84e7c-147">Read/write</span></span><br/> | <span data-ttu-id="84e7c-148">設定並取得用戶端應用程式等候的最大時間量（以毫秒為單位） () 。</span><span class="sxs-lookup"><span data-stu-id="84e7c-148">Sets and gets the maximum amount of time (in milliseconds) for the client application to wait.</span></span><br/>                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="84e7c-149">備註</span><span class="sxs-lookup"><span data-stu-id="84e7c-149">Remarks</span></span>

<span data-ttu-id="84e7c-150">**會話** 物件會對應至 [**iwsmansession.invoke**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)介面。</span><span class="sxs-lookup"><span data-stu-id="84e7c-150">The **Session** object corresponds to the [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="84e7c-151">範例</span><span class="sxs-lookup"><span data-stu-id="84e7c-151">Examples</span></span>

<span data-ttu-id="84e7c-152">下列 VBScript 程式碼範例顯示如何建立 **會話** 物件。</span><span class="sxs-lookup"><span data-stu-id="84e7c-152">The following VBScript code example shows how to create a **Session** object.</span></span>


```VB
' Create a WSMan object.
Dim objWsman 
Set objWsman = CreateObject( "WSMAN.Automation" )

' Create Session object.
Dim objSession
Set objSession = objWsman.CreateSession
```



## <a name="requirements"></a><span data-ttu-id="84e7c-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="84e7c-153">Requirements</span></span>



| <span data-ttu-id="84e7c-154">需求</span><span class="sxs-lookup"><span data-stu-id="84e7c-154">Requirement</span></span> | <span data-ttu-id="84e7c-155">值</span><span class="sxs-lookup"><span data-stu-id="84e7c-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="84e7c-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84e7c-156">Minimum supported client</span></span><br/> | <span data-ttu-id="84e7c-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84e7c-157">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="84e7c-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84e7c-158">Minimum supported server</span></span><br/> | <span data-ttu-id="84e7c-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84e7c-159">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="84e7c-160">標頭</span><span class="sxs-lookup"><span data-stu-id="84e7c-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="84e7c-161"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="84e7c-161"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="84e7c-162">Idl</span><span class="sxs-lookup"><span data-stu-id="84e7c-162">IDL</span></span><br/>                      | <dl> <span data-ttu-id="84e7c-163"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="84e7c-163"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="84e7c-164">程式庫</span><span class="sxs-lookup"><span data-stu-id="84e7c-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="84e7c-165"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="84e7c-165"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="84e7c-166">DLL</span><span class="sxs-lookup"><span data-stu-id="84e7c-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84e7c-167"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84e7c-167"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="84e7c-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84e7c-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84e7c-169">WinRM 腳本 API</span><span class="sxs-lookup"><span data-stu-id="84e7c-169">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="84e7c-170">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="84e7c-170">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="84e7c-171">使用 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="84e7c-171">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="84e7c-172">Windows 遠端管理中的腳本</span><span class="sxs-lookup"><span data-stu-id="84e7c-172">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="84e7c-173">從本機電腦取得資料</span><span class="sxs-lookup"><span data-stu-id="84e7c-173">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="84e7c-174">從遠端電腦取得資料</span><span class="sxs-lookup"><span data-stu-id="84e7c-174">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

 





