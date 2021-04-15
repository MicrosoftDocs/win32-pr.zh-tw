---
description: 收集器實例的控制權。 需要系統管理員 (BA) 許可權。
ms.assetid: 83b485b2-b03b-4882-a3ff-187eac299755
ms.tgt_platform: multiple
title: Control 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 2681af7425fd5cacf88375e11e4658e5d4b1a2c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510389"
---
# <a name="control-class"></a><span data-ttu-id="6afac-104">Control 類別</span><span class="sxs-lookup"><span data-stu-id="6afac-104">Control class</span></span>

<span data-ttu-id="6afac-105">收集器實例的控制權。</span><span class="sxs-lookup"><span data-stu-id="6afac-105">Control of the collector instance.</span></span> <span data-ttu-id="6afac-106">需要系統管理員 (BA) 許可權。</span><span class="sxs-lookup"><span data-stu-id="6afac-106">Requires the Administrator (BA) privileges.</span></span>

<span data-ttu-id="6afac-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6afac-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6afac-108">語法</span><span class="sxs-lookup"><span data-stu-id="6afac-108">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), AMENDMENT]
class Control
{
};
```

## <a name="members"></a><span data-ttu-id="6afac-109">成員</span><span class="sxs-lookup"><span data-stu-id="6afac-109">Members</span></span>

<span data-ttu-id="6afac-110">**控制項** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6afac-110">The **Control** class has these types of members:</span></span>

-   [<span data-ttu-id="6afac-111">方法</span><span class="sxs-lookup"><span data-stu-id="6afac-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6afac-112">方法</span><span class="sxs-lookup"><span data-stu-id="6afac-112">Methods</span></span>

<span data-ttu-id="6afac-113">**控制項** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6afac-113">The **Control** class has these methods.</span></span>



| <span data-ttu-id="6afac-114">方法</span><span class="sxs-lookup"><span data-stu-id="6afac-114">Method</span></span>                                                         | <span data-ttu-id="6afac-115">描述</span><span class="sxs-lookup"><span data-stu-id="6afac-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6afac-116">**Checkpoint**</span><span class="sxs-lookup"><span data-stu-id="6afac-116">**Checkpoint**</span></span>](control-checkpoint.md)                       | <span data-ttu-id="6afac-117">如果目前的設定是復原/重做/還原的結果，請將它標示為已明確設定，讓歷程記錄保留設定的時間，並在下一次設定變更時建立備份檔案。</span><span class="sxs-lookup"><span data-stu-id="6afac-117">If the current configuration is a result of the Undo/Redo/Restore, marks it as if it has been set explicitly, so that the history will preserve the time when it was set, and a backup file will be created for it on the next configuration change.</span></span> <span data-ttu-id="6afac-118">如果已明確設定目前的設定，就不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="6afac-118">If the current configuration was already set explicitly, has no effect.</span></span> <span data-ttu-id="6afac-119">在成功時傳回1，錯誤則為0。</span><span class="sxs-lookup"><span data-stu-id="6afac-119">Returns 1 on success, 0 on error.</span></span><br/> |
| [<span data-ttu-id="6afac-120">**DumpDiagnostics**</span><span class="sxs-lookup"><span data-stu-id="6afac-120">**DumpDiagnostics**</span></span>](control-dumpdiagnostics.md)             | <span data-ttu-id="6afac-121">將診斷資訊傾印到記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="6afac-121">Dump the diagnostic information into the log.</span></span><br/>                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="6afac-122">**FastShutdown**</span><span class="sxs-lookup"><span data-stu-id="6afac-122">**FastShutdown**</span></span>](control-fastshutdown.md)                   | <span data-ttu-id="6afac-123">快速停止收集器，並捨棄所有已排入佇列的資料。</span><span class="sxs-lookup"><span data-stu-id="6afac-123">Stop the collector quickly, discarding all the queued data.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="6afac-124">**清除**</span><span class="sxs-lookup"><span data-stu-id="6afac-124">**Flush**</span></span>](control-flush.md)                                 | <span data-ttu-id="6afac-125">清除轉寄站緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6afac-125">Flush the forwarder buffers.</span></span><br/>                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="6afac-126">**GetConfiguration**</span><span class="sxs-lookup"><span data-stu-id="6afac-126">**GetConfiguration**</span></span>](control-getconfiguration.md)           | <span data-ttu-id="6afac-127">讀取收集器的主動式設定。</span><span class="sxs-lookup"><span data-stu-id="6afac-127">Read the active configuration of the collector.</span></span><br/>                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="6afac-128">**IsConfigurationEqual**</span><span class="sxs-lookup"><span data-stu-id="6afac-128">**IsConfigurationEqual**</span></span>](control-isconfigurationequal.md)   | <span data-ttu-id="6afac-129">將引數與收集器的使用中設定進行比較。</span><span class="sxs-lookup"><span data-stu-id="6afac-129">Compare the argument with the active configuration of the collector.</span></span> <span data-ttu-id="6afac-130">如果兩者相符，則傳回1，否則傳回0。</span><span class="sxs-lookup"><span data-stu-id="6afac-130">Returns 1 if they match, 0 if they don't.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="6afac-131">**ListBackups**</span><span class="sxs-lookup"><span data-stu-id="6afac-131">**ListBackups**</span></span>](control-listbackups.md)                     | <span data-ttu-id="6afac-132">傳回可還原的已儲存備份配置檔案清單。</span><span class="sxs-lookup"><span data-stu-id="6afac-132">Return the list of the saved backup configuration files that can be restored.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="6afac-133">**取消復原**</span><span class="sxs-lookup"><span data-stu-id="6afac-133">**Redo**</span></span>](control-redo.md)                                   | <span data-ttu-id="6afac-134">從較新的備份檔案中重設收集器的使用中設定， (從目前的原始時間戳記) 開始判斷。</span><span class="sxs-lookup"><span data-stu-id="6afac-134">Reset the active configuration of the collector from the later backup file (determined by going forward from the current original timestamp).</span></span> <span data-ttu-id="6afac-135">如果設定已復原，這表示會重做復原的變更。</span><span class="sxs-lookup"><span data-stu-id="6afac-135">If the configuration has been undone, this means redoing the undone change.</span></span> <span data-ttu-id="6afac-136">在成功時傳回1，錯誤則為0。</span><span class="sxs-lookup"><span data-stu-id="6afac-136">Returns 1 on success, 0 on error.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="6afac-137">**RestoreFile**</span><span class="sxs-lookup"><span data-stu-id="6afac-137">**RestoreFile**</span></span>](control-restorefile.md)                     | <span data-ttu-id="6afac-138">從備份檔案還原收集器的主動式設定。</span><span class="sxs-lookup"><span data-stu-id="6afac-138">Restore the active configuration of the collector from a backup file.</span></span> <span data-ttu-id="6afac-139">在成功時傳回1，錯誤則為0。</span><span class="sxs-lookup"><span data-stu-id="6afac-139">Returns 1 on success, 0 on error.</span></span><br/>                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="6afac-140">**RestoreFromTime**</span><span class="sxs-lookup"><span data-stu-id="6afac-140">**RestoreFromTime**</span></span>](control-restorefromtime.md)             | <span data-ttu-id="6afac-141">從以時間戳記選取的備份檔案還原收集器的使用中設定。</span><span class="sxs-lookup"><span data-stu-id="6afac-141">Restore the active configuration of the collector from a backup file, selected by a timestamp.</span></span> <span data-ttu-id="6afac-142">在成功時傳回1，錯誤則為0。</span><span class="sxs-lookup"><span data-stu-id="6afac-142">Returns 1 on success, 0 on error.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="6afac-143">**SetConfiguration**</span><span class="sxs-lookup"><span data-stu-id="6afac-143">**SetConfiguration**</span></span>](control-setconfiguration.md)           | <span data-ttu-id="6afac-144">設定收集器的新使用中設定。</span><span class="sxs-lookup"><span data-stu-id="6afac-144">Set the new active configuration of the collector.</span></span> <span data-ttu-id="6afac-145">在成功時傳回1，錯誤則為0。</span><span class="sxs-lookup"><span data-stu-id="6afac-145">Returns 1 on success, 0 on error.</span></span><br/>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="6afac-146">**關閉**</span><span class="sxs-lookup"><span data-stu-id="6afac-146">**Shutdown**</span></span>](control-shutdown.md)                           | <span data-ttu-id="6afac-147">停止收集器。</span><span class="sxs-lookup"><span data-stu-id="6afac-147">Stop the collector.</span></span> <span data-ttu-id="6afac-148">如果收集器是以服務方式執行，則停止服務是較佳的方法。</span><span class="sxs-lookup"><span data-stu-id="6afac-148">If the collector is running as a service, stopping the service is the better approach.</span></span><br/>                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="6afac-149">**復原**</span><span class="sxs-lookup"><span data-stu-id="6afac-149">**Undo**</span></span>](control-undo.md)                                   | <span data-ttu-id="6afac-150">從先前的備份檔案還原收集器的使用中設定， (由從目前的原始時間戳記) 來判斷。</span><span class="sxs-lookup"><span data-stu-id="6afac-150">Restore the active configuration of the collector from the previous backup file (determined by going back from the current original timestamp).</span></span> <span data-ttu-id="6afac-151">如果設定是剛設定的，這表示還原該變更。</span><span class="sxs-lookup"><span data-stu-id="6afac-151">If the configuration has been just set, this means undoing that change.</span></span> <span data-ttu-id="6afac-152">連續的呼叫將會復原到先前和先前的設定。</span><span class="sxs-lookup"><span data-stu-id="6afac-152">The consecutive calls will undo to the earlier and earlier configurations.</span></span> <span data-ttu-id="6afac-153">在成功時傳回1，錯誤則為0。</span><span class="sxs-lookup"><span data-stu-id="6afac-153">Returns 1 on success, 0 on error.</span></span><br/>                           |
| [<span data-ttu-id="6afac-154">**ValidateConfiguration**</span><span class="sxs-lookup"><span data-stu-id="6afac-154">**ValidateConfiguration**</span></span>](control-validateconfiguration.md) | <span data-ttu-id="6afac-155">驗證設定文字的正確性，而不將其設定為使用中。</span><span class="sxs-lookup"><span data-stu-id="6afac-155">Validate a configuration text for correctness without setting it active.</span></span> <span data-ttu-id="6afac-156">在成功時傳回1，錯誤則為0。</span><span class="sxs-lookup"><span data-stu-id="6afac-156">Returns 1 on success, 0 on error.</span></span><br/>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="6afac-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="6afac-157">Requirements</span></span>



| <span data-ttu-id="6afac-158">需求</span><span class="sxs-lookup"><span data-stu-id="6afac-158">Requirement</span></span> | <span data-ttu-id="6afac-159">值</span><span class="sxs-lookup"><span data-stu-id="6afac-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6afac-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6afac-160">Minimum supported client</span></span><br/> | <span data-ttu-id="6afac-161">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6afac-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6afac-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6afac-162">Minimum supported server</span></span><br/> | <span data-ttu-id="6afac-163">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6afac-163">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="6afac-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="6afac-164">Namespace</span></span><br/>                | <span data-ttu-id="6afac-165">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="6afac-165">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="6afac-166">MOF</span><span class="sxs-lookup"><span data-stu-id="6afac-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6afac-167"><dt>BootEventCollectorWMI mof</dt></span><span class="sxs-lookup"><span data-stu-id="6afac-167"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="6afac-168">DLL</span><span class="sxs-lookup"><span data-stu-id="6afac-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6afac-169"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6afac-169"><dt>BEvtCol.exe</dt></span></span> </dl>               |



 

 




