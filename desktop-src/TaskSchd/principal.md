---
title: Principal 物件
description: 提供主體安全性認證的腳本物件。
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Principal 物件工作排程器
- 主體物件工作排程器，說明
topic_type:
- apiref
api_name:
- Principal
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6dc9ff69973fb340bf3b140462c4012499680ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843324"
---
# <a name="principal-object"></a><span data-ttu-id="493fa-105">Principal 物件</span><span class="sxs-lookup"><span data-stu-id="493fa-105">Principal object</span></span>

<span data-ttu-id="493fa-106">提供主體安全性認證的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="493fa-106">Scripting object that provides the security credentials for a principal.</span></span> <span data-ttu-id="493fa-107">這些安全性認證會定義與主體相關聯之工作的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="493fa-107">These security credentials define the security context for the tasks that are associated with the principal.</span></span>

## <a name="members"></a><span data-ttu-id="493fa-108">成員</span><span class="sxs-lookup"><span data-stu-id="493fa-108">Members</span></span>

<span data-ttu-id="493fa-109">**Principal** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="493fa-109">The **Principal** object has these types of members:</span></span>

-   [<span data-ttu-id="493fa-110">屬性</span><span class="sxs-lookup"><span data-stu-id="493fa-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="493fa-111">屬性</span><span class="sxs-lookup"><span data-stu-id="493fa-111">Properties</span></span>

<span data-ttu-id="493fa-112">**Principal** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="493fa-112">The **Principal** object has these properties.</span></span>



| <span data-ttu-id="493fa-113">屬性</span><span class="sxs-lookup"><span data-stu-id="493fa-113">Property</span></span>                                                | <span data-ttu-id="493fa-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="493fa-114">Access type</span></span>           | <span data-ttu-id="493fa-115">Description</span><span class="sxs-lookup"><span data-stu-id="493fa-115">Description</span></span>                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="493fa-116">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="493fa-116">**DisplayName**</span></span>](principal-displayname.md)<br/> | <span data-ttu-id="493fa-117">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="493fa-117">Read/write</span></span><br/> | <span data-ttu-id="493fa-118">取得或設定工作排程器 UI 中顯示之主體的名稱。</span><span class="sxs-lookup"><span data-stu-id="493fa-118">Gets or sets the name of the principal that is displayed in the Task Scheduler UI.</span></span><br/>                                                                |
| [<span data-ttu-id="493fa-119">**GroupId**</span><span class="sxs-lookup"><span data-stu-id="493fa-119">**GroupId**</span></span>](principal-groupid.md)<br/>         | <span data-ttu-id="493fa-120">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="493fa-120">Read/write</span></span><br/> | <span data-ttu-id="493fa-121">取得或設定執行與主體相關聯之工作所需之使用者群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="493fa-121">Gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.</span></span><br/>                           |
| [<span data-ttu-id="493fa-122">**Id**</span><span class="sxs-lookup"><span data-stu-id="493fa-122">**Id**</span></span>](principal-id.md)<br/>                   | <span data-ttu-id="493fa-123">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="493fa-123">Read/write</span></span><br/> | <span data-ttu-id="493fa-124">取得或設定主體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="493fa-124">Gets or sets the identifier of the principal.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="493fa-125">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="493fa-125">**LogonType**</span></span>](principal-logontype.md)<br/>     | <span data-ttu-id="493fa-126">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="493fa-126">Read/write</span></span><br/> | <span data-ttu-id="493fa-127">取得或設定執行與主體相關聯之工作所需的安全性登入方法。</span><span class="sxs-lookup"><span data-stu-id="493fa-127">Gets or sets the security logon method that is required to run the tasks that are associated with the principal.</span></span><br/>                                  |
| [<span data-ttu-id="493fa-128">**RunLevel**</span><span class="sxs-lookup"><span data-stu-id="493fa-128">**RunLevel**</span></span>](principal-runlevel.md)<br/>       | <span data-ttu-id="493fa-129">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="493fa-129">Read/write</span></span><br/> | <span data-ttu-id="493fa-130">取得或設定識別碼，這個識別碼用來指定執行與主體相關聯之工作所需的許可權層級。</span><span class="sxs-lookup"><span data-stu-id="493fa-130">Gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span><br/> |
| [<span data-ttu-id="493fa-131">**UserId**</span><span class="sxs-lookup"><span data-stu-id="493fa-131">**UserId**</span></span>](principal-userid.md)<br/>           | <span data-ttu-id="493fa-132">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="493fa-132">Read/write</span></span><br/> | <span data-ttu-id="493fa-133">取得或設定執行與主體相關聯之工作所需的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="493fa-133">Gets or sets the user identifier that is required to run the tasks that are associated with the principal.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="493fa-134">備註</span><span class="sxs-lookup"><span data-stu-id="493fa-134">Remarks</span></span>

<span data-ttu-id="493fa-135">指定帳戶時，請記得在程式碼中正確使用雙反斜線來指定網域和使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="493fa-135">When specifying an account, remember to properly use the double backslash in code to specify the domain and user name.</span></span> <span data-ttu-id="493fa-136">例如，使用網域 \\ \\ 使用者名稱來指定 [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid)屬性的值。</span><span class="sxs-lookup"><span data-stu-id="493fa-136">For example, use DOMAIN\\\\UserName to specify a value for the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) property.</span></span>

<span data-ttu-id="493fa-137">讀取或寫入工作的 XML 時，主體的安全性認證是在工作排程器架構的 [**principal**](taskschedulerschema-principal-principaltype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="493fa-137">When reading or writing XML for a task, the security credentials for a principal are specified in the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="493fa-138">如果工作是使用 at.exe 命令列工具來註冊，而且此物件是用來取得工作的相關資訊，則 [**LogonType**](principal-logontype.md) 屬性會傳回0， [**RunLevel**](principal-runlevel.md) 屬性將會傳回0，而且 [**UserId**](principal-userid.md) 屬性不會傳回任何內容。</span><span class="sxs-lookup"><span data-stu-id="493fa-138">If a task is registered using the at.exe command line tool, and this object is used to retrieve information about the task, then the [**LogonType**](principal-logontype.md) property will return 0, the [**RunLevel**](principal-runlevel.md) property will return 0, and the [**UserId**](principal-userid.md) property will return Nothing.</span></span>

## <a name="examples"></a><span data-ttu-id="493fa-139">範例</span><span class="sxs-lookup"><span data-stu-id="493fa-139">Examples</span></span>

<span data-ttu-id="493fa-140">如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="493fa-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="493fa-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="493fa-141">Requirements</span></span>



| <span data-ttu-id="493fa-142">需求</span><span class="sxs-lookup"><span data-stu-id="493fa-142">Requirement</span></span> | <span data-ttu-id="493fa-143">值</span><span class="sxs-lookup"><span data-stu-id="493fa-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="493fa-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="493fa-144">Minimum supported client</span></span><br/> | <span data-ttu-id="493fa-145">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="493fa-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="493fa-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="493fa-146">Minimum supported server</span></span><br/> | <span data-ttu-id="493fa-147">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="493fa-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="493fa-148">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="493fa-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="493fa-149"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="493fa-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="493fa-150">DLL</span><span class="sxs-lookup"><span data-stu-id="493fa-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="493fa-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="493fa-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





