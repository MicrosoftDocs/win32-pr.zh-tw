---
description: 描述讀取 WMI 腳本 API 主題的檔慣例。
ms.assetid: 889e6322-96f6-4a24-a084-e3b7bfa94a40
ms.tgt_platform: multiple
title: 腳本 API 的檔慣例
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33335982672472fa9924a6e250305a3630628b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319672"
---
# <a name="document-conventions-for-the-scripting-api"></a><span data-ttu-id="9e247-103">腳本 API 的檔慣例</span><span class="sxs-lookup"><span data-stu-id="9e247-103">Document Conventions for the Scripting API</span></span>

<span data-ttu-id="9e247-104">[適用于 WMI 的腳本 API](scripting-api-for-wmi.md)參考會使用下列檔慣例：</span><span class="sxs-lookup"><span data-stu-id="9e247-104">The [Scripting API for WMI](scripting-api-for-wmi.md) reference uses the following document conventions:</span></span>

-   <span data-ttu-id="9e247-105">參數類型的定義是使用前置詞： b (布林值) 、str (字串) 、I (整數) 、obj (Automation 物件) 、var (變異) 。</span><span class="sxs-lookup"><span data-stu-id="9e247-105">Parameter types are defined using a prefix: b (Boolean), str (string), I (integer), obj (Automation object), var (Variant).</span></span>
-   <span data-ttu-id="9e247-106">選擇性參數會以方括弧括住，並以指派顯示其預設值。</span><span class="sxs-lookup"><span data-stu-id="9e247-106">Optional parameters are placed in square brackets with their default values shown by assignment.</span></span>
-   <span data-ttu-id="9e247-107">在物件參數的情況下，"obj" 前置詞後面的字元會指出所需的物件類型。</span><span class="sxs-lookup"><span data-stu-id="9e247-107">In the case of object parameters, the characters after the "obj" prefix indicate the type of object expected.</span></span>



| <span data-ttu-id="9e247-108">物件參數</span><span class="sxs-lookup"><span data-stu-id="9e247-108">Object parameter</span></span>      | <span data-ttu-id="9e247-109">物件型別</span><span class="sxs-lookup"><span data-stu-id="9e247-109">Object type</span></span>                                          |
|-----------------------|------------------------------------------------------|
| <span data-ttu-id="9e247-110">*WbemDatetime*</span><span class="sxs-lookup"><span data-stu-id="9e247-110">*WbemDatetime*</span></span>        | [<span data-ttu-id="9e247-111">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="9e247-111">**SWbemDateTime**</span></span>](swbemdatetime.md)               |
| <span data-ttu-id="9e247-112">*WbemEventSource*</span><span class="sxs-lookup"><span data-stu-id="9e247-112">*WbemEventSource*</span></span>     | [<span data-ttu-id="9e247-113">**SWbemEventSource**</span><span class="sxs-lookup"><span data-stu-id="9e247-113">**SWbemEventSource**</span></span>](swbemeventsource.md)         |
| <span data-ttu-id="9e247-114">*WbemLocator*</span><span class="sxs-lookup"><span data-stu-id="9e247-114">*WbemLocator*</span></span>         | [<span data-ttu-id="9e247-115">**Wbemscripting.swbemlocator**</span><span class="sxs-lookup"><span data-stu-id="9e247-115">**SWbemLocator**</span></span>](swbemlocator.md)                 |
| <span data-ttu-id="9e247-116">*WbemMethod*</span><span class="sxs-lookup"><span data-stu-id="9e247-116">*WbemMethod*</span></span>          | [<span data-ttu-id="9e247-117">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="9e247-117">**SWbemMethod**</span></span>](swbemmethod.md)                   |
| <span data-ttu-id="9e247-118">*WbemMethodSet*</span><span class="sxs-lookup"><span data-stu-id="9e247-118">*WbemMethodSet*</span></span>       | [<span data-ttu-id="9e247-119">**SWbemMethodSet**</span><span class="sxs-lookup"><span data-stu-id="9e247-119">**SWbemMethodSet**</span></span>](swbemmethodset.md)             |
| <span data-ttu-id="9e247-120">*WbemNamedValueSet*</span><span class="sxs-lookup"><span data-stu-id="9e247-120">*WbemNamedValueSet*</span></span>   | [<span data-ttu-id="9e247-121">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="9e247-121">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)     |
| <span data-ttu-id="9e247-122">*WbemObject*</span><span class="sxs-lookup"><span data-stu-id="9e247-122">*WbemObject*</span></span>          | [<span data-ttu-id="9e247-123">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="9e247-123">**SWbemObject**</span></span>](swbemobject.md)                   |
| <span data-ttu-id="9e247-124">*WbemObjectEx*</span><span class="sxs-lookup"><span data-stu-id="9e247-124">*WbemObjectEx*</span></span>        | [<span data-ttu-id="9e247-125">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="9e247-125">**SWbemObjectEx**</span></span>](swbemobjectex.md)               |
| <span data-ttu-id="9e247-126">*WbemObjectPath*</span><span class="sxs-lookup"><span data-stu-id="9e247-126">*WbemObjectPath*</span></span>      | [<span data-ttu-id="9e247-127">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="9e247-127">**SWbemObjectPath**</span></span>](swbemobjectpath.md)           |
| <span data-ttu-id="9e247-128">*WbemObjectSet*</span><span class="sxs-lookup"><span data-stu-id="9e247-128">*WbemObjectSet*</span></span>       | [<span data-ttu-id="9e247-129">**Swbemobjectset 搭配使用**</span><span class="sxs-lookup"><span data-stu-id="9e247-129">**SWbemObjectSet**</span></span>](swbemobjectset.md)             |
| <span data-ttu-id="9e247-130">*WbemPrivilege*</span><span class="sxs-lookup"><span data-stu-id="9e247-130">*WbemPrivilege*</span></span>       | [<span data-ttu-id="9e247-131">**SWbemPrivilege**</span><span class="sxs-lookup"><span data-stu-id="9e247-131">**SWbemPrivilege**</span></span>](swbemprivilege.md)             |
| <span data-ttu-id="9e247-132">*WbemPrivilegeSet*</span><span class="sxs-lookup"><span data-stu-id="9e247-132">*WbemPrivilegeSet*</span></span>    | [<span data-ttu-id="9e247-133">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="9e247-133">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)       |
| <span data-ttu-id="9e247-134">*WbemProperty*</span><span class="sxs-lookup"><span data-stu-id="9e247-134">*WbemProperty*</span></span>        | [<span data-ttu-id="9e247-135">**Swbempropertyset**</span><span class="sxs-lookup"><span data-stu-id="9e247-135">**SWbemProperty**</span></span>](swbemproperty.md)               |
| <span data-ttu-id="9e247-136">*WbemPropertySet*</span><span class="sxs-lookup"><span data-stu-id="9e247-136">*WbemPropertySet*</span></span>     | [<span data-ttu-id="9e247-137">**內含**</span><span class="sxs-lookup"><span data-stu-id="9e247-137">**SWbemPropertySet**</span></span>](swbempropertyset.md)         |
| <span data-ttu-id="9e247-138">*WbemQualifier*</span><span class="sxs-lookup"><span data-stu-id="9e247-138">*WbemQualifier*</span></span>       | [<span data-ttu-id="9e247-139">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="9e247-139">**SWbemQualifier**</span></span>](swbemqualifier.md)             |
| <span data-ttu-id="9e247-140">*WbemQualifierSet*</span><span class="sxs-lookup"><span data-stu-id="9e247-140">*WbemQualifierSet*</span></span>    | [<span data-ttu-id="9e247-141">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="9e247-141">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)       |
| <span data-ttu-id="9e247-142">*WbemRefreshableItem*</span><span class="sxs-lookup"><span data-stu-id="9e247-142">*WbemRefreshableItem*</span></span> | [<span data-ttu-id="9e247-143">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="9e247-143">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md) |
| <span data-ttu-id="9e247-144">*WbemRefresher*</span><span class="sxs-lookup"><span data-stu-id="9e247-144">*WbemRefresher*</span></span>       | [<span data-ttu-id="9e247-145">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="9e247-145">**SWbemRefresher**</span></span>](swbemrefresher.md)             |
| <span data-ttu-id="9e247-146">*WbemServices*</span><span class="sxs-lookup"><span data-stu-id="9e247-146">*WbemServices*</span></span>        | [<span data-ttu-id="9e247-147">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="9e247-147">**SWbemServices**</span></span>](swbemservices.md)               |
| <span data-ttu-id="9e247-148">*WbemServicesEx*</span><span class="sxs-lookup"><span data-stu-id="9e247-148">*WbemServicesEx*</span></span>      | [<span data-ttu-id="9e247-149">**SWbemServicesEx**</span><span class="sxs-lookup"><span data-stu-id="9e247-149">**SWbemServicesEx**</span></span>](swbemservicesex.md)           |



 

<span data-ttu-id="9e247-150">例如，下列程式碼會示範如何為不同類型的物件命名變數：</span><span class="sxs-lookup"><span data-stu-id="9e247-150">For example, the following code shows how to name variables for different types of objects:</span></span>


```VB
strComputerName  ' a string value for a computer name
bStatusFlag  ' a boolean value used for a status
objServices  ' an object value used to store an SWbemServices value
```



 

 



