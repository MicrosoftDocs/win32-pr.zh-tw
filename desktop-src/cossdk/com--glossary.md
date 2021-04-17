---
description: 詞彙頁面
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26a72de1-24bc-41e6-8d41-61d45f581e51
title: COM + 詞彙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5a6cb30529cd8b97b8cf11316347d68003e32c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468165"
---
# <a name="com-glossary"></a><span data-ttu-id="9ee82-103">COM + 詞彙</span><span class="sxs-lookup"><span data-stu-id="9ee82-103">COM+ Glossary</span></span>

<dl> <dt>

<span data-ttu-id="9ee82-104"><span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**存取權杖**</span><span class="sxs-lookup"><span data-stu-id="9ee82-104"><span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**access token**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-105">物件，描述進程或執行緒的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="9ee82-105">An object that describes the security context of a process or thread.</span></span> <span data-ttu-id="9ee82-106">權杖中的資訊包括與進程或執行緒相關聯之使用者帳戶的身分識別和許可權。</span><span class="sxs-lookup"><span data-stu-id="9ee82-106">The information in a token includes the identity and privileges of the user account associated with the process or thread.</span></span> <span data-ttu-id="9ee82-107">當使用者登入時，系統會將使用者的密碼與儲存在安全性資料庫中的資訊進行比較，以驗證該使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="9ee82-107">When a user logs on, the system verifies the user's password by comparing it with information stored in a security database.</span></span> <span data-ttu-id="9ee82-108">如果密碼經過驗證，系統會產生存取權杖。</span><span class="sxs-lookup"><span data-stu-id="9ee82-108">If the password is authenticated, the system produces an access token.</span></span> <span data-ttu-id="9ee82-109">代表此使用者執行的每個處理常式都有此存取權杖的複本。</span><span class="sxs-lookup"><span data-stu-id="9ee82-109">Every process executed on behalf of this user has a copy of this access token.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-110"><span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**ACID 屬性**</span><span class="sxs-lookup"><span data-stu-id="9ee82-110"><span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**ACID properties**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-111">以不可部分完成、一致、隔離且持久的交易處理先鋒創造的縮寫。</span><span class="sxs-lookup"><span data-stu-id="9ee82-111">Acronym coined by transaction processing pioneers for atomic, consistent, isolated, and durable.</span></span> <span data-ttu-id="9ee82-112">這些屬性可確保可預測的行為，將交易的角色強化為全或無的主張，其設計目的是為了在分散式環境中提供一致且可預測的結果，而且可能發生獨立失敗。</span><span class="sxs-lookup"><span data-stu-id="9ee82-112">These properties ensure predictable behavior, reinforcing the role of transactions as all-or-none propositions designed to provide consistent and predictable results in a distributed environment when independent failures can occur.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-113"><span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**啟動**</span><span class="sxs-lookup"><span data-stu-id="9ee82-113"><span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**activation**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-114">導致建立 COM 物件，以及將有效指標傳回給該物件介面的事件鏈。</span><span class="sxs-lookup"><span data-stu-id="9ee82-114">The chain of events that results in the creation of a COM object and the return of a valid pointer to an interface on that object.</span></span> <span data-ttu-id="9ee82-115">在 COM + 中，物件會在其自己的內容中啟動，或在其建立者 (已要求啟始物件) 的物件中啟用。</span><span class="sxs-lookup"><span data-stu-id="9ee82-115">In COM+, an object gets activated either in its own context or in that of its creator (an object that has requested the object being activated).</span></span> <span data-ttu-id="9ee82-116">COM + 服務會根據物件的設定，依賴適當的物件啟用。</span><span class="sxs-lookup"><span data-stu-id="9ee82-116">COM+ services rely on appropriate activation of an object based on the object's configuration.</span></span> <span data-ttu-id="9ee82-117">在啟用過程中，系統會判斷物件執行所在的內容、初始化內容屬性、檢查存取權限，以及建立安全性身分識別。</span><span class="sxs-lookup"><span data-stu-id="9ee82-117">In the course of activation, the system determines the context in which the object runs, initializes the context properties, checks access permissions, and establishes a security identity.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-118"><span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**啟用安全性**</span><span class="sxs-lookup"><span data-stu-id="9ee82-118"><span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**activation security**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-119">一種安全性保護形式，可決定誰可以啟動伺服器。</span><span class="sxs-lookup"><span data-stu-id="9ee82-119">A form of security protection that determines who can launch a server.</span></span> <span data-ttu-id="9ee82-120">「服務控制管理員」會自動套用「啟用安全性」 (特定電腦的 SCM) 。</span><span class="sxs-lookup"><span data-stu-id="9ee82-120">Activation security is automatically applied by the Service Control Manager (SCM) of a particular computer.</span></span> <span data-ttu-id="9ee82-121">當收到來自用戶端的要求以啟始物件時，SCM 會根據儲存在登錄中的啟用安全性資訊來檢查要求。</span><span class="sxs-lookup"><span data-stu-id="9ee82-121">Upon receipt of a request from a client to activate an object, the SCM checks the request against activation-security information stored within its registry.</span></span> <span data-ttu-id="9ee82-122">也會檢查是否有相同電腦啟用的啟用安全性。</span><span class="sxs-lookup"><span data-stu-id="9ee82-122">Activation security is also checked for same-computer activations.</span></span> <span data-ttu-id="9ee82-123">也稱為 *啟動安全性*。</span><span class="sxs-lookup"><span data-stu-id="9ee82-123">Also called *launch security*.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-124"><span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**啟用類型**</span><span class="sxs-lookup"><span data-stu-id="9ee82-124"><span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**activation type**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-125">COM + 應用程式的啟動類別) ，指出應用程式是否會在其用戶端的進程空間中執行 (，取決於它是程式庫或伺服器應用程式，以及應用程式是否以服務的形式執行。</span><span class="sxs-lookup"><span data-stu-id="9ee82-125">Activation category for a COM+ application that indicates whether the application runs in or out of its client's process space (depending on whether it's a library or server application, respectively) as well as whether the application runs as a service.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-126"><span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**活動**</span><span class="sxs-lookup"><span data-stu-id="9ee82-126"><span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**activity**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-127">在 COM + 中，包含一或多個交易的邏輯執行緒，並包含組成 COM + 應用程式的元件集合。</span><span class="sxs-lookup"><span data-stu-id="9ee82-127">In COM+, a logical thread comprising one or more transactions and containing a collection of components that are grouped into a COM+ application.</span></span> <span data-ttu-id="9ee82-128">每個 COM 物件都屬於一個活動。</span><span class="sxs-lookup"><span data-stu-id="9ee82-128">Every COM object belongs to one activity.</span></span> <span data-ttu-id="9ee82-129">物件與活動之間的關聯無法變更。</span><span class="sxs-lookup"><span data-stu-id="9ee82-129">The association between an object and an activity cannot be changed.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-130"><span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**單元模型進程**</span><span class="sxs-lookup"><span data-stu-id="9ee82-130"><span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**apartment model process**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-131">具有兩個或多個單一執行緒單元且沒有多執行緒單元的進程。</span><span class="sxs-lookup"><span data-stu-id="9ee82-131">A process that has two or more single-threaded apartments and no multithreaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-132"><span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**應用程式 proxy**</span><span class="sxs-lookup"><span data-stu-id="9ee82-132"><span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**application proxy**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-133">一組檔案，其中包含可讓用戶端從遠端存取 COM + 伺服器應用程式的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="9ee82-133">A set of files containing registration information that allows a client to remotely access a COM+ server application.</span></span> <span data-ttu-id="9ee82-134">在用戶端電腦上安裝時，應用程式 proxy 檔案會將伺服器應用程式的相關資訊寫入用戶端電腦。然後，用戶端可以從遠端存取服務器應用程式。</span><span class="sxs-lookup"><span data-stu-id="9ee82-134">When installed on a client computer, an application proxy file writes information about the server application to the client computer; the client can then remotely access the server application.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-135"><span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**認證**</span><span class="sxs-lookup"><span data-stu-id="9ee82-135"><span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**authentication**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-136">判斷應用程式的呼叫者實際上是誰指出的安全性程式，就是驗證身分識別宣告的真實性。</span><span class="sxs-lookup"><span data-stu-id="9ee82-136">The security process of determining that a caller of an application is actually who it says it is—verifying the authenticity of an identity claim.</span></span> <span data-ttu-id="9ee82-137">針對 COM + 應用程式，可以開啟並設定系統管理員的驗證，之後它會以透明的方式在應用程式中運作。</span><span class="sxs-lookup"><span data-stu-id="9ee82-137">For COM+ applications, authentication can be turned on and configured administratively, after which it works transparently to the application.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-138"><span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**授權**</span><span class="sxs-lookup"><span data-stu-id="9ee82-138"><span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**authorization**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-139">判斷應用程式的呼叫端是否已獲授權可進行要求之動作的安全性程式。</span><span class="sxs-lookup"><span data-stu-id="9ee82-139">The security process of determining whether a caller of an application is authorized to do what it is asking to do.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-140"><span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**快取 resource manager**</span><span class="sxs-lookup"><span data-stu-id="9ee82-140"><span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**caching resource manager**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-141">資源管理員，可作為另一個 resource manager 的前端，並在本機快取資訊，降低存取基礎資源的成本。</span><span class="sxs-lookup"><span data-stu-id="9ee82-141">A resource manager that acts as a front-end to another resource manager and that caches information locally, reducing the cost of accessing the underlying resource.</span></span> <span data-ttu-id="9ee82-142">不同于傳統的資源管理員，快取資源管理員不會參與復原，因為它永遠不會永久儲存基礎資料。</span><span class="sxs-lookup"><span data-stu-id="9ee82-142">Unlike a conventional resource manager, a caching resource manager does not participate in recovery because it never permanently stores the underlying data.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-143"><span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**呼叫安全性**</span><span class="sxs-lookup"><span data-stu-id="9ee82-143"><span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**call security**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-144">一種安全性保護形式，可在伺服器啟動之後協助控制伺服器物件方法的存取。</span><span class="sxs-lookup"><span data-stu-id="9ee82-144">A form of security protection that helps control access to a server object's methods after a server has been launched.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-145"><span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**COM)  (類別**</span><span class="sxs-lookup"><span data-stu-id="9ee82-145"><span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**class (COM)**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-146">一或多個介面的已命名、具體實作為。</span><span class="sxs-lookup"><span data-stu-id="9ee82-146">A named, concrete implementation of one or more interfaces.</span></span> <span data-ttu-id="9ee82-147">COM 類別是以 CLSID 識別，有時也是 ProgID。</span><span class="sxs-lookup"><span data-stu-id="9ee82-147">A COM class is identified by a CLSID and, sometimes, a ProgID.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-148"><span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**隱形**</span><span class="sxs-lookup"><span data-stu-id="9ee82-148"><span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-149">伺服器在代表用戶端進行呼叫時，能夠遮罩自己的身分識別。</span><span class="sxs-lookup"><span data-stu-id="9ee82-149">A server's ability to mask its own identity when making calls on a client's behalf.</span></span> <span data-ttu-id="9ee82-150">啟用「遮蓋」時，您可以透過用戶端的身分識別，在模擬用戶端的伺服器上進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="9ee82-150">When cloaking is enabled, calls made by the server impersonating the client can be made under the client's identity.</span></span> <span data-ttu-id="9ee82-151">停用遮蓋時，伺服器的呼叫會在伺服器的身分識別下進行。</span><span class="sxs-lookup"><span data-stu-id="9ee82-151">When cloaking is disabled, calls by the server will be made under the server's identity.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-152"><span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**COM + 應用程式**</span><span class="sxs-lookup"><span data-stu-id="9ee82-152"><span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**COM+ application**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-153">元件服務的管理和安全性主要單位。</span><span class="sxs-lookup"><span data-stu-id="9ee82-153">The primary unit of administration and security for Component Services.</span></span> <span data-ttu-id="9ee82-154">COM + 應用程式是一組 COM 元件，通常會執行相關的函數。</span><span class="sxs-lookup"><span data-stu-id="9ee82-154">A COM+ application is a group of COM components that, generally, perform related functions.</span></span> <span data-ttu-id="9ee82-155">這些元件會進一步包含 COM 介面和方法。</span><span class="sxs-lookup"><span data-stu-id="9ee82-155">These components further consist of COM interfaces and methods.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-156"><span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**COM + 應用程式共用**</span><span class="sxs-lookup"><span data-stu-id="9ee82-156"><span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**COM+ Application Pooling**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-157">一種元件服務功能，可讓單一執行緒進程進行調整，也可以協助您藉由提供可處理啟用的其他執行中進程，從單一進程中的失敗中復原。</span><span class="sxs-lookup"><span data-stu-id="9ee82-157">A Component Services feature that allows single-threaded processes to scale and can also help you recover from failures in single processes by providing other running processes able to handle activations.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-158"><span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**COM + 應用程式回收**</span><span class="sxs-lookup"><span data-stu-id="9ee82-158"><span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**COM+ Application Recycling**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-159">元件服務功能，可讓您正常關閉與應用程式相關聯的程式並重新啟動，以大幅提升應用程式的整體穩定性。</span><span class="sxs-lookup"><span data-stu-id="9ee82-159">A Component Services feature that significantly increases the overall stability of your applications by allowing you to gracefully shut down a process associated with an application and restart it.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-160"><span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**COM + 類別目錄**</span><span class="sxs-lookup"><span data-stu-id="9ee82-160"><span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**COM+ catalog**</span></span> 
</dt> <dd>

<span data-ttu-id="9ee82-161">保存 COM + 設定資料的資料存放區。</span><span class="sxs-lookup"><span data-stu-id="9ee82-161">The data store that holds COM+ configuration data.</span></span> <span data-ttu-id="9ee82-162">COM + 系統管理工作的效能需要讀取和寫入儲存在目錄中的資料。</span><span class="sxs-lookup"><span data-stu-id="9ee82-162">Performance of COM+ administration tasks requires reading and writing data stored in the catalog.</span></span> <span data-ttu-id="9ee82-163">您只能透過 [元件服務] 系統管理工具或透過 COMAdmin 程式庫來存取目錄。</span><span class="sxs-lookup"><span data-stu-id="9ee82-163">The catalog can be accessed only through the Component Services administrative tool or through the COMAdmin library.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-164"><span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**COM + 事件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-164"><span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**COM+ Events**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-165">COM + 事件會比對發行者和訂閱者，並透過鬆散結合的事件系統來連接。</span><span class="sxs-lookup"><span data-stu-id="9ee82-165">COM+ Events matches and connects publishers and subscribers through a loosely coupled events system.</span></span> <span data-ttu-id="9ee82-166">發行者會進行方法呼叫來起始事件，而訂閱者會透過事件系統（而不是直接從發行者）接收這些呼叫。</span><span class="sxs-lookup"><span data-stu-id="9ee82-166">A publisher makes the method call to initiate an event, and a subscriber receives these calls through the event system rather than directly from the publisher.</span></span> <span data-ttu-id="9ee82-167">COM + 事件服務會維護接收呼叫的有興趣的訂閱者清單，並在不需要發行者知識的情況下指示這些呼叫。</span><span class="sxs-lookup"><span data-stu-id="9ee82-167">The COM+ Events service maintains the list of interested subscribers who receive the calls and directs those calls without requiring the knowledge of the publisher.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-168"><span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**COM + 程式庫應用程式**</span><span class="sxs-lookup"><span data-stu-id="9ee82-168"><span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**COM+ library application**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-169">COM + 應用程式，會在建立該應用程式的用戶端進程中執行。</span><span class="sxs-lookup"><span data-stu-id="9ee82-169">A COM+ application that runs in the process of the client that creates it.</span></span> <span data-ttu-id="9ee82-170">程式庫應用程式可以使用以角色為基礎的安全性，但不支援遠端存取或已排入佇列的元件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-170">Library applications can use role-based security but do not support remote access or queued components.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-171"><span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**COM + 物件共用**</span><span class="sxs-lookup"><span data-stu-id="9ee82-171"><span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**COM+ Object Pooling**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-172">COM + 提供的自動服務，可讓您將元件的實例設定為在集區中保持作用中狀態，以供任何要求元件的用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="9ee82-172">An automatic service provided by COM+ that enables you to configure a component to have instances of itself kept active in a pool, ready to be used by any client that requests the component.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-173"><span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**COM + 磁碟分割**</span><span class="sxs-lookup"><span data-stu-id="9ee82-173"><span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**COM+ Partitions**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-174">一種 COM + 服務，可在單一電腦上建立應用程式的個別執行空間。</span><span class="sxs-lookup"><span data-stu-id="9ee82-174">A COM+ service that enables, on a single computer, the creation of separate execution spaces for applications.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-175"><span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**COM + 分割集**</span><span class="sxs-lookup"><span data-stu-id="9ee82-175"><span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**COM+ partition sets**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-176">在 Active Directory 中對應至特定使用者識別碼的 COM + 分割群組。</span><span class="sxs-lookup"><span data-stu-id="9ee82-176">A group of COM+ partitions that is mapped to a particular user ID in Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-177"><span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**COM + 佇列元件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-177"><span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**COM+ Queued Components**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-178">以 Microsoft Message Queuing 為基礎的 COM + 服務，可提供簡單的方法，以非同步方式叫用和執行元件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-178">A COM+ service, based on Microsoft Message Queuing, that provides an easy way to invoke and execute components asynchronously.</span></span> <span data-ttu-id="9ee82-179">訊息處理可能會發生，而不考慮傳送者或接收者的可用性或可存取性。</span><span class="sxs-lookup"><span data-stu-id="9ee82-179">Message processing can occur without regard to the availability or accessibility of either the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-180"><span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**COM + 伺服器應用程式**</span><span class="sxs-lookup"><span data-stu-id="9ee82-180"><span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**COM+ server application**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-181">在其本身的進程中執行的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="9ee82-181">A COM+ application that runs in its own process.</span></span> <span data-ttu-id="9ee82-182">伺服器應用程式可支援所有 COM + 服務。</span><span class="sxs-lookup"><span data-stu-id="9ee82-182">Server applications can support all COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-183"><span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**COM + SOAP**</span><span class="sxs-lookup"><span data-stu-id="9ee82-183"><span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**COM+ SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-184">元件服務功能，可讓您將 COM + 應用程式公開為 XML web service。</span><span class="sxs-lookup"><span data-stu-id="9ee82-184">A Component Services feature that allows you to expose a COM+ application as an XML web service.</span></span> <span data-ttu-id="9ee82-185">COM + SOAP 也可讓您使用 XML web service 做為 COM 元件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-185">COM+ SOAP also enables you to use an XML web service as a COM component.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-186"><span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**COM 元件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-186"><span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**COM component**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-187">程式碼的二進位單位，其中包含封裝和註冊程式碼，並且會建立 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-187">A binary unit of code that includes packaging and registration code and that creates COM objects.</span></span> <span data-ttu-id="9ee82-188">所有 COM + 應用程式都是由一或多個 COM 元件所組成。</span><span class="sxs-lookup"><span data-stu-id="9ee82-188">All COM+ applications consist of one or more COM components.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-189"><span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**認可樹狀結構**</span><span class="sxs-lookup"><span data-stu-id="9ee82-189"><span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**commit tree**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-190">在分散式交易系統中，交易的概念表示，會根據參與分散式交易的個別交易管理員之間的階層式關聯性而定。</span><span class="sxs-lookup"><span data-stu-id="9ee82-190">In a distributed transaction system, the conceptual representation of a transaction as based on the hierarchical relationships between individual transaction managers participating in a distributed transaction.</span></span> <span data-ttu-id="9ee82-191">包含在該階層中的是與交易管理員相關聯的已登記資源管理員。</span><span class="sxs-lookup"><span data-stu-id="9ee82-191">Included in that hierarchy are the enlisted resource managers associated with the transaction managers.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-192"><span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**COM 物件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-192"><span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**COM object**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-193">在 COM 程式設計模型中，程式設計結構會同時封裝資料和功能，而這些資料和功能是以單一單位來定義和配置，而只有公用存取是透過程式設計結構的介面。</span><span class="sxs-lookup"><span data-stu-id="9ee82-193">In the COM programming model, a programming structure encapsulating both data and functionality, which are defined and allocated as a single unit and for which the only public access is through the programming structure's interfaces.</span></span> <span data-ttu-id="9ee82-194">COM 物件至少必須支援 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) 介面，此介面會在使用時維持物件的存在，並提供物件其他介面的存取權。</span><span class="sxs-lookup"><span data-stu-id="9ee82-194">A COM object must support, at a minimum, the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface, which maintains the object's existence while it is being used and provides access to the object's other interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-195"><span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Resource Manager (CRM) 補償**</span><span class="sxs-lookup"><span data-stu-id="9ee82-195"><span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Compensating Resource Manager (CRM)**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-196">一種 COM + 功能，可讓非交易式資源參與具有 Microsoft Distributed Transaction Coordinator (DTC) 的兩階段認可交易。</span><span class="sxs-lookup"><span data-stu-id="9ee82-196">A COM+ feature that enables non-transactional resources to participate in a two-phase commit transaction with the Microsoft Distributed Transaction Coordinator (DTC).</span></span> <span data-ttu-id="9ee82-197">一般而言，Crm 並不提供完整資源管理員的隔離功能，但會寫入記錄檔，以提供交易式不可部分完成性和持久性。</span><span class="sxs-lookup"><span data-stu-id="9ee82-197">Typically, CRMs do not provide the isolation capabilities of full resource managers, but they do provide transactional atomicity and durability by writing to a log.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-198"><span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**元件服務系統管理工具**</span><span class="sxs-lookup"><span data-stu-id="9ee82-198"><span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Component Services administrative tool**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-199">使用者介面嵌入式管理單元，可讓系統管理員和開發人員建立、設定和維護 COM + 應用程式，以及管理分散式交易和記憶體常駐資料庫。</span><span class="sxs-lookup"><span data-stu-id="9ee82-199">A user-interface snap-in through which administrators and developers can create, configure, and maintain COM+ applications, as well as administer distributed transactions and memory-resident databases.</span></span> <span data-ttu-id="9ee82-200">[元件服務] 系統管理工具也可以用來在安裝工具的電腦上，用來查看系統事件及管理本機系統服務。</span><span class="sxs-lookup"><span data-stu-id="9ee82-200">The Component Services administrative tool can also be used to view system events and manage system services local to the computer on which the tool is installed.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-201"><span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**概念模型**</span><span class="sxs-lookup"><span data-stu-id="9ee82-201"><span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**conceptual model**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-202">COM + 應用程式設計階段的第一個步驟，就是開發人員定義要解決的商務問題，並決定需要哪些元件和服務。</span><span class="sxs-lookup"><span data-stu-id="9ee82-202">The first step in the COM+ application design phase, where the developer defines the business problems to be solved and decides what components and services are required.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-203"><span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**併發**</span><span class="sxs-lookup"><span data-stu-id="9ee82-203"><span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**concurrency**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-204">一個以上的交易或進程同時存取相同資料的能力。</span><span class="sxs-lookup"><span data-stu-id="9ee82-204">The ability of more than one transaction or process to access the same data at the same time.</span></span> <span data-ttu-id="9ee82-205">COM + 通常會透過同步處理來管理並行。</span><span class="sxs-lookup"><span data-stu-id="9ee82-205">COM+ generally manages concurrency through synchronization.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-206"><span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**設定的元件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-206"><span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**configured component**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-207">已安裝至 COM + 應用程式的 COM 元件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-207">A COM component that has been installed into a COM+ application.</span></span> <span data-ttu-id="9ee82-208">安裝之後，元件會在 COM + 類別目錄內設定，以利用可用的 COM + 服務。</span><span class="sxs-lookup"><span data-stu-id="9ee82-208">After it is installed, the component is configured within the COM+ catalog to make use of the available COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-209"><span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**上下文**</span><span class="sxs-lookup"><span data-stu-id="9ee82-209"><span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-210">一組與一或多個 COM 物件相關聯的執行時間屬性，可用來為這些物件提供服務。</span><span class="sxs-lookup"><span data-stu-id="9ee82-210">A set of run-time properties associated with one or more COM objects that are used to provide services for those objects.</span></span> <span data-ttu-id="9ee82-211">每個 COM 物件都會在啟動的單一內容中執行，而不是在相同的公寓) 內 (一律停用。</span><span class="sxs-lookup"><span data-stu-id="9ee82-211">Every COM object runs in a single context from activation to deactivation (always within the same apartment).</span></span> <span data-ttu-id="9ee82-212">當物件啟動時初始化、內容屬性，例如資訊安全內容屬性，代表物件的執行時間需求。</span><span class="sxs-lookup"><span data-stu-id="9ee82-212">Initialized when an object is activated, context properties, such as security context properties, represent the run-time needs of an object.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-213"><span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**資料層**</span><span class="sxs-lookup"><span data-stu-id="9ee82-213"><span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**data tier**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-214">在商務應用程式的三層式架構模型中，可透過仲介層或商務服務層存取的 DBMS 存取層，以及有時透過展示層或使用者服務層來存取的 DBMS 存取層。</span><span class="sxs-lookup"><span data-stu-id="9ee82-214">In the three-tier architecture model for business applications, the DBMS access layer, which can be accessed through the middle tier, or business services layer, and on occasion through the presentation tier, or user services layer.</span></span> <span data-ttu-id="9ee82-215">資料層是由 (的資料存取元件所組成，而不是原始的 DBMS 連接) 協助資源分享，並允許設定用戶端，而不需要在每個用戶端上安裝 DBMS 程式庫和 ODBC 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="9ee82-215">The data tier consists of data access components (rather than raw DBMS connections) to aid in resource sharing and to allow clients to be configured without installing the DBMS libraries and ODBC drivers on each client.</span></span> <span data-ttu-id="9ee82-216">也稱為 *資料服務層*。</span><span class="sxs-lookup"><span data-stu-id="9ee82-216">Also called *data services layer*.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-217"><span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**僵局**</span><span class="sxs-lookup"><span data-stu-id="9ee82-217"><span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**deadlock**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-218">在多執行緒應用程式中，當一組執行緒的每個成員正在等候集合的另一個成員時，就會發生執行緒問題。</span><span class="sxs-lookup"><span data-stu-id="9ee82-218">In multithreaded applications, a threading problem that occurs when each member of a set of threads is waiting for another member of the set.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-219"><span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**代表團**</span><span class="sxs-lookup"><span data-stu-id="9ee82-219"><span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**delegation**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-220">一種模擬形式，可授權伺服器代表用戶端進行動作，讓伺服器能夠透過網路模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="9ee82-220">A form of impersonation that authorizes a server to act on a client's behalf, giving the server the ability to impersonate clients over the network.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-221"><span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**分散式交易**</span><span class="sxs-lookup"><span data-stu-id="9ee82-221"><span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**distributed transaction**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-222">牽涉到多個資源管理員的交易，可位於相同或不同的電腦上。</span><span class="sxs-lookup"><span data-stu-id="9ee82-222">A transaction that involves multiple resource managers, which can be on the same or different computers.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-223"><span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**分散式交易協調器 (DTC)**</span><span class="sxs-lookup"><span data-stu-id="9ee82-223"><span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Distributed Transaction Coordinator (DTC)**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-224">一種系統服務，可管理一或多個系統上分散于兩個或多個資源管理員的交易和交易相關通訊，以確保 ACID 交易的正確性。</span><span class="sxs-lookup"><span data-stu-id="9ee82-224">A system service that manages transactions and transaction-related communications that are distributed across two or more resource managers on one or more systems to ensure correct ACID transactions.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-225"><span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**動態掩蓋**</span><span class="sxs-lookup"><span data-stu-id="9ee82-225"><span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**dynamic cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-226">一種掩蓋形式，其中原始用戶端身分識別會在每次對下游伺服器的方法呼叫上探索為伺服器執行緒存取權杖。</span><span class="sxs-lookup"><span data-stu-id="9ee82-226">A form of cloaking where the original client identity is discovered as the server thread access token on each method call to the downstream server.</span></span> <span data-ttu-id="9ee82-227">雖然提供的身分識別可動態判斷，但進行這項作業所需的額外負荷可能會大幅增加。</span><span class="sxs-lookup"><span data-stu-id="9ee82-227">Although the identity that is presented can be determined dynamically, the overhead required to do this can be considerably more expensive.</span></span> <span data-ttu-id="9ee82-228">針對 COM + 應用程式，預設設定適用于動態擬呼功能，因為它提供了通常需要在一開始使用模擬的情況下所需的彈性。</span><span class="sxs-lookup"><span data-stu-id="9ee82-228">For COM+ applications, the default configuration is for dynamic cloaking capability because it provides the flexibility that is usually required by circumstances that necessitate using impersonation in the first place.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-229"><span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**列舉值物件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-229"><span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**enumerator object**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-230">啟用集合中項目的列舉。</span><span class="sxs-lookup"><span data-stu-id="9ee82-230">Enables enumeration of items in a collection.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-231"><span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**事件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-231"><span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**event**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-232">物件所辨識的動作，例如按一下滑鼠或按下按鍵，以及您可以撰寫程式碼來回應的動作。</span><span class="sxs-lookup"><span data-stu-id="9ee82-232">An action recognized by an object, such as clicking the mouse or pressing a key, and for which you can write code to respond.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-233"><span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**事件類別物件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-233"><span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**event class object**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-234">在 COM + 事件系統中提供持續性記錄的已設定元件，用以描述與這些發行者相關聯的發行者和引發介面。</span><span class="sxs-lookup"><span data-stu-id="9ee82-234">A configured component that provides a persistent record in the COM+ event system to describe the publishers and the firing interfaces associated with those publishers.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-235"><span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**事件方法**</span><span class="sxs-lookup"><span data-stu-id="9ee82-235"><span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**event method**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-236">COM + 介面中識別 COM + 事件的方法。</span><span class="sxs-lookup"><span data-stu-id="9ee82-236">A method in a COM+ interface that identifies a COM+ event.</span></span> <span data-ttu-id="9ee82-237">事件方法必須是唯一的名稱，而且只能包含輸入參數。</span><span class="sxs-lookup"><span data-stu-id="9ee82-237">Event methods must be uniquely named and can contain only input parameters.</span></span> <span data-ttu-id="9ee82-238">傳回值必須是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="9ee82-238">The return value must be an **HRESULT**.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-239"><span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**事件物件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-239"><span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**event object**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-240">COM 物件，可通知一個或多個發生事件的執行緒。</span><span class="sxs-lookup"><span data-stu-id="9ee82-240">A COM object that can signal one or more threads that an event has occurred.</span></span> <span data-ttu-id="9ee82-241">進程內的任何執行緒都可以建立事件物件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-241">Any thread within a process can create an event object.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-242"><span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**例外**</span><span class="sxs-lookup"><span data-stu-id="9ee82-242"><span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**exception**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-243">在程式執行期間發生的異常狀況或錯誤，需要在正常控制流程之外執行軟體。</span><span class="sxs-lookup"><span data-stu-id="9ee82-243">An abnormal condition or error that occurs during the execution of a program and that requires the execution of software outside the normal flow of control.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-244"><span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**故障**</span><span class="sxs-lookup"><span data-stu-id="9ee82-244"><span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**failover**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-245">在叢集網路系統中，將超載或失敗的資源（例如伺服器、磁片磁碟機或網路）重新放置到其備份元件的程式。</span><span class="sxs-lookup"><span data-stu-id="9ee82-245">In a cluster network system, the process of relocating an overloaded or failed resource—such as a server, a disk drive, or a network—to its backup component.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-246"><span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**無限制執行緒進程**</span><span class="sxs-lookup"><span data-stu-id="9ee82-246"><span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**free-threaded process**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-247">具有多執行緒單元且沒有單一執行緒單元的進程。</span><span class="sxs-lookup"><span data-stu-id="9ee82-247">A process that has a multithreaded apartment and no single-threaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-248"><span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**全域認可協調器**</span><span class="sxs-lookup"><span data-stu-id="9ee82-248"><span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**global commit coordinator**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-249">在以 Microsoft Windows 為基礎的分散式交易系統上，認可樹狀結構的根交易管理員。</span><span class="sxs-lookup"><span data-stu-id="9ee82-249">On a Microsoft Windows–based distributed transaction system, the root transaction manager of the commit tree.</span></span> <span data-ttu-id="9ee82-250">此協調器會決定要認可或中止指定的交易，而且永遠不會有任何疑慮。</span><span class="sxs-lookup"><span data-stu-id="9ee82-250">This coordinator makes the decision to either commit or abort a given transaction and is never in doubt.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-251"><span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**類比**</span><span class="sxs-lookup"><span data-stu-id="9ee82-251"><span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**impersonation**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-252">執行緒在安全性內容中執行的能力，與擁有線程的進程不同。</span><span class="sxs-lookup"><span data-stu-id="9ee82-252">The ability of a thread to execute in a security context different from that of the process owning the thread.</span></span> <span data-ttu-id="9ee82-253">伺服器執行緒會使用代表用戶端認證的存取權杖，並透過此存取權杖存取用戶端可以存取的資源。</span><span class="sxs-lookup"><span data-stu-id="9ee82-253">The server thread uses an access token representing the client's credentials, and with this, it can access resources that the client can access.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-254"><span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**模擬等級**</span><span class="sxs-lookup"><span data-stu-id="9ee82-254"><span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**impersonation level**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-255">用戶端用來授與伺服器特定授權層級的設定，以代表用戶端執行動作。</span><span class="sxs-lookup"><span data-stu-id="9ee82-255">The setting used by the client to grant the server a particular level of authority to carry out actions on the client's behalf.</span></span> <span data-ttu-id="9ee82-256">在 COM + 中，這只能針對 COM + 伺服器應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="9ee82-256">In COM+, this can be set only for COM+ server applications.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-257"><span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**攔截**</span><span class="sxs-lookup"><span data-stu-id="9ee82-257"><span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**interception**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-258">針對在給定內容中啟動的物件，處理從內容界限呼叫該物件的程式。</span><span class="sxs-lookup"><span data-stu-id="9ee82-258">For an object activated in a given context, the process of handling calls to that object from across the context boundary.</span></span> <span data-ttu-id="9ee82-259">跨內容的呼叫會使用輕量介面 proxy 來處理，而這些 proxy 會處理任何需要的中繼工作，將執行時間環境從容納呼叫者的執行時間環境調整為容納被呼叫端的伺服器。</span><span class="sxs-lookup"><span data-stu-id="9ee82-259">Calls across context are handled with lightweight interface proxies that will handle whatever mediation is required to adjust the run-time environment from one that accommodates the caller to one that accommodates the callee.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-260"><span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**介面**</span><span class="sxs-lookup"><span data-stu-id="9ee82-260"><span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**interface**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-261">在以 COM 為基礎的程式設計中，提供 COM 物件存取權的相關公用函式集合。</span><span class="sxs-lookup"><span data-stu-id="9ee82-261">In COM-based programming, a collection of related public functions that provide access to a COM object.</span></span> <span data-ttu-id="9ee82-262">COM 物件上的介面集合會撰寫一個合約，以指定程式和其他物件如何與 COM 物件互動。</span><span class="sxs-lookup"><span data-stu-id="9ee82-262">The set of interfaces on a COM object composes a contract that specifies how programs and other objects can interact with the COM object.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-263"><span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**介面 proxy**</span><span class="sxs-lookup"><span data-stu-id="9ee82-263"><span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**interface proxy**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-264">封裝 (的介面特定物件會封送處理該介面的) 參數，以準備遠端方法呼叫，並 unpackages (拆收) 來自介面存根的傳回值。</span><span class="sxs-lookup"><span data-stu-id="9ee82-264">An interface-specific object that packages (marshals) parameters for that interface in preparation for a remote method call and unpackages (unmarshals) the return values from the interface stub.</span></span> <span data-ttu-id="9ee82-265">Proxy 會在寄件者的位址空間中執行，並與接收者位址空間中的對應存根進行通訊。</span><span class="sxs-lookup"><span data-stu-id="9ee82-265">A proxy runs in the address space of the sender and communicates with a corresponding stub in the receiver's address space.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-266"><span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**介面存根**</span><span class="sxs-lookup"><span data-stu-id="9ee82-266"><span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**interface stub**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-267">介面特定的物件，可 unpackages 封送處理的參數、呼叫所需的方法和封裝， (封送處理來自所呼叫方法的) 傳回值。</span><span class="sxs-lookup"><span data-stu-id="9ee82-267">An interface-specific object that unpackages marshaled parameters, calls the required method, and packages (marshals) return values from the called method.</span></span> <span data-ttu-id="9ee82-268">Stub 會在接收者的位址空間中執行，並與寄件者位址空間中的對應介面 proxy 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="9ee82-268">The stub runs in the receiver's address space and communicates with a corresponding interface proxy in the sender's address space.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-269"><span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**內建物件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-269"><span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**interior object**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-270">在交易式階層中，根物件下的任何物件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-270">In a transactional hierarchy, any object under the root object.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-271"><span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**及時 (JIT) 啟用**</span><span class="sxs-lookup"><span data-stu-id="9ee82-271"><span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**just-in-time (JIT) activation**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-272">COM + 提供的自動服務，可讓閒置的伺服器資源更有效率地使用。</span><span class="sxs-lookup"><span data-stu-id="9ee82-272">An automatic service provided by COM+ that allows idle server resources to be used more productively.</span></span> <span data-ttu-id="9ee82-273">當元件設定為 JIT 啟用時，COM + 可以停用它的實例，而用戶端仍保留物件的使用中參考。</span><span class="sxs-lookup"><span data-stu-id="9ee82-273">When a component is configured as JIT activated, COM+ can deactivate an instance of it while a client still holds an active reference to the object.</span></span> <span data-ttu-id="9ee82-274">下次用戶端在物件上呼叫方法時，COM + 會以透明的方式將物件重新開機至用戶端。</span><span class="sxs-lookup"><span data-stu-id="9ee82-274">The next time the client calls a method on the object, COM+ will reactivate the object transparently to the client, just in time.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-275"><span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**舊版元件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-275"><span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**legacy component**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-276">已安裝至 COM + 應用程式的未設定元件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-276">An unconfigured component that has been installed into a COM+ application.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-277"><span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**聽眾**</span><span class="sxs-lookup"><span data-stu-id="9ee82-277"><span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**listener**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-278">COM + 佇列元件服務的架構元素。</span><span class="sxs-lookup"><span data-stu-id="9ee82-278">An architectural element of the COM+ Queued Components service.</span></span> <span data-ttu-id="9ee82-279">接聽程式是 COM 物件，它會開啟與其主機應用程式相關聯的訊息佇列，並等候訊息到達。</span><span class="sxs-lookup"><span data-stu-id="9ee82-279">The listener is a COM object that opens the message queue associated with its host application and waits for messages to arrive.</span></span> <span data-ttu-id="9ee82-280">當訊息抵達時，接聽程式會分派處理訊息的執行緒。</span><span class="sxs-lookup"><span data-stu-id="9ee82-280">As messages arrive, the listener dispatches threads that process messages.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-281"><span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**邏輯模型**</span><span class="sxs-lookup"><span data-stu-id="9ee82-281"><span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**logical model**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-282">COM + 應用程式設計程式中的第二個步驟，概念模型會分成三層架構的邏輯層，如下所示：展示層或使用者服務。中介層或商務服務;和資料層，或資料服務。</span><span class="sxs-lookup"><span data-stu-id="9ee82-282">The second step in a COM+ application design process, where the conceptual model is broken out into the logical tiers of the three-tier architecture, as follows: the presentation tier, or user services; the middle tier, or business services; and the data tier, or data services.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-283"><span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**鬆散結合的事件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-283"><span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**loosely coupled event**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-284">傳送者 (發行者) 和接收者 (訂閱者) 未緊密系結的事件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-284">An event whose sender (publisher) and receiver (subscriber) are not closely bound.</span></span> <span data-ttu-id="9ee82-285">在鬆散結合的事件系統中（例如 COM + 事件），來自不同發行者的事件資訊會保存在事件存放區中。</span><span class="sxs-lookup"><span data-stu-id="9ee82-285">In a loosely coupled event system, such as COM+ Events, event information from different publishers is persisted in an event store.</span></span> <span data-ttu-id="9ee82-286">訂閱者會查詢此存放區，並選取要接收的事件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-286">Subscribers query this store and select the events that they want to receive.</span></span> <span data-ttu-id="9ee82-287">從事件存放區選取事件資訊會建立訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="9ee82-287">Selecting event information from the event store creates a subscription.</span></span> <span data-ttu-id="9ee82-288">當事件發生時，事件系統會在此資料庫中尋找，並尋找感興趣的訂閱者、建立每個感興趣類別的新物件，並在該物件上呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="9ee82-288">When an event occurs, the event system looks in this database and finds the interested subscribers, creates a new object of each interested class, and calls a method on that object.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-289"><span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**編組**</span><span class="sxs-lookup"><span data-stu-id="9ee82-289"><span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**marshaling**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-290">跨執行緒或進程界限封裝和解除封裝介面方法參數的程式，讓遠端程序呼叫得以進行。</span><span class="sxs-lookup"><span data-stu-id="9ee82-290">The process of packaging and unpackaging interface method parameters across thread or process boundaries so that a remote procedure call can take place.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-291"><span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**訊息移動器**</span><span class="sxs-lookup"><span data-stu-id="9ee82-291"><span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**message mover**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-292">COM + 佇列元件服務的架構元素，會將失敗的訊息移回其輸入佇列，以便重試。</span><span class="sxs-lookup"><span data-stu-id="9ee82-292">The architectural element of the COM+ Queued Components service that moves failed messages back to their input queue so that they can be retried.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-293"><span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**中繼事件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-293"><span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**meta-event**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-294">當建立、修改或移除事件類別物件或訂用帳戶時，COM + 事件系統用來通知有興趣的訂閱者的事件種類。</span><span class="sxs-lookup"><span data-stu-id="9ee82-294">A type of event used by the COM+ Events system to notify interested subscribers whenever event class objects or subscriptions are created, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-295"><span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**方法**</span><span class="sxs-lookup"><span data-stu-id="9ee82-295"><span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**method**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-296">在以 COM 為基礎的程式設計中，COM 物件在接收訊息時所執行的處理常式。</span><span class="sxs-lookup"><span data-stu-id="9ee82-296">In COM-based programming, a process performed by a COM object when it receives a message.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-297"><span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**中介層**</span><span class="sxs-lookup"><span data-stu-id="9ee82-297"><span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**middle tier**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-298">在商務應用程式的三層式架構模型中，包含商務邏輯和資料規則的圖層。</span><span class="sxs-lookup"><span data-stu-id="9ee82-298">In the three-tier architecture model for business applications, the layer comprising the business logic and data rules.</span></span> <span data-ttu-id="9ee82-299">組成仲介層的元件可以用來強制執行商務規則，例如商務演算法、法律或政府法規，以及資料規則，這些規則是設計用來在特定或多個資料庫中保持一致的資料結構。</span><span class="sxs-lookup"><span data-stu-id="9ee82-299">The components that make up the middle tier can be used to enforce business rules, such as business algorithms, legal or governmental regulations, and data rules, which are designed to keep the data structures consistent within either specific or multiple databases.</span></span> <span data-ttu-id="9ee82-300">因為這些中介層元件未系結至特定的用戶端，所以可供所有應用程式使用，並可隨著回應時間和其他規則的需求移至不同的位置。</span><span class="sxs-lookup"><span data-stu-id="9ee82-300">Because these middle-tier components are not tied to a specific client, they can be used by all applications and can be moved to different locations as response time and other rules require.</span></span> <span data-ttu-id="9ee82-301">也稱為「 *商務服務層* 」或「 *商務邏輯層*」。</span><span class="sxs-lookup"><span data-stu-id="9ee82-301">Also called *business services layer* or *business logic tier*.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-302"><span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**混合模型進程**</span><span class="sxs-lookup"><span data-stu-id="9ee82-302"><span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**mixed model process**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-303">具有多執行緒單元的進程，以及一或多個單一執行緒單元。</span><span class="sxs-lookup"><span data-stu-id="9ee82-303">A process that has a multithreaded apartment and one or more single-threaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-304"><span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**綽號**</span><span class="sxs-lookup"><span data-stu-id="9ee82-304"><span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**moniker**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-305">可唯一識別 COM 物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ee82-305">A name that uniquely identifies a COM object.</span></span> <span data-ttu-id="9ee82-306">與路徑在檔案系統中識別檔案的方式相同，標記會識別目錄命名空間中的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-306">In the same way that a path identifies a file in the file system, a moniker identifies a COM object in the directory namespace.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-307"><span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**.msi 檔案**</span><span class="sxs-lookup"><span data-stu-id="9ee82-307"><span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**.msi file**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-308">當您匯出 COM + 應用程式或應用程式 proxy 以便在另一部電腦上安裝時，由 [元件服務] 系統管理工具所建立的檔案。</span><span class="sxs-lookup"><span data-stu-id="9ee82-308">A file created by the Component Services administrative tool when you export a COM+ application or application proxy for installation on another computer.</span></span> <span data-ttu-id="9ee82-309">您可以使用 Windows Installer 將 .msi 檔案安裝在任何 Windows 型用戶端上。</span><span class="sxs-lookup"><span data-stu-id="9ee82-309">The .msi file can be installed on any Windows-based client using Windows Installer.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-310"><span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**多執行緒單元模型**</span><span class="sxs-lookup"><span data-stu-id="9ee82-310"><span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**multithreaded apartment model**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-311">一個單元模型，在此模型中，進程中已初始化為自由執行緒的所有線程都位於單一單元中。</span><span class="sxs-lookup"><span data-stu-id="9ee82-311">An apartment model in which all the threads in the process that have been initialized as free-threaded reside in a single apartment.</span></span> <span data-ttu-id="9ee82-312">因此，不需要線上程之間進行封送處理。</span><span class="sxs-lookup"><span data-stu-id="9ee82-312">Therefore, there is no need to marshal between threads.</span></span> <span data-ttu-id="9ee82-313">執行緒不需要取得和分派訊息，因為 COM 不會在此模型中使用視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="9ee82-313">The threads need not retrieve and dispatch messages because COM does not use window messages in this model.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-314"><span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**嵌套交易**</span><span class="sxs-lookup"><span data-stu-id="9ee82-314"><span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**nested transaction**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-315">從現有的主要或父系交易界限內起始的次要交易。</span><span class="sxs-lookup"><span data-stu-id="9ee82-315">A secondary transaction initiated from within an existing primary or parent transaction boundary.</span></span> <span data-ttu-id="9ee82-316">在其所有從屬或嵌套交易認可之前，不會認可主要交易。</span><span class="sxs-lookup"><span data-stu-id="9ee82-316">The primary transaction does not commit until all of its subordinate, or nested, transactions commit.</span></span> <span data-ttu-id="9ee82-317">COM + 不支援嵌套交易。</span><span class="sxs-lookup"><span data-stu-id="9ee82-317">COM+ does not support nested transactions.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-318"><span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**中立的單元模型**</span><span class="sxs-lookup"><span data-stu-id="9ee82-318"><span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**neutral apartment model**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-319">執行緒模型，其中的物件會遵循多執行緒單元的指導方針，但可以在任何類型的執行緒上執行。</span><span class="sxs-lookup"><span data-stu-id="9ee82-319">A threading model in which objects follow the guidelines for multithreaded apartments but can execute on any kind of thread.</span></span> <span data-ttu-id="9ee82-320">中立的單元模型是適用于 COM 元件和 COM + 應用程式的建議執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="9ee82-320">The neutral apartment model is the recommended threading model for COM components and COM+ applications.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-321"><span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**持續性物件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-321"><span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**persistent object**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-322">COM 物件，可在用戶端要求用戶端時儲存其內部狀態，且符合 COM 定義的標準，用戶端可以要求物件在資料存放區之間進行初始化、載入和儲存， (例如一般檔案、結構化儲存體或記憶體) 。</span><span class="sxs-lookup"><span data-stu-id="9ee82-322">A COM object that can save its internal state when asked to do so by a client and that conforms to COM-defined standards through which clients can request objects to be initialized, loaded, and saved to and from a data store (for example, flat file, structured storage, or memory).</span></span> <span data-ttu-id="9ee82-323">用戶端負責管理物件的持續性資料的儲存位置，而非資料的格式。</span><span class="sxs-lookup"><span data-stu-id="9ee82-323">It is the client's responsibility to manage the location where the object's persistent data is stored but not the format of the data.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-324"><span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**持續性物件介面**</span><span class="sxs-lookup"><span data-stu-id="9ee82-324"><span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**persistent object interface**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-325">由持續性物件所執行的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="9ee82-325">A COM interface implemented by a persistent object.</span></span> <span data-ttu-id="9ee82-326">用戶端會使用持續性物件介面，來告知這些持續性物件的儲存狀態和位置。</span><span class="sxs-lookup"><span data-stu-id="9ee82-326">Clients use persistent object interfaces to tell those persistent objects when and where to store their state.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-327"><span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**階段零通知介面**</span><span class="sxs-lookup"><span data-stu-id="9ee82-327"><span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**phase zero notification interface**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-328">COM + 介面，可讓應用程式偵測交易何時準備好繼續進行兩階段認可通訊協定，讓它可以執行必要的通知作業，並在作業完成時與交易管理員進行通訊。</span><span class="sxs-lookup"><span data-stu-id="9ee82-328">COM+ interface that allows applications to detect when a transaction is ready to proceed with a two-phase commit protocol so that it can perform the necessary notification operations and communicate to the transaction manager when the operations have been completed.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-329"><span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**實體模型**</span><span class="sxs-lookup"><span data-stu-id="9ee82-329"><span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**physical model**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-330">COM + 應用程式設計程式中的第三個和最後一個步驟，可讓開發人員判斷元件的實際位置，以及如何編寫程式碼。</span><span class="sxs-lookup"><span data-stu-id="9ee82-330">The third and final step in the COM+ application design process, where the developer determines where the components reside physically and how they are to be coded.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-331"><span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**球員**</span><span class="sxs-lookup"><span data-stu-id="9ee82-331"><span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**player**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-332">COM + 佇列元件服務的架構專案，會從佇列中取出訊息，然後載入伺服器物件和標準介面存根，以 unmarshal 資料並叫用伺服器方法。</span><span class="sxs-lookup"><span data-stu-id="9ee82-332">The architectural element of the COM+ Queued Components service that retrieves the message from a queue and then loads the server object and the standard interface stubs to unmarshal data and invoke server methods.</span></span> <span data-ttu-id="9ee82-333">播放程式會在伺服器端拆收用戶端的安全性內容，然後再叫用伺服器元件，並進行相同的方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="9ee82-333">The player unmarshals the client's security context at the server side and then invokes the server component and makes the same method calls.</span></span> <span data-ttu-id="9ee82-334">除非用戶端元件完成，而且記錄方法的交易呼叫認可，否則播放程式不會播放方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="9ee82-334">The method calls are not played back by the player until the client component completes and the transaction that recorded the method calls commits.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-335"><span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**展示層**</span><span class="sxs-lookup"><span data-stu-id="9ee82-335"><span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**presentation tier**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-336">在商務應用程式的三層式架構模型中，將資料呈現給使用者，並選擇性地允許資料操作和資料輸入的圖層。</span><span class="sxs-lookup"><span data-stu-id="9ee82-336">In the three-tier architecture model for business applications, the layer that presents data to the user and optionally permits data manipulation and data entry.</span></span> <span data-ttu-id="9ee82-337">展示層的兩個主要使用者介面類別型是傳統的應用程式和 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="9ee82-337">The two main types of user interface for the presentation tier are the traditional application and the Web-based application.</span></span> <span data-ttu-id="9ee82-338">也稱為 *使用者服務層*。</span><span class="sxs-lookup"><span data-stu-id="9ee82-338">Also called *user services layer*.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-339"><span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**主要存取權杖**</span><span class="sxs-lookup"><span data-stu-id="9ee82-339"><span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**primary access token**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-340">描述與進程相關聯之使用者帳戶的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="9ee82-340">Describes the security context of the user account associated with a process.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-341"><span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**proxy 管理員**</span><span class="sxs-lookup"><span data-stu-id="9ee82-341"><span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**proxy manager**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-342">在標準封送處理中，管理單一物件之所有介面 proxy 的元件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-342">In standard marshaling, a component that manages all the interface proxies for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-343"><span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**虛擬物件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-343"><span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**pseudo-object**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-344">包含的物件類型，例如檔中的使用者選取專案、試算表中的資料格範圍，或文字檔中的字元範圍。</span><span class="sxs-lookup"><span data-stu-id="9ee82-344">A type of contained object, such as a user selection in a document, a range of cells in a spreadsheet, or a range of characters in a text document.</span></span> <span data-ttu-id="9ee82-345">這種類型的物件稱為虛擬物件，因為它不會被視為相異物件，直到使用者標示選取範圍為止。</span><span class="sxs-lookup"><span data-stu-id="9ee82-345">This type of object is called a pseudo-object because it isn't treated as a distinct object until a user marks the selection.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-346"><span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**出版商**</span><span class="sxs-lookup"><span data-stu-id="9ee82-346"><span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**publisher**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-347">事件的寄件者。</span><span class="sxs-lookup"><span data-stu-id="9ee82-347">The sender of an event.</span></span> <span data-ttu-id="9ee82-348">在 COM + 事件架構中，發行者會進行方法呼叫來起始事件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-348">In the COM+ Events architecture, the publisher makes the method call to initiate an event.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-349"><span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**佇列標記**</span><span class="sxs-lookup"><span data-stu-id="9ee82-349"><span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**queue moniker**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-350">用來啟動已排入佇列之元件的標記。</span><span class="sxs-lookup"><span data-stu-id="9ee82-350">The moniker used to activate a queued component.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-351"><span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**競爭條件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-351"><span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**race condition**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-352">在多執行緒應用程式中，當多個執行緒存取資料項目但沒有協調時所發生的狀況，可能會導致不一致的結果，視哪個執行緒先到達資料項目而定。</span><span class="sxs-lookup"><span data-stu-id="9ee82-352">In a multithreaded application, a condition that occurs when multiple threads access a data item without coordination, possibly causing inconsistent results, depending on which thread reaches the data item first.</span></span> <span data-ttu-id="9ee82-353">COM 提供一些特別設計來協助避免跨進程伺服器發生競爭情況的函式。</span><span class="sxs-lookup"><span data-stu-id="9ee82-353">COM supplies some functions specifically designed to help avoid race conditions in out-of-process servers.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-354"><span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**答錄機**</span><span class="sxs-lookup"><span data-stu-id="9ee82-354"><span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**recorder**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-355">COM + 佇列元件服務的架構專案，會將用戶端的安全性內容封送處理到訊息中，並記錄物件的所有方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="9ee82-355">The architectural element of the COM+ Queued Components service that marshals the client's security context into a message and records all of the method calls for an object.</span></span> <span data-ttu-id="9ee82-356">錄製器是系統提供的 proxy 管理員，可從 COM + 目錄中的 queuable 介面選取介面。</span><span class="sxs-lookup"><span data-stu-id="9ee82-356">The recorder is a system-provided proxy manager that selects interfaces from the queuable interfaces in the COM+ catalog.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-357"><span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**資源配置器**</span><span class="sxs-lookup"><span data-stu-id="9ee82-357"><span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**resource dispenser**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-358">在 COM + 程式設計模型中，會代表進程內的應用程式元件來管理非持久性共用狀態的元件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-358">In the COM+ programming model, a component that manages nondurable shared state on behalf of the application components within a process.</span></span> <span data-ttu-id="9ee82-359">資源機類似于資源管理員，但不保證持久性。</span><span class="sxs-lookup"><span data-stu-id="9ee82-359">Resource dispensers are similar to resource managers but without the guarantee of durability.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-360"><span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**資源管理員**</span><span class="sxs-lookup"><span data-stu-id="9ee82-360"><span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**resource manager**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-361">管理資料庫、持久訊息佇列或交易式檔案系統中的持續性或持久性資料的服務。</span><span class="sxs-lookup"><span data-stu-id="9ee82-361">A service that manages persistent or durable data in databases, durable message queues, or transactional file systems.</span></span> <span data-ttu-id="9ee82-362">它是知道如何儲存資料並執行嚴重損壞修復的資源管理員。</span><span class="sxs-lookup"><span data-stu-id="9ee82-362">It is the resource manager that knows how to store data and perform disaster recovery.</span></span> <span data-ttu-id="9ee82-363">COM + 伺服器應用程式會使用資源管理員來維護應用程式的持久狀態，例如庫存手邊的記錄、待處理的訂單，以及應收帳款的帳戶。</span><span class="sxs-lookup"><span data-stu-id="9ee82-363">COM+ server applications use resource managers to maintain the durable state of an application, such as the record of inventory on hand, pending orders, and accounts receivable.</span></span> <span data-ttu-id="9ee82-364">資源管理員與 Microsoft Distributed Transaction Coordinator (DTC) 合作，以確保應用程式的不可部分完成性和隔離。</span><span class="sxs-lookup"><span data-stu-id="9ee82-364">Resource managers work in cooperation with the Microsoft Distributed Transaction Coordinator (DTC) to guarantee atomicity and isolation to an application.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-365"><span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**以角色為基礎的安全性**</span><span class="sxs-lookup"><span data-stu-id="9ee82-365"><span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**role-based security**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-366">Com + 應用程式所提供的 COM + 安全性服務。</span><span class="sxs-lookup"><span data-stu-id="9ee82-366">A COM+ security service provided for COM+ applications.</span></span> <span data-ttu-id="9ee82-367">角色代表針對 COM + 應用程式所定義的使用者類別，目的是要判斷應用程式資源的存取權限。</span><span class="sxs-lookup"><span data-stu-id="9ee82-367">A role represents a category of users defined for a COM+ application for the purpose of determining access permissions to the application's resources.</span></span> <span data-ttu-id="9ee82-368">開發人員將角色指派給元件、介面和方法。</span><span class="sxs-lookup"><span data-stu-id="9ee82-368">Roles are assigned by a developer to components, interfaces, and methods.</span></span> <span data-ttu-id="9ee82-369">系統管理員會將使用者指派給適當的角色，讓指定角色內的使用者可以存取指派該角色的任何資源。</span><span class="sxs-lookup"><span data-stu-id="9ee82-369">Users are assigned by an administrator to appropriate roles, enabling a user within a given role to access any resources to which that role is assigned.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-370"><span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**根物件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-370"><span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**root object**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-371">交易的第一個物件，稱為交易的根目錄，且一律放置在新的交易界限內。</span><span class="sxs-lookup"><span data-stu-id="9ee82-371">The first object of a transaction, called the root of the transaction, and always placed in a new transactional boundary.</span></span> <span data-ttu-id="9ee82-372">交易中只能有一個根物件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-372">There can be only one root object in a transaction.</span></span> <span data-ttu-id="9ee82-373">在根物件下，交易式階層中的所有其他物件都稱為內建物件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-373">All other objects in the transactional hierarchy under the root object are called interior objects.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-374"><span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**根交易管理員**</span><span class="sxs-lookup"><span data-stu-id="9ee82-374"><span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**root transaction manager**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-375">啟動交易之系統上的交易管理員。</span><span class="sxs-lookup"><span data-stu-id="9ee82-375">The transaction manager on the system that initiates a transaction.</span></span> <span data-ttu-id="9ee82-376">在根交易管理員判斷交易狀態 (認可或中止) 之前，交易不會完成。</span><span class="sxs-lookup"><span data-stu-id="9ee82-376">The transaction is not finalized until the root transaction manager determines the transaction's status (either committed or aborted).</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-377"><span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**信號**</span><span class="sxs-lookup"><span data-stu-id="9ee82-377"><span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**semaphore**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-378">用來仲裁共用資源存取權的核心物件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-378">A kernel object used to arbitrate access to a shared resource.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-379"><span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**服務控制管理員 (SCM)**</span><span class="sxs-lookup"><span data-stu-id="9ee82-379"><span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**service control manager (SCM)**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-380">管理 Windows 登錄中所有服務的 Microsoft Windows server 進程。</span><span class="sxs-lookup"><span data-stu-id="9ee82-380">A Microsoft Windows server process that manages all the services in the Windows registry.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-381"><span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**共用屬性管理員 (SPM)**</span><span class="sxs-lookup"><span data-stu-id="9ee82-381"><span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**shared property manager (SPM)**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-382">在 Com + 中，您可以用來在伺服器進程內的多個物件之間共用非持續狀態的資源配置器。</span><span class="sxs-lookup"><span data-stu-id="9ee82-382">In Com+, a resource dispenser that you can use to share nonpersistent state among multiple objects within a server process.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-383"><span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**單一執行緒進程**</span><span class="sxs-lookup"><span data-stu-id="9ee82-383"><span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**single-threaded process**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-384">只由一個單一執行緒的單元組成的進程，其中只包含一個執行緒。</span><span class="sxs-lookup"><span data-stu-id="9ee82-384">A process that consists of just one single-threaded apartment, which in turn consists of exactly one thread.</span></span> <span data-ttu-id="9ee82-385">存留于單一執行緒單元中的所有 COM 物件都只能從屬於該單元的一個執行緒接收方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="9ee82-385">All COM objects that live in a single-threaded apartment can receive method calls from only the one thread that belongs to that apartment.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-386"><span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**肥皂**</span><span class="sxs-lookup"><span data-stu-id="9ee82-386"><span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-387">以 XML 為基礎的簡易通訊協定，可在網路上交換結構化和類型資訊。</span><span class="sxs-lookup"><span data-stu-id="9ee82-387">A simple, XML-based protocol for exchanging structured and type information on the Web.</span></span> <span data-ttu-id="9ee82-388">此通訊協定不包含任何應用程式或傳輸語義，使其具有高度模組化和可擴充性。</span><span class="sxs-lookup"><span data-stu-id="9ee82-388">The protocol contains no application or transport semantics, which makes it highly modular and extensible.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-389"><span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**分割註冊**</span><span class="sxs-lookup"><span data-stu-id="9ee82-389"><span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**split registration**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-390">對於已經存在的 COM 元件，並在 COM + 服務環境中使用的元件，註冊的註冊相片順序是將註冊的基本 COM 部分儲存在 Windows 登錄中，並使用新的 COM + 服務和屬性 (例如，已排入佇列的元件) 會儲存在 COM + 註冊資料庫中。</span><span class="sxs-lookup"><span data-stu-id="9ee82-390">For components that are already existing COM components and are used in the COM+ services environment, the registration arrangement in which the basic COM aspect of the registration is stored in the Windows registry and new COM+ services and attributes (for example, Queued Components) are stored in the COM+ Registration Database.</span></span> <span data-ttu-id="9ee82-391">每個元件屬性都會儲存在 Windows 登錄或 COM + 註冊資料庫中。</span><span class="sxs-lookup"><span data-stu-id="9ee82-391">Each component attribute is stored in either the Windows registry or the COM+ Registration Database.</span></span> <span data-ttu-id="9ee82-392">新的 COM 元件會以獨佔方式在 COM + 註冊資料庫中註冊，並在 Windows 登錄中進行一些重複，讓現有的工具可以使用這些元件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-392">New COM components are registered exclusively in the COM+ Registration Database, with some duplication in the Windows registry so that existing tools can use them.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-393"><span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**狀態**</span><span class="sxs-lookup"><span data-stu-id="9ee82-393"><span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**stateful**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-394">或相關的系統或進程，可監視它所參與的活動狀態的所有詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9ee82-394">Of or pertaining to a system or process that monitors all details of the state of an activity in which it participates.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-395"><span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**無 國籍**</span><span class="sxs-lookup"><span data-stu-id="9ee82-395"><span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**stateless**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-396">或相關于參與活動的系統或進程，而不監視其狀態的所有詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9ee82-396">Of or pertaining to a system or process that participates in activity without monitoring all details of its state.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-397"><span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**靜態掩蓋**</span><span class="sxs-lookup"><span data-stu-id="9ee82-397"><span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**static cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-398">一種掩蓋形式，其中原始用戶端身分識別可以向下游伺服器呈現一次，並在 proxy 上設定一次原始用戶端身分識別。</span><span class="sxs-lookup"><span data-stu-id="9ee82-398">A form of cloaking where the original client identity can be presented once to a downstream server, setting the original client identity once on the proxy.</span></span> <span data-ttu-id="9ee82-399">此用戶端身分識別會以伺服器執行緒標記的形式呈現，將用於後續的方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="9ee82-399">This client identity is presented as a server thread token that will be used on subsequent method calls.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-400"><span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**使用者**</span><span class="sxs-lookup"><span data-stu-id="9ee82-400"><span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**subscriber**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-401">事件的接收者。</span><span class="sxs-lookup"><span data-stu-id="9ee82-401">The receiver of an event.</span></span> <span data-ttu-id="9ee82-402">在 COM + 事件架構中，訂閱者會收到發行者所發出的呼叫。</span><span class="sxs-lookup"><span data-stu-id="9ee82-402">In the COM+ Events architecture, the subscriber receives the calls made by the publisher.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-403"><span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**訂用帳戶物件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-403"><span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**subscription object**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-404">在 COM + 事件系統中，訂閱者所建立的物件，用來要求和管理事件的傳遞。</span><span class="sxs-lookup"><span data-stu-id="9ee82-404">In the COM+ Events system, an object created by a subscriber to request and manage the delivery of events.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-405"><span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**同步**</span><span class="sxs-lookup"><span data-stu-id="9ee82-405"><span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**synchronization**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-406">在 COM + 中，一項服務會從元件流至元件，並禁止多個呼叫者在任何指定時間輸入元件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-406">In COM+, a service that flows from component to component and prohibits more than one caller from entering the component at any given time.</span></span> <span data-ttu-id="9ee82-407">同步處理會決定執行緒可以將呼叫分派給物件的時間。</span><span class="sxs-lookup"><span data-stu-id="9ee82-407">Synchronization determines when threads can dispatch calls to an object.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-408"><span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**三層架構模型**</span><span class="sxs-lookup"><span data-stu-id="9ee82-408"><span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**three-tier architectural model**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-409">邏輯設計模型的基本架構，將應用程式的元件分成三個服務層級，如下所示：展示層或使用者服務。中介層或商務服務;和資料層，或資料服務。</span><span class="sxs-lookup"><span data-stu-id="9ee82-409">The fundamental framework for the logical design model, segments an application's components into three tiers of services as follows: the presentation tier, or user services; the middle tier, or business services; and the data tier, or data services.</span></span> <span data-ttu-id="9ee82-410">這些層級不一定會對應到網路上不同電腦上的實體位置，而是對應到應用程式的邏輯層。</span><span class="sxs-lookup"><span data-stu-id="9ee82-410">These tiers do not necessarily correspond to physical locations on various computers on a network, but rather to logical layers of the application.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-411"><span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**緊密結合的活動**</span><span class="sxs-lookup"><span data-stu-id="9ee82-411"><span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**tightly coupled event**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-412">其傳送者 (發行者) 和接收者 (訂閱者) 緊密系結的事件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-412">An event whose sender (publisher) and receiver (subscriber) are closely bound.</span></span> <span data-ttu-id="9ee82-413">在緊密結合的事件系統中，發行者提供了一個介面，可在變更發生時呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="9ee82-413">In a tightly coupled event system, the publisher is provided with an interface on which to call a method when a change occurs.</span></span> <span data-ttu-id="9ee82-414">訂閱者知道要要求通知的發行者，以及公開的介面。</span><span class="sxs-lookup"><span data-stu-id="9ee82-414">The subscriber knows which publisher to request notification from and the interfaces that are exposed.</span></span> <span data-ttu-id="9ee82-415">緊密結合的事件系統需要發行者和訂閱者隨時都在執行。</span><span class="sxs-lookup"><span data-stu-id="9ee82-415">A tightly coupled event system requires that both the publisher and the subscriber are running at all times.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-416"><span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**追蹤記錄檔**</span><span class="sxs-lookup"><span data-stu-id="9ee82-416"><span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**trace log**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-417">由 Microsoft Distributed Transaction Coordinator 自動產生的記錄檔，可顯示與一或多個分散式交易相關的資料。</span><span class="sxs-lookup"><span data-stu-id="9ee82-417">A log file automatically generated by the Microsoft Distributed Transaction Coordinator that shows data related to one or more distributed transactions.</span></span> <span data-ttu-id="9ee82-418">追蹤記錄檔中的資料範例包括交易識別碼、交易時間和指出交易結果的訊息。</span><span class="sxs-lookup"><span data-stu-id="9ee82-418">Examples of data in a trace log are transaction ID, transaction time, and messages indicating the transaction outcome.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-419"><span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**交易**</span><span class="sxs-lookup"><span data-stu-id="9ee82-419"><span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**transaction**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-420">在應用程式處理期間發生一連串相關作業的工作單位。</span><span class="sxs-lookup"><span data-stu-id="9ee82-420">A unit of work in which a series of related operations occur during an application process.</span></span> <span data-ttu-id="9ee82-421">交易只會執行一次，而且是不可部分完成的，可能是所有工作都已完成，或者都不是。</span><span class="sxs-lookup"><span data-stu-id="9ee82-421">A transaction executes exactly once and is atomic—either all of the work is done or none of it is.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-422"><span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**交易網際網路通訊協定 (提示)**</span><span class="sxs-lookup"><span data-stu-id="9ee82-422"><span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Transaction Internet Protocol (TIP)**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-423">交易網際網路通訊協定是標準的兩階段認可通訊協定，可讓異類交易管理員協調分散式交易，尤其是透過網際網路。</span><span class="sxs-lookup"><span data-stu-id="9ee82-423">Transaction Internet Protocol is a standard two-phase commit protocol that enables heterogeneous transaction managers to coordinate distributed transactions, especially over the Internet.</span></span> <span data-ttu-id="9ee82-424">秘訣兩階段認可通訊協定很容易執行，而且獨立于應用程式對應用程式的通訊協定，因此可用於任何應用程式協定，但特別是 HTTP。</span><span class="sxs-lookup"><span data-stu-id="9ee82-424">The TIP two-phase commit protocol is simple to implement and is independent of the application-to-application communications protocol, such that it may be used with any application protocol but especially HTTP.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-425"><span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**交易管理員**</span><span class="sxs-lookup"><span data-stu-id="9ee82-425"><span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**transaction manager**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-426">在參與分散式交易的每一部電腦上執行的 Microsoft Distributed Transaction Coordinator (DTC) 的一部分，並且管理與認可或中止交易交易相關的活動。</span><span class="sxs-lookup"><span data-stu-id="9ee82-426">The part of the Microsoft Distributed Transaction Coordinator (DTC) that executes on each computer participating in a distributed transaction and manages the activities related to committing or aborting that part of the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-427"><span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**交易處理應用程式**</span><span class="sxs-lookup"><span data-stu-id="9ee82-427"><span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**transaction processing application**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-428">將指定的商務工作自動化的交易作業集合。</span><span class="sxs-lookup"><span data-stu-id="9ee82-428">A collection of transaction operations that automate a given business task.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-429"><span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**交易處理系統**</span><span class="sxs-lookup"><span data-stu-id="9ee82-429"><span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**transaction processing system**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-430">包含電腦硬體和軟體的完整系統，可裝載交易處理應用程式，以執行執行業務所需的例行交易。</span><span class="sxs-lookup"><span data-stu-id="9ee82-430">A complete system, comprising both computer hardware and software, that hosts a transaction processing application to perform routine transactions necessary to conduct business.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-431"><span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**兩階段認可通訊協定**</span><span class="sxs-lookup"><span data-stu-id="9ee82-431"><span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**two-phase commit protocol**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-432">只有在分散式交易中使用的通訊協定，可確保交易的結果會在參與交易的所有交易管理員之間保持一致。</span><span class="sxs-lookup"><span data-stu-id="9ee82-432">A protocol used only in distributed transactions, ensures that the outcome of a transaction is consistent across all transaction managers participating in the transaction.</span></span> <span data-ttu-id="9ee82-433">通訊協定會在兩個不同的階段中運作，以最後認可或中止交易：第一個階段會評估每個資源管理員的條件，而第二階段則會完成交易。</span><span class="sxs-lookup"><span data-stu-id="9ee82-433">The protocol operates in two distinct phases to ultimately commit or abort a transaction: phase one evaluates the condition of each resource manager, and phase two completes the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-434"><span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**未設定的元件**</span><span class="sxs-lookup"><span data-stu-id="9ee82-434"><span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**unconfigured component**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-435">尚未在 COM + 目錄中設定的 COM 元件。</span><span class="sxs-lookup"><span data-stu-id="9ee82-435">A COM component that has not been configured within the COM+ catalog.</span></span> <span data-ttu-id="9ee82-436">未配置的元件無法利用 COM + 服務。</span><span class="sxs-lookup"><span data-stu-id="9ee82-436">Unconfigured components cannot make use of COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-437"><span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**下落**</span><span class="sxs-lookup"><span data-stu-id="9ee82-437"><span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**whereabouts**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-438">對於 DTC 交易而言，這是一個不透明的資料結構，代表資源管理員的交易管理員位址。</span><span class="sxs-lookup"><span data-stu-id="9ee82-438">For DTC transactions, an opaque data structure that represents the address of the resource manager's transaction manager.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-439"><span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**XA 介面**</span><span class="sxs-lookup"><span data-stu-id="9ee82-439"><span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**XA interfaces**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-440">一組標準的程式設計介面，可讓 COM + 應用程式開發人員存取 XA 相容的資料庫，並建立可與關係資料庫、訊息佇列、交易式檔案和麵向物件資料庫操作的資源管理員。</span><span class="sxs-lookup"><span data-stu-id="9ee82-440">A standard set of programming interfaces that allow COM+ application developers to access XA-compliant databases and create resource managers that operate with relational databases, message queuing, transactional files, and object-oriented databases.</span></span> <span data-ttu-id="9ee82-441">雖然 Microsoft 不直接支援 XA 通訊協定，但是 Microsoft 支援 OLE 交易與 XA 之間的翻譯工具。</span><span class="sxs-lookup"><span data-stu-id="9ee82-441">Although Microsoft does not directly support the XA protocol, Microsoft does support translation facilities between OLE transactions and XA.</span></span>

</dd> <dt>

<span data-ttu-id="9ee82-442"><span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**XML web service**</span><span class="sxs-lookup"><span data-stu-id="9ee82-442"><span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**XML web services**</span></span>
</dt> <dd>

<span data-ttu-id="9ee82-443">為其他應用程式提供資料和服務的應用程式邏輯單位。</span><span class="sxs-lookup"><span data-stu-id="9ee82-443">Units of application logic providing data and services to other applications.</span></span> <span data-ttu-id="9ee82-444">應用程式會透過標準 Web 通訊協定（例如 SOAP）存取 XML web service。</span><span class="sxs-lookup"><span data-stu-id="9ee82-444">Applications access XML web services through standard Web protocols, such as SOAP.</span></span>

</dd> </dl>

 

 
