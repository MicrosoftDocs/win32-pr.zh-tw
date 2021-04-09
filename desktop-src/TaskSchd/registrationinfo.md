---
title: RegistrationInfo 物件
description: 提供可用來描述工作之系統管理資訊的腳本物件。
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- 註冊資訊工作排程器、物件
- RegistrationInfo 物件工作排程器
- RegistrationInfo 物件工作排程器，說明
topic_type:
- apiref
api_name:
- RegistrationInfo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b7eb50da6b69622f6101fdbae4ad098d88f0366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024826"
---
# <a name="registrationinfo-object"></a><span data-ttu-id="0317c-106">RegistrationInfo 物件</span><span class="sxs-lookup"><span data-stu-id="0317c-106">RegistrationInfo object</span></span>

<span data-ttu-id="0317c-107">提供可用來描述工作之系統管理資訊的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="0317c-107">Scripting object that provides the administrative information that can be used to describe the task.</span></span> <span data-ttu-id="0317c-108">這項資訊包含詳細資料，例如工作的描述、工作的作者、註冊工作的日期，以及工作的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="0317c-108">This information includes details such as a description of the task, the author of the task, the date the task is registered, and the security descriptor of the task.</span></span>

## <a name="members"></a><span data-ttu-id="0317c-109">成員</span><span class="sxs-lookup"><span data-stu-id="0317c-109">Members</span></span>

<span data-ttu-id="0317c-110">**RegistrationInfo** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0317c-110">The **RegistrationInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="0317c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="0317c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0317c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="0317c-112">Properties</span></span>

<span data-ttu-id="0317c-113">**RegistrationInfo** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0317c-113">The **RegistrationInfo** object has these properties.</span></span>



| <span data-ttu-id="0317c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="0317c-114">Property</span></span>                                                                     | <span data-ttu-id="0317c-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="0317c-115">Access type</span></span>           | <span data-ttu-id="0317c-116">Description</span><span class="sxs-lookup"><span data-stu-id="0317c-116">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0317c-117">**作者**</span><span class="sxs-lookup"><span data-stu-id="0317c-117">**Author**</span></span>](registrationinfo-author.md)<br/>                         | <span data-ttu-id="0317c-118">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0317c-118">Read/write</span></span><br/> | <span data-ttu-id="0317c-119">取得或設定工作的作者。</span><span class="sxs-lookup"><span data-stu-id="0317c-119">Gets or sets the author of the task.</span></span><br/>                                                                                            |
| [<span data-ttu-id="0317c-120">**日期**</span><span class="sxs-lookup"><span data-stu-id="0317c-120">**Date**</span></span>](registrationinfo-date.md)<br/>                             | <span data-ttu-id="0317c-121">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0317c-121">Read/write</span></span><br/> | <span data-ttu-id="0317c-122">取得或設定工作的註冊日期和時間。</span><span class="sxs-lookup"><span data-stu-id="0317c-122">Gets or sets the date and time when the task is registered.</span></span><br/>                                                                     |
| [<span data-ttu-id="0317c-123">**描述**</span><span class="sxs-lookup"><span data-stu-id="0317c-123">**Description**</span></span>](registrationinfo-description.md)<br/>               | <span data-ttu-id="0317c-124">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0317c-124">Read/write</span></span><br/> | <span data-ttu-id="0317c-125">取得或設定工作的描述。</span><span class="sxs-lookup"><span data-stu-id="0317c-125">Gets or sets the description of the task.</span></span><br/>                                                                                       |
| [<span data-ttu-id="0317c-126">**文件**</span><span class="sxs-lookup"><span data-stu-id="0317c-126">**Documentation**</span></span>](registrationinfo-documentation.md)<br/>           | <span data-ttu-id="0317c-127">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0317c-127">Read/write</span></span><br/> | <span data-ttu-id="0317c-128">取得或設定工作的任何其他檔。</span><span class="sxs-lookup"><span data-stu-id="0317c-128">Gets or sets any additional documentation for the task.</span></span><br/>                                                                         |
| [<span data-ttu-id="0317c-129">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0317c-129">**SecurityDescriptor**</span></span>](registrationinfo-securitydescriptor.md)<br/> |                       | <span data-ttu-id="0317c-130">取得或設定工作的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="0317c-130">Gets or sets the security descriptor of the task.</span></span><br/>                                                                               |
| [<span data-ttu-id="0317c-131">**來源**</span><span class="sxs-lookup"><span data-stu-id="0317c-131">**Source**</span></span>](registrationinfo-source.md)<br/>                         | <span data-ttu-id="0317c-132">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0317c-132">Read/write</span></span><br/> | <span data-ttu-id="0317c-133">取得或設定工作源自的位置。</span><span class="sxs-lookup"><span data-stu-id="0317c-133">Gets or sets where the task originated from.</span></span> <span data-ttu-id="0317c-134">例如，工作可能源自元件、服務、應用程式或使用者。</span><span class="sxs-lookup"><span data-stu-id="0317c-134">For example, a task may originate from a component, service, application, or user.</span></span><br/> |
| [<span data-ttu-id="0317c-135">**URI**</span><span class="sxs-lookup"><span data-stu-id="0317c-135">**URI**</span></span>](registrationinfo-uri.md)<br/>                               | <span data-ttu-id="0317c-136">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0317c-136">Read/write</span></span><br/> | <span data-ttu-id="0317c-137">取得或設定工作的 URI。</span><span class="sxs-lookup"><span data-stu-id="0317c-137">Gets or sets the URI of the task.</span></span><br/>                                                                                               |
| [<span data-ttu-id="0317c-138">**版本**</span><span class="sxs-lookup"><span data-stu-id="0317c-138">**Version**</span></span>](registrationinfo-version.md)<br/>                       | <span data-ttu-id="0317c-139">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0317c-139">Read/write</span></span><br/> | <span data-ttu-id="0317c-140">取得或設定工作的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="0317c-140">Gets or sets the version number of the task.</span></span><br/>                                                                                    |
| [<span data-ttu-id="0317c-141">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="0317c-141">**XmlText**</span></span>](registrationinfo-xmltext.md)<br/>                       | <span data-ttu-id="0317c-142">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0317c-142">Read/write</span></span><br/> | <span data-ttu-id="0317c-143">取得或設定工作的 XML 格式版本的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="0317c-143">Gets or sets an XML-formatted version of the registration information for the task.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="0317c-144">備註</span><span class="sxs-lookup"><span data-stu-id="0317c-144">Remarks</span></span>

<span data-ttu-id="0317c-145">註冊資訊可以用來透過工作排程器 UI 來識別工作，或是在列舉已註冊的工作時作為搜尋準則。</span><span class="sxs-lookup"><span data-stu-id="0317c-145">Registration information can be used to identify a task through the Task Scheduler UI, or as search criteria when enumerating over the registered tasks.</span></span>

<span data-ttu-id="0317c-146">讀取或寫入工作的 XML 時，會在工作排程器架構的 [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) 元素中指定工作的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="0317c-146">When reading or writing XML for a task, registration information for the task is specified in the [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="0317c-147">範例</span><span class="sxs-lookup"><span data-stu-id="0317c-147">Examples</span></span>

<span data-ttu-id="0317c-148">如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="0317c-148">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0317c-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="0317c-149">Requirements</span></span>



| <span data-ttu-id="0317c-150">需求</span><span class="sxs-lookup"><span data-stu-id="0317c-150">Requirement</span></span> | <span data-ttu-id="0317c-151">值</span><span class="sxs-lookup"><span data-stu-id="0317c-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0317c-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0317c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="0317c-153">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0317c-153">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0317c-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0317c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="0317c-155">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0317c-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0317c-156">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0317c-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="0317c-157"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0317c-157"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0317c-158">DLL</span><span class="sxs-lookup"><span data-stu-id="0317c-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0317c-159"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0317c-159"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





