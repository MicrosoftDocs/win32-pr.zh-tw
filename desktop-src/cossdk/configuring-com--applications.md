---
description: COM + 應用程式基本上是一種宣告式的結構，可讓您設定任何數目的萬用群組件。 例如，您可以使用一般安全性原則來設定應用程式中的元件。
ms.assetid: 50039b30-1c91-4e93-9f23-873accb651cf
title: 設定 COM + 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16319baf7e34348751e9cafd0efcbd99906d0985
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973378"
---
# <a name="configuring-com-applications"></a><span data-ttu-id="19645-104">設定 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="19645-104">Configuring COM+ Applications</span></span>

<span data-ttu-id="19645-105">COM + 應用程式基本上是一種宣告式的結構，可讓您設定任何數目的萬用群組件。</span><span class="sxs-lookup"><span data-stu-id="19645-105">A COM+ application is essentially a declarative construct that enables you to configure any number of components in common.</span></span> <span data-ttu-id="19645-106">例如，您可以使用一般安全性原則來設定應用程式中的元件。</span><span class="sxs-lookup"><span data-stu-id="19645-106">For example, you can configure the components in an application with a common security policy.</span></span>

<span data-ttu-id="19645-107">在 COM + 應用程式的開發程式中，設定是不可或缺的一部分。</span><span class="sxs-lookup"><span data-stu-id="19645-107">Configuration is an essential part of the development process for COM+ applications.</span></span> <span data-ttu-id="19645-108">您如何設定應用程式，將決定 COM + 如何為其提供服務，以及在執行時如何運作。</span><span class="sxs-lookup"><span data-stu-id="19645-108">How you configure an application will determine how COM+ will provide services for it and how it behaves when running.</span></span>

<span data-ttu-id="19645-109">您可以使用 [元件服務] 系統管理工具或可編寫腳本的管理物件和介面（提供管理工具的基礎功能）來設定 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="19645-109">You can configure COM+ applications using either the Component Services administration tool or the scriptable administration objects and interfaces that provide the underlying functionality of the administration tool.</span></span> <span data-ttu-id="19645-110">如需執行腳本管理的詳細資訊，請參閱 [自動化 COM + 管理](automating-com--administration.md)。</span><span class="sxs-lookup"><span data-stu-id="19645-110">For details on performing scripted administration, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

<span data-ttu-id="19645-111">您可以在 COM + 應用程式內的下列層級設定元素：</span><span class="sxs-lookup"><span data-stu-id="19645-111">You can configure elements at the following levels within COM+ applications:</span></span>

-   [<span data-ttu-id="19645-112">應用層級設定</span><span class="sxs-lookup"><span data-stu-id="19645-112">Application-Level Settings</span></span>](#application-level-settings)
-   [<span data-ttu-id="19645-113">元件層級 (類別層級) 設定</span><span class="sxs-lookup"><span data-stu-id="19645-113">Component-Level (Class-Level) Settings</span></span>](#component-level-class-level-settings)
-   [<span data-ttu-id="19645-114">介面層級設定</span><span class="sxs-lookup"><span data-stu-id="19645-114">Interface-Level Setting</span></span>](#interface-level-setting)
-   [<span data-ttu-id="19645-115">方法層級設定</span><span class="sxs-lookup"><span data-stu-id="19645-115">Method-Level Setting</span></span>](#method-level-setting)
-   [<span data-ttu-id="19645-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="19645-116">Related topics</span></span>](#related-topics)

<span data-ttu-id="19645-117">您將元件安裝到應用程式的方式，可能會影響您如何進行設定。</span><span class="sxs-lookup"><span data-stu-id="19645-117">How you install components into an application can affect how you can configure them.</span></span> <span data-ttu-id="19645-118">您應該一律將元件安裝至 COM + 應用程式 (而不是將它們匯入) 。</span><span class="sxs-lookup"><span data-stu-id="19645-118">You should always install components into COM+ applications (as opposed to importing them).</span></span> <span data-ttu-id="19645-119">安裝元件會在 COM + 類別註冊資料庫中完整註冊它們，以及介面和類型程式庫 (RegDB) ，讓您可以進行設定。</span><span class="sxs-lookup"><span data-stu-id="19645-119">Installing components will fully register them, along with interfaces and type libraries, in the COM+ class registration database (RegDB) so that you can configure them.</span></span>

## <a name="application-level-settings"></a><span data-ttu-id="19645-120">Application-Level 設定</span><span class="sxs-lookup"><span data-stu-id="19645-120">Application-Level Settings</span></span>



| <span data-ttu-id="19645-121">屬性</span><span class="sxs-lookup"><span data-stu-id="19645-121">Attribute</span></span>                                                                                        | <span data-ttu-id="19645-122">描述</span><span class="sxs-lookup"><span data-stu-id="19645-122">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19645-123">啟用</span><span class="sxs-lookup"><span data-stu-id="19645-123">Activation</span></span>](context-activation.md)<br/>                                                  | <span data-ttu-id="19645-124">指定應用程式類型： [伺服器應用程式] 或 [程式庫應用程式]。</span><span class="sxs-lookup"><span data-stu-id="19645-124">Specifies application type: either server application or library application.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="19645-125">啟用存取檢查</span><span class="sxs-lookup"><span data-stu-id="19645-125">Enabling access checks</span></span>](enabling-access-checks-for-an-application.md)<br/>               | <span data-ttu-id="19645-126">開啟和關閉安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="19645-126">Turns security checking on and off.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="19645-127">安全性層級</span><span class="sxs-lookup"><span data-stu-id="19645-127">Security level</span></span>](setting-a-security-level-for-access-checks.md)<br/>                      | <span data-ttu-id="19645-128">指定將在進程層級執行存取檢查， (從角色) 或同時在進程和元件層級產生的存取檢查層級 (完整的角色型安全性) 。</span><span class="sxs-lookup"><span data-stu-id="19645-128">Specifies that access checks will be performed at the process level (access-checking levels generated from roles) or both at process and at component levels (full role-based security).</span></span><br/> |
| [<span data-ttu-id="19645-129">驗證等級</span><span class="sxs-lookup"><span data-stu-id="19645-129">Authentication level</span></span>](setting-an-authentication-level-for-a-server-application.md)<br/>  | <span data-ttu-id="19645-130">設定用於呼叫應用程式的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="19645-130">Sets the authentication level used on calls into the application.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="19645-131">模擬等級</span><span class="sxs-lookup"><span data-stu-id="19645-131">Impersonation level</span></span>](setting-an-impersonation-level.md)<br/>                             | <span data-ttu-id="19645-132">設定呼叫其他應用程式時所使用的模擬等級。</span><span class="sxs-lookup"><span data-stu-id="19645-132">Sets the impersonation level used on calls to other applications.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="19645-133">排隊</span><span class="sxs-lookup"><span data-stu-id="19645-133">Queuing</span></span>](creating-queuable-components.md)<br/>                                           | <span data-ttu-id="19645-134">指定應用程式元件將使用佇列服務。</span><span class="sxs-lookup"><span data-stu-id="19645-134">Specifies that application components will use queuing services.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="19645-135">啟用 CRM</span><span class="sxs-lookup"><span data-stu-id="19645-135">Enable CRM</span></span>](configuring-com--crm-components.md)<br/>                                     | <span data-ttu-id="19645-136">啟用補償資源管理員的使用。</span><span class="sxs-lookup"><span data-stu-id="19645-136">Enables use of Compensating Resource Managers.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="19645-137">以服務形式執行應用程式</span><span class="sxs-lookup"><span data-stu-id="19645-137">Run application as a service</span></span>](com--applications-running-as-service-applications.md)<br/> | <span data-ttu-id="19645-138">將 COM + 伺服器應用程式設定和實作為 NT 服務。</span><span class="sxs-lookup"><span data-stu-id="19645-138">Configures and implements a COM+ server application as an NT service.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="19645-139">COM + SOAP 服務</span><span class="sxs-lookup"><span data-stu-id="19645-139">COM+ SOAP service</span></span>](com--soap-service.md)<br/>                                            | <span data-ttu-id="19645-140">將 COM + 應用程式公開為 XML web service。</span><span class="sxs-lookup"><span data-stu-id="19645-140">Exposes a COM+ application as an XML web service.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="19645-141">應用程式共用</span><span class="sxs-lookup"><span data-stu-id="19645-141">Application pooling</span></span>](com--application-pooling.md)<br/>                                   | <span data-ttu-id="19645-142">為單一執行緒進程新增擴充性，並與 COM + 應用程式回收服務整合。</span><span class="sxs-lookup"><span data-stu-id="19645-142">Adds scalability for single-threaded processes and integrates with the COM+ Application Recycling service.</span></span><br/>                                                                               |
| [<span data-ttu-id="19645-143">應用程式回收</span><span class="sxs-lookup"><span data-stu-id="19645-143">Application recycling</span></span>](com--application-recycling.md)<br/>                               | <span data-ttu-id="19645-144">藉由正常關閉與應用程式相關聯的進程並重新啟動，來提高應用程式穩定性。</span><span class="sxs-lookup"><span data-stu-id="19645-144">Increases application stability by gracefully shutting down a process associated with an application and restarting it.</span></span><br/>                                                                  |
| [<span data-ttu-id="19645-145">進程傾印</span><span class="sxs-lookup"><span data-stu-id="19645-145">Process dumping</span></span>](what-s-new-in-com--1-5.md)<br/>                                         | <span data-ttu-id="19645-146">傾印整個進程的狀態，而不終止它，以供進行調試。</span><span class="sxs-lookup"><span data-stu-id="19645-146">Dumps the entire state of a process without terminating it, for debugging purposes.</span></span><br/>                                                                                                      |
| <span data-ttu-id="19645-147">伺服器進程關機</span><span class="sxs-lookup"><span data-stu-id="19645-147">Server process shutdown</span></span><br/>                                                               | <span data-ttu-id="19645-148">在指定的閒置期限之後關閉進程。</span><span class="sxs-lookup"><span data-stu-id="19645-148">Shuts down a process after a specified idle period.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="19645-149">權限</span><span class="sxs-lookup"><span data-stu-id="19645-149">Permissions</span></span><br/>                                                                           | <span data-ttu-id="19645-150">停用設定的變更，包括刪除。</span><span class="sxs-lookup"><span data-stu-id="19645-150">Disables changes to configuration settings, including deletion.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="19645-151">安全性身分識別</span><span class="sxs-lookup"><span data-stu-id="19645-151">Security identity</span></span><br/>                                                                     | <span data-ttu-id="19645-152">指定應用程式執行時所用的身分識別。</span><span class="sxs-lookup"><span data-stu-id="19645-152">Specifies the identity under which the application runs.</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="19645-153">在偵錯工具中啟動</span><span class="sxs-lookup"><span data-stu-id="19645-153">Launch in debugger</span></span><br/>                                                                    | <span data-ttu-id="19645-154">指定將在偵錯工具中啟動應用程式，並使用使用者指定的命令列設定。</span><span class="sxs-lookup"><span data-stu-id="19645-154">Specifies that the application will be launched in a debugger, with user-specified command-line settings.</span></span><br/>                                                                                |
| <span data-ttu-id="19645-155">啟用 3GB 支援</span><span class="sxs-lookup"><span data-stu-id="19645-155">Enable 3GB support</span></span><br/>                                                                    | <span data-ttu-id="19645-156">啟用擴充進程記憶體位址空間的使用。</span><span class="sxs-lookup"><span data-stu-id="19645-156">Enables use of extended process memory address space.</span></span><br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a><span data-ttu-id="19645-157">Component-Level (類別層級) 設定</span><span class="sxs-lookup"><span data-stu-id="19645-157">Component-Level (Class-Level) Settings</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="19645-158">屬性</span><span class="sxs-lookup"><span data-stu-id="19645-158">Attribute</span></span></th>
<th><span data-ttu-id="19645-159">描述</span><span class="sxs-lookup"><span data-stu-id="19645-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19645-160"><a href="configuring-transactions.md">交易</a></span><span class="sxs-lookup"><span data-stu-id="19645-160"><a href="configuring-transactions.md">Transactions</a></span></span><br/></td>
<td><span data-ttu-id="19645-161">設定停用、不支援、支援、必要或需要新的自動交易需求。</span><span class="sxs-lookup"><span data-stu-id="19645-161">Sets automatic transaction requirements Disabled, Not Supported, Supported, Required, or Requires New.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19645-162"><a href="setting-the-synchronization-attribute.md">同步處理</a></span><span class="sxs-lookup"><span data-stu-id="19645-162"><a href="setting-the-synchronization-attribute.md">Synchronization</a></span></span><br/></td>
<td><span data-ttu-id="19645-163">設定停用、不支援、支援、必要或需要新的同步處理需求。</span><span class="sxs-lookup"><span data-stu-id="19645-163">Sets synchronization requirements Disabled, Not Supported, Supported, Required, or Requires New.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19645-164"><a href="enabling-jit-activation-for-a-component.md">JIT 啟用</a></span><span class="sxs-lookup"><span data-stu-id="19645-164"><a href="enabling-jit-activation-for-a-component.md">JIT Activation</a></span></span><br/></td>
<td><span data-ttu-id="19645-165">啟用即時啟用。</span><span class="sxs-lookup"><span data-stu-id="19645-165">Enables just-in-time activation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19645-166"><a href="configuring-a-component-to-be-pooled.md">物件集區</a></span><span class="sxs-lookup"><span data-stu-id="19645-166"><a href="configuring-a-component-to-be-pooled.md">Object pooling</a></span></span><br/></td>
<td><span data-ttu-id="19645-167">啟用物件共用。</span><span class="sxs-lookup"><span data-stu-id="19645-167">Enables object pooling.</span></span> <span data-ttu-id="19645-168">最小和最大集區大小和物件超時值都是可設定的。</span><span class="sxs-lookup"><span data-stu-id="19645-168">Minimum and maximum pool size and object time-out values are configurable.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19645-169"><a href="specifying-an-object-constructor-string-for-a-component.md">物件結構</a></span><span class="sxs-lookup"><span data-stu-id="19645-169"><a href="specifying-an-object-constructor-string-for-a-component.md">Object construction</a></span></span><br/></td>
<td><span data-ttu-id="19645-170">使用系統管理指定的函式字串來啟用參數化物件結構。</span><span class="sxs-lookup"><span data-stu-id="19645-170">Enables parameterized object construction with an administratively specified constructor string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="19645-171">不應使用此函式字串來儲存安全性機密資訊。</span><span class="sxs-lookup"><span data-stu-id="19645-171">The constructor string should not be used to store security-sensitive information.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19645-172"><a href="enabling-access-checks-at-the-component-level.md">元件層級存取檢查</a></span><span class="sxs-lookup"><span data-stu-id="19645-172"><a href="enabling-access-checks-at-the-component-level.md">Component-level access checks</a></span></span><br/></td>
<td><span data-ttu-id="19645-173">開啟或關閉元件層級以角色為基礎的安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="19645-173">Turns on or off component-level role-based security checking.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19645-174"><a href="assigning-roles-to-components--interfaces--or-methods.md">宣告式角色指派</a></span><span class="sxs-lookup"><span data-stu-id="19645-174"><a href="assigning-roles-to-components--interfaces--or-methods.md">Declarative role assignment</a></span></span><br/></td>
<td><span data-ttu-id="19645-175">啟用將角色明確指派給元件。</span><span class="sxs-lookup"><span data-stu-id="19645-175">Enables explicit assignment of roles to the component.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19645-176"><a href="persistent-client-side-failures.md">佇列例外狀況類別</a></span><span class="sxs-lookup"><span data-stu-id="19645-176"><a href="persistent-client-side-failures.md">Queuing exception class</a></span></span><br/></td>
<td><span data-ttu-id="19645-177">表示處理用戶端失敗的例外狀況類別。</span><span class="sxs-lookup"><span data-stu-id="19645-177">Indicates an exception class for handling client-side failures.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19645-178"><a href="com--instrumentation-concepts.md">檢測事件和統計資料</a></span><span class="sxs-lookup"><span data-stu-id="19645-178"><a href="com--instrumentation-concepts.md">Instrumentation events and statistics</a></span></span><br/></td>
<td><span data-ttu-id="19645-179">啟用詳細的系統事件和物件統計資料包告。</span><span class="sxs-lookup"><span data-stu-id="19645-179">Enables detailed system event and object statistics reporting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19645-180"><a href="context-activation.md">啟用內容</a></span><span class="sxs-lookup"><span data-stu-id="19645-180"><a href="context-activation.md">Activation context</a></span></span><br/></td>
<td><span data-ttu-id="19645-181">啟用在呼叫端的內容或預設內容中強制啟用物件。</span><span class="sxs-lookup"><span data-stu-id="19645-181">Enables forced activation of an object in the caller's context or default context.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19645-182"><a href="what-s-new-in-com--1-5.md">建立私用元件</a></span><span class="sxs-lookup"><span data-stu-id="19645-182"><a href="what-s-new-in-com--1-5.md">Creating private components</a></span></span><br/></td>
<td><span data-ttu-id="19645-183">將元件標示為私用應用程式。</span><span class="sxs-lookup"><span data-stu-id="19645-183">Marks component as private to the application.</span></span> <span data-ttu-id="19645-184">私用元件只能由相同應用程式中的其他元件來查看和啟用。</span><span class="sxs-lookup"><span data-stu-id="19645-184">A private component can be seen and activated only by other components in the same application.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="interface-level-setting"></a><span data-ttu-id="19645-185">Interface-Level 設定</span><span class="sxs-lookup"><span data-stu-id="19645-185">Interface-Level Setting</span></span>



| <span data-ttu-id="19645-186">屬性</span><span class="sxs-lookup"><span data-stu-id="19645-186">Attribute</span></span>                                                                                           | <span data-ttu-id="19645-187">描述</span><span class="sxs-lookup"><span data-stu-id="19645-187">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19645-188">已排入佇列</span><span class="sxs-lookup"><span data-stu-id="19645-188">Queued</span></span>](creating-queuable-components.md)<br/>                                               | <span data-ttu-id="19645-189">表示 IDL 中定義的 queuable 介面。</span><span class="sxs-lookup"><span data-stu-id="19645-189">Indicates a queuable interface, defined in IDL.</span></span><br/>                                                                       |
| [<span data-ttu-id="19645-190">宣告式角色指派</span><span class="sxs-lookup"><span data-stu-id="19645-190">Declarative role assignment</span></span>](assigning-roles-to-components--interfaces--or-methods.md)<br/> | <span data-ttu-id="19645-191">可以明確地將角色指派給介面，以及從元件層級隱含繼承角色。</span><span class="sxs-lookup"><span data-stu-id="19645-191">Enables explicit assignment of roles to the interface as well as implicitly inherited roles from the component level.</span></span><br/> |



 

## <a name="method-level-setting"></a><span data-ttu-id="19645-192">Method-Level 設定</span><span class="sxs-lookup"><span data-stu-id="19645-192">Method-Level Setting</span></span>



| <span data-ttu-id="19645-193">屬性</span><span class="sxs-lookup"><span data-stu-id="19645-193">Attribute</span></span>                                                                                           | <span data-ttu-id="19645-194">描述</span><span class="sxs-lookup"><span data-stu-id="19645-194">Description</span></span>                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19645-195">自動完成</span><span class="sxs-lookup"><span data-stu-id="19645-195">Auto-done</span></span>](enabling-auto-done-for-a-method.md)<br/>                                         | <span data-ttu-id="19645-196">自動停用方法傳回的物件和交易中的投票。</span><span class="sxs-lookup"><span data-stu-id="19645-196">Automatically deactivates object on method return and votes in transaction.</span></span><br/>                                                       |
| [<span data-ttu-id="19645-197">宣告式角色指派</span><span class="sxs-lookup"><span data-stu-id="19645-197">Declarative role assignment</span></span>](assigning-roles-to-components--interfaces--or-methods.md)<br/> | <span data-ttu-id="19645-198">可以明確地將角色指派給方法，以及從介面和元件層級隱含繼承角色。</span><span class="sxs-lookup"><span data-stu-id="19645-198">Enables explicit assignment of roles to the method as well as implicitly inherited roles from the interface and component levels.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="19645-199">相關主題</span><span class="sxs-lookup"><span data-stu-id="19645-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19645-200">自動化 COM + 管理</span><span class="sxs-lookup"><span data-stu-id="19645-200">Automating COM+ Administration</span></span>](automating-com--administration.md)
</dt> <dt>

[<span data-ttu-id="19645-201">建立 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="19645-201">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="19645-202">部署 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="19645-202">Deploying COM+ Applications</span></span>](deploying-com--applications.md)
</dt> </dl>

 

 




