---
description: 為 C/c + + 程式設計人員提供適用于 WMI 的腳本 API 的介面，以取代 COM API 版本。
ms.assetid: 18f6cc70-9df1-4d43-a2e0-af03e2f9e2c5
ms.tgt_platform: multiple
title: 自動化介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 652e9a1fb35a66bddb9f0aebe543770e89e6e2ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985052"
---
# <a name="automation-interfaces"></a><span data-ttu-id="aa1f0-103">自動化介面</span><span class="sxs-lookup"><span data-stu-id="aa1f0-103">Automation Interfaces</span></span>

<span data-ttu-id="aa1f0-104">自動化 API 可讓 C/c + + 程式設計人員使用適用于 WMI 的腳本 API 的介面，取代 COM API 的版本。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-104">The Automation API makes the interfaces of the Scripting API for WMI available to C/C++ programmers, in place of the COM API versions.</span></span>

<span data-ttu-id="aa1f0-105">下表列出 WMI 物件，以及如何在自動化 API 中使用它們。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-105">The following table lists WMI objects and how they are used in the Automation API.</span></span> <span data-ttu-id="aa1f0-106">適用于 WMI 對等的腳本 API 之介面檔的交互參照連結。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-106">The cross-references link to the interface documentation for the Scripting API for WMI equivalents.</span></span>



| <span data-ttu-id="aa1f0-107">Automation 物件</span><span class="sxs-lookup"><span data-stu-id="aa1f0-107">Automation Object</span></span>                                 | <span data-ttu-id="aa1f0-108">Description</span><span class="sxs-lookup"><span data-stu-id="aa1f0-108">Description</span></span>                                                                                                                 |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa1f0-109">**ISWbemEventSource**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-109">**ISWbemEventSource**</span></span>](swbemeventsource.md)     | <span data-ttu-id="aa1f0-110">與 [**ISWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)一起抓取事件。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-110">Retrieves events in conjunction with [**ISWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span>   |
| [<span data-ttu-id="aa1f0-111">**ISWbemLastError**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-111">**ISWbemLastError**</span></span>](swbemlasterror.md)         | <span data-ttu-id="aa1f0-112">當發生錯誤時，提供延伸的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-112">Provides extended error information when an error occurs.</span></span>                                                                   |
| [<span data-ttu-id="aa1f0-113">**ISWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-113">**ISWbemLocator**</span></span>](swbemlocator.md)             | <span data-ttu-id="aa1f0-114">取得 [**ISWbemServices**](swbemservices.md) 物件的參考，該物件可以存取特定主機電腦上的 WMI。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-114">Obtains a reference to an [**ISWbemServices**](swbemservices.md) object that can access WMI on a particular host computer.</span></span> |
| [<span data-ttu-id="aa1f0-115">**ISWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-115">**ISWbemMethod**</span></span>](swbemmethod.md)               | <span data-ttu-id="aa1f0-116">包含單一方法定義。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-116">Contains a single method definition.</span></span>                                                                                        |
| [<span data-ttu-id="aa1f0-117">**ISWbemMethodSet**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-117">**ISWbemMethodSet**</span></span>](swbemmethodset.md)         | <span data-ttu-id="aa1f0-118">取得 [**ISWbemMethod**](swbemmethod.md) 物件集合的存取權。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-118">Gets access to a collection of [**ISWbemMethod**](swbemmethod.md) objects.</span></span>                                                 |
| [<span data-ttu-id="aa1f0-119">**ISWbemNamedValue**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-119">**ISWbemNamedValue**</span></span>](swbemnamedvalue.md)       | <span data-ttu-id="aa1f0-120">包含單一的名稱值。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-120">Contains a single named value.</span></span>                                                                                              |
| [<span data-ttu-id="aa1f0-121">**ISWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-121">**ISWbemNamedValueSet**</span></span>](swbemnamedvalueset.md) | <span data-ttu-id="aa1f0-122">取得 [**ISWbemNamedValue**](swbemnamedvalue.md) 物件集合的存取權。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-122">Gets access to a collection of [**ISWbemNamedValue**](swbemnamedvalue.md) objects.</span></span>                                         |
| [<span data-ttu-id="aa1f0-123">**ISWbemObject**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-123">**ISWbemObject**</span></span>](swbemobject.md)               | <span data-ttu-id="aa1f0-124">包含和操作單一通用訊息模型 (CIM) 物件類別或實例。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-124">Contains and manipulates a single Common Information Model (CIM) object class or instance.</span></span>                                  |
| [<span data-ttu-id="aa1f0-125">**ISWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-125">**ISWbemObjectPath**</span></span>](swbemobjectpath.md)       | <span data-ttu-id="aa1f0-126">產生並驗證物件路徑。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-126">Generates and validates an object path.</span></span>                                                                                     |
| [<span data-ttu-id="aa1f0-127">**ISWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-127">**ISWbemObjectSet**</span></span>](swbemobjectset.md)         | <span data-ttu-id="aa1f0-128">取得 [**ISWbemObject**](swbemobject.md) 物件集合的存取權。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-128">Gets access to a collection of [**ISWbemObject**](swbemobject.md) objects.</span></span>                                                 |
| [<span data-ttu-id="aa1f0-129">**ISWbemPrivilege**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-129">**ISWbemPrivilege**</span></span>](swbemprivilege.md)         | <span data-ttu-id="aa1f0-130">設定或清除許可權。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-130">Sets or clears a privilege.</span></span>                                                                                                 |
| [<span data-ttu-id="aa1f0-131">**ISWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-131">**ISWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)   | <span data-ttu-id="aa1f0-132">取得 [**ISWbemPrivilege**](swbemprivilege.md) 物件集合的存取權。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-132">Gets access to a collection of [**ISWbemPrivilege**](swbemprivilege.md) objects.</span></span>                                           |
| [<span data-ttu-id="aa1f0-133">**ISWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-133">**ISWbemProperty**</span></span>](swbemproperty.md)           | <span data-ttu-id="aa1f0-134">用來包含單一 CIM 屬性。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-134">Used to contain a single CIM property.</span></span>                                                                                      |
| [<span data-ttu-id="aa1f0-135">**ISWbemPropertySet**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-135">**ISWbemPropertySet**</span></span>](swbempropertyset.md)     | <span data-ttu-id="aa1f0-136">取得 [**ISWbemProperty**](swbemproperty.md) 物件集合的存取權。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-136">Get access to a collection of [**ISWbemProperty**](swbemproperty.md) objects.</span></span>                                              |
| [<span data-ttu-id="aa1f0-137">**ISWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-137">**ISWbemQualifier**</span></span>](swbemqualifier.md)         | <span data-ttu-id="aa1f0-138">包含單一類別限定詞。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-138">Contains a single class qualifier.</span></span>                                                                                          |
| [<span data-ttu-id="aa1f0-139">**ISWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-139">**ISWbemQualifierSet**</span></span>](swbemqualifierset.md)   | <span data-ttu-id="aa1f0-140">取得 [**ISWbemQualifier**](swbemqualifier.md) 物件集合的存取權。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-140">Gets access to a collection of [**ISWbemQualifier**](swbemqualifier.md) objects.</span></span>                                           |
| [<span data-ttu-id="aa1f0-141">**ISWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-141">**ISWbemSecurity**</span></span>](swbemsecurity.md)           | <span data-ttu-id="aa1f0-142">管理安全性設定，例如元件物件模型 (COM) 許可權、AuthenticationLevel 和 ImpersonationLevel。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-142">Manages security settings such as Component Object Model (COM) Privilege, AuthenticationLevel, and ImpersonationLevel.</span></span>      |
| [<span data-ttu-id="aa1f0-143">**ISWbemServices**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-143">**ISWbemServices**</span></span>](swbemservices.md)           | <span data-ttu-id="aa1f0-144">建立、更新及抓取實例或類別。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-144">Creates, updates, and retrieves instances or classes.</span></span>                                                                       |
| [<span data-ttu-id="aa1f0-145">**ISWbemSink**</span><span class="sxs-lookup"><span data-stu-id="aa1f0-145">**ISWbemSink**</span></span>](swbemsink.md)                   | <span data-ttu-id="aa1f0-146">接收用戶端應用程式非同步作業和事件通知的結果。</span><span class="sxs-lookup"><span data-stu-id="aa1f0-146">Receives the results of client application asynchronous operations and event notifications.</span></span>                                 |



 

 

 



