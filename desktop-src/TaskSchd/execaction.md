---
title: ExecAction 物件
description: 腳本物件，代表執行命令列操作的動作。
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- 執行動作工作排程器，介面
- ExecAction 物件工作排程器
- ExecAction 物件工作排程器，說明
topic_type:
- apiref
api_name:
- ExecAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cddd1b9b44612b4ce896fb3ceb99a6deeaa5e3a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105690"
---
# <a name="execaction-object"></a><span data-ttu-id="b6cb6-106">ExecAction 物件</span><span class="sxs-lookup"><span data-stu-id="b6cb6-106">ExecAction object</span></span>

<span data-ttu-id="b6cb6-107">腳本物件，代表執行命令列操作的動作。</span><span class="sxs-lookup"><span data-stu-id="b6cb6-107">Scripting object that represents an action that executes a command-line operation.</span></span>

## <a name="members"></a><span data-ttu-id="b6cb6-108">成員</span><span class="sxs-lookup"><span data-stu-id="b6cb6-108">Members</span></span>

<span data-ttu-id="b6cb6-109">**ExecAction** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b6cb6-109">The **ExecAction** object has these types of members:</span></span>

-   [<span data-ttu-id="b6cb6-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b6cb6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6cb6-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b6cb6-111">Properties</span></span>

<span data-ttu-id="b6cb6-112">**ExecAction** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b6cb6-112">The **ExecAction** object has these properties.</span></span>



| <span data-ttu-id="b6cb6-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b6cb6-113">Property</span></span>                                                            | <span data-ttu-id="b6cb6-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="b6cb6-114">Access type</span></span>           | <span data-ttu-id="b6cb6-115">Description</span><span class="sxs-lookup"><span data-stu-id="b6cb6-115">Description</span></span>                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6cb6-116">**引數**</span><span class="sxs-lookup"><span data-stu-id="b6cb6-116">**Arguments**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | <span data-ttu-id="b6cb6-117">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6cb6-117">Read/write</span></span><br/> | <span data-ttu-id="b6cb6-118">取得或設定與命令列操作相關聯的引數。</span><span class="sxs-lookup"><span data-stu-id="b6cb6-118">Gets or sets the arguments associated with the command-line operation.</span></span><br/>                                                 |
| [<span data-ttu-id="b6cb6-119">**Id**</span><span class="sxs-lookup"><span data-stu-id="b6cb6-119">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | <span data-ttu-id="b6cb6-120">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6cb6-120">Read/write</span></span><br/> | <span data-ttu-id="b6cb6-121">繼承自 [**動作**](action.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b6cb6-121">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="b6cb6-122">取得或設定動作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b6cb6-122">Gets or sets the identifier of the action.</span></span><br/>                         |
| [<span data-ttu-id="b6cb6-123">**路徑**</span><span class="sxs-lookup"><span data-stu-id="b6cb6-123">**Path**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | <span data-ttu-id="b6cb6-124">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6cb6-124">Read/write</span></span><br/> | <span data-ttu-id="b6cb6-125">取得或設定可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="b6cb6-125">Gets or sets the path to an executable file.</span></span><br/>                                                                           |
| [<span data-ttu-id="b6cb6-126">**類型**</span><span class="sxs-lookup"><span data-stu-id="b6cb6-126">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | <span data-ttu-id="b6cb6-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="b6cb6-127">Read-only</span></span><br/>  | <span data-ttu-id="b6cb6-128">繼承自 [**動作**](action.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b6cb6-128">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="b6cb6-129">取得動作的類型。</span><span class="sxs-lookup"><span data-stu-id="b6cb6-129">Gets the type of the action.</span></span><br/>                                       |
| [<span data-ttu-id="b6cb6-130">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="b6cb6-130">**WorkingDirectory**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | <span data-ttu-id="b6cb6-131">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6cb6-131">Read/write</span></span><br/> | <span data-ttu-id="b6cb6-132">取得或設定包含可執行檔的目錄，或可執行檔所使用的檔案。</span><span class="sxs-lookup"><span data-stu-id="b6cb6-132">Gets or sets the directory that contains either the executable file or the files that are used by the executable file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b6cb6-133">備註</span><span class="sxs-lookup"><span data-stu-id="b6cb6-133">Remarks</span></span>

<span data-ttu-id="b6cb6-134">如果在 [**Path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)、 [**Arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)或 [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) 屬性中使用環境變數，則在啟動工作引擎) 的 Taskeng.exe (時，會快取並使用環境變數的值。</span><span class="sxs-lookup"><span data-stu-id="b6cb6-134">If environment variables are used in the [**Path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**Arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments), or [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) properties, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched.</span></span> <span data-ttu-id="b6cb6-135">工作引擎啟動後所發生的環境變數變更將不會由工作引擎使用。</span><span class="sxs-lookup"><span data-stu-id="b6cb6-135">Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.</span></span>

<span data-ttu-id="b6cb6-136">此動作會執行命令列操作。</span><span class="sxs-lookup"><span data-stu-id="b6cb6-136">This action performs a command-line operation.</span></span> <span data-ttu-id="b6cb6-137">例如，動作可以執行腳本或啟動可執行檔。</span><span class="sxs-lookup"><span data-stu-id="b6cb6-137">For example, the action could run a script or launch an executable.</span></span>

<span data-ttu-id="b6cb6-138">讀取或寫入 XML 時，會在工作排程器架構的 [**Exec**](taskschedulerschema-exec-actiongroup-element.md) 元素中指定執行動作。</span><span class="sxs-lookup"><span data-stu-id="b6cb6-138">When reading or writing XML, an execution action is specified in the [**Exec**](taskschedulerschema-exec-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="b6cb6-139">範例</span><span class="sxs-lookup"><span data-stu-id="b6cb6-139">Examples</span></span>

<span data-ttu-id="b6cb6-140">如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="b6cb6-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6cb6-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6cb6-141">Requirements</span></span>



| <span data-ttu-id="b6cb6-142">需求</span><span class="sxs-lookup"><span data-stu-id="b6cb6-142">Requirement</span></span> | <span data-ttu-id="b6cb6-143">值</span><span class="sxs-lookup"><span data-stu-id="b6cb6-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6cb6-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6cb6-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b6cb6-145">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6cb6-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b6cb6-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6cb6-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b6cb6-147">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6cb6-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b6cb6-148">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b6cb6-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="b6cb6-149"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b6cb6-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b6cb6-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b6cb6-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6cb6-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6cb6-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





