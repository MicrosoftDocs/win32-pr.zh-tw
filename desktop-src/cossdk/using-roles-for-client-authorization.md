---
description: 您可以使用以角色為基礎的安全性來建立授權原則，以決定要讓哪個用戶端或用戶端使用哪些授權單位。 您要決定誰可以執行哪些動作並存取哪些資源。
ms.assetid: 8fc27fe1-e50a-44ba-a595-70b1fe463e24
title: 使用角色進行用戶端授權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ae748ddfec438a79e3d0440a00ed7c2f672aed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110889"
---
# <a name="using-roles-for-client-authorization"></a><span data-ttu-id="73b84-104">使用角色進行用戶端授權</span><span class="sxs-lookup"><span data-stu-id="73b84-104">Using Roles for Client Authorization</span></span>

<span data-ttu-id="73b84-105">您可以使用以角色為基礎的安全性來建立授權原則，以決定要讓哪個用戶端或用戶端使用哪些授權單位。</span><span class="sxs-lookup"><span data-stu-id="73b84-105">You use role-based security to establish an authorization policy, determining which client or clients to let in and with what authority.</span></span> <span data-ttu-id="73b84-106">您要決定誰可以執行哪些動作並存取哪些資源。</span><span class="sxs-lookup"><span data-stu-id="73b84-106">You are deciding who should be able to perform which actions and access which resources.</span></span>

<span data-ttu-id="73b84-107">角色可作為每次使用者嘗試存取任何應用程式資源時所叫用的存取控制機制，以協助達成。</span><span class="sxs-lookup"><span data-stu-id="73b84-107">Roles facilitate this by acting as an access control mechanism invoked whenever a user attempts to access any application resource.</span></span> <span data-ttu-id="73b84-108">角色基本上是使用者清單，更精確地說，是共用相同安全性許可權之使用者的符號類別。</span><span class="sxs-lookup"><span data-stu-id="73b84-108">A role is basically a list of users—more precisely, a symbolic category of users that share the same security privilege.</span></span> <span data-ttu-id="73b84-109">當您將角色指派給應用程式資源時，您會將該資源的存取權限授與該角色的成員。</span><span class="sxs-lookup"><span data-stu-id="73b84-109">When you assign a role to an application resource, you are granting access permission for that resource to whoever is a member of that role.</span></span>

<span data-ttu-id="73b84-110">因此，您可以藉由將它宣告為角色，然後將角色指派給特定資源，來定義非常特殊的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="73b84-110">Therefore, you can define a very particular security privilege by declaring it as a role and then assigning the role to specific resources.</span></span> <span data-ttu-id="73b84-111">部署應用程式時，系統管理員可以在角色中填入實際的使用者和使用者群組。</span><span class="sxs-lookup"><span data-stu-id="73b84-111">When the application is deployed, the system administrator can populate the role with actual users and user groups.</span></span> <span data-ttu-id="73b84-112">當應用程式執行時，COM + 會執行角色檢查來強制執行原則。</span><span class="sxs-lookup"><span data-stu-id="73b84-112">When the application runs, COM+ will enforce the policy by carrying out role checks.</span></span>

<span data-ttu-id="73b84-113">基本上，角色可協助保護您的程式碼，也就是 COM + 應用程式的用戶端可以呼叫的方法。</span><span class="sxs-lookup"><span data-stu-id="73b84-113">Fundamentally, roles help protect your code—that is, the methods that can be called by clients of a COM+ application.</span></span> <span data-ttu-id="73b84-114">每當用戶端嘗試呼叫應用程式中的元件所公開的方法時，就會檢查角色成員資格。</span><span class="sxs-lookup"><span data-stu-id="73b84-114">Role membership is checked whenever a client attempts to call a method exposed by a component in an application.</span></span> <span data-ttu-id="73b84-115">如果呼叫端是在指派給被呼叫方法或資源的角色中，則呼叫會成功;否則，它會失敗。</span><span class="sxs-lookup"><span data-stu-id="73b84-115">If the caller is in a role assigned to the called method, or resource, the call succeeds; otherwise, it fails.</span></span>

## <a name="declarative-role-based-security"></a><span data-ttu-id="73b84-116">宣告式 Role-Based 安全性</span><span class="sxs-lookup"><span data-stu-id="73b84-116">Declarative Role-Based Security</span></span>

<span data-ttu-id="73b84-117">使用宣告式以角色為基礎的安全性時，您系統管理員可以使用「元件服務」系統管理工具或系統管理功能來宣告角色，並以系統管理員的方式將它們指派給應用程式資源。</span><span class="sxs-lookup"><span data-stu-id="73b84-117">With declarative role-based security, you administratively declare roles—using either the Component Services administrative tool or the Administrative functions—and administratively assign them to application resources.</span></span> <span data-ttu-id="73b84-118">設定宣告式安全性的位置和方式將會決定您的應用程式在何處繪製安全性界限。</span><span class="sxs-lookup"><span data-stu-id="73b84-118">Where and how you set declarative security will determine where security boundaries are drawn for your application.</span></span> <span data-ttu-id="73b84-119">如需詳細資訊，請參閱 [安全性界限](security-boundaries.md)。</span><span class="sxs-lookup"><span data-stu-id="73b84-119">For more detail, see [Security Boundaries](security-boundaries.md).</span></span>

<span data-ttu-id="73b84-120">您可以將指定的角色指派給整個應用程式、特定元件、元件中的特定介面，或指派給介面上的特定方法。</span><span class="sxs-lookup"><span data-stu-id="73b84-120">You can assign a given role to the entire application, to a particular component, to a particular interface in a component, or to a particular method on an interface.</span></span> <span data-ttu-id="73b84-121">角色指派是繼承自包含的自然鏈，也就是說，如果您將角色指派給元件，它會隱含地指派給該元件所公開的每個介面和方法。</span><span class="sxs-lookup"><span data-stu-id="73b84-121">Role assignments are inherited down the natural chain of inclusion—that is, if you assign a role to a component, it is implicitly assigned to every interface and method exposed by that component.</span></span>

<span data-ttu-id="73b84-122">有了方法層級角色指派的可用性之後，您就可以有效地協助保護尚未考慮安全性的元件和介面。</span><span class="sxs-lookup"><span data-stu-id="73b84-122">With the availability of method-level role assignments, you can effectively help protect components and interfaces that have not been designed with security in mind.</span></span> <span data-ttu-id="73b84-123">但是，如果方法本身並未使用宣告式角色指派進行安全性實體，您可能需要進行程式設計的角色檢查。</span><span class="sxs-lookup"><span data-stu-id="73b84-123">However, if the methods themselves are not securable with declarative role assignments, you might need to do programmatic role checking.</span></span> <span data-ttu-id="73b84-124">一般來說，當您決定如何透過方法來建立商務功能的考慮時，請記住安全性的好主意。否則，您可能會發現自己在最後一分鐘新增安全性相關程式碼。</span><span class="sxs-lookup"><span data-stu-id="73b84-124">It is generally a good idea to keep security in mind when deciding how to factor business functionality through methods; otherwise, you could find yourself adding in security-related code at the last minute.</span></span>

<span data-ttu-id="73b84-125">如需設定以角色為基礎之安全性的詳細程式，請參閱設定 [Role-Based 安全性](configuring-role-based-security.md)。</span><span class="sxs-lookup"><span data-stu-id="73b84-125">For detailed procedures for setting role-based security, see [Configuring Role-Based Security](configuring-role-based-security.md).</span></span>

## <a name="programmatic-security"></a><span data-ttu-id="73b84-126">程式設計安全性</span><span class="sxs-lookup"><span data-stu-id="73b84-126">Programmatic Security</span></span>

<span data-ttu-id="73b84-127">在某些情況下，您可能會想要將安全性邏輯放入元件，同時仍然使用以角色為基礎的安全性。</span><span class="sxs-lookup"><span data-stu-id="73b84-127">In some circumstances you may want to put security logic into components while still using role-based security.</span></span> <span data-ttu-id="73b84-128">您可能無法（或選擇不是）透過方法來構成所有存取決策。</span><span class="sxs-lookup"><span data-stu-id="73b84-128">It might be that you're not able to—or choose not to—factor all access decisions through methods.</span></span> <span data-ttu-id="73b84-129">例如，您可能會有私用應用程式資源（可能是特定的資料庫），而您只想要允許某些方法的呼叫端存取，同時排除其他呼叫者。</span><span class="sxs-lookup"><span data-stu-id="73b84-129">For example, you might have a private application resource, perhaps a particular database, that you want to allow only some callers of a method to access while excluding others.</span></span> <span data-ttu-id="73b84-130">或者，您可能會有單一的 TransferMoney 方法，而且想要藉由限制可傳送的數量來限制某些呼叫者。</span><span class="sxs-lookup"><span data-stu-id="73b84-130">Or you might have a single TransferMoney method and want to restrict some callers by limiting the amount they can transfer.</span></span>

<span data-ttu-id="73b84-131">在這種情況下，您可以在程式碼中進行角色檢查。</span><span class="sxs-lookup"><span data-stu-id="73b84-131">In such circumstances, you can do role checking in code.</span></span> <span data-ttu-id="73b84-132">提供簡單的 API，可讓您檢查安全性是否已開啟，以及呼叫者或特定使用者是否在指定的角色中。</span><span class="sxs-lookup"><span data-stu-id="73b84-132">A simple API is provided, enabling you to check whether security is turned on and whether a caller or a particular user is in a given role.</span></span> <span data-ttu-id="73b84-133">只有啟用以角色為基礎的安全性時，才能使用此功能。</span><span class="sxs-lookup"><span data-stu-id="73b84-133">This functionality is available only when role-based security is enabled.</span></span> <span data-ttu-id="73b84-134">這表示，您仍然可以利用宣告式以角色為基礎的安全性尾碼，然後在必要時，以程式設計的方式將它擴充到更精細的資料細微性層級。</span><span class="sxs-lookup"><span data-stu-id="73b84-134">This means that you can still take advantage of declarative role-based security where it suffices, and then you can programmatically extend it to a finer level of granularity when necessary.</span></span>

<span data-ttu-id="73b84-135">此外，當您使用以角色為基礎的安全性時，您可以透過程式設計方式存取您的元件呼叫鏈中所有上游呼叫端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="73b84-135">Additionally, when you use role-based security, you have programmatic access to information regarding all upstream callers in the chain of calls to your component.</span></span> <span data-ttu-id="73b84-136">當您想要保留詳細的審核記錄時，這特別有用。</span><span class="sxs-lookup"><span data-stu-id="73b84-136">This is especially useful when you want to keep a detailed audit trail.</span></span>

<span data-ttu-id="73b84-137">如需如何在程式碼中進行角色檢查，以及如何存取安全性呼叫內容資訊的說明，請參閱程式 [設計元件安全性](programmatic-component-security.md)。</span><span class="sxs-lookup"><span data-stu-id="73b84-137">For descriptions of how to do role checking in code and how to access security call context information, see [Programmatic Component Security](programmatic-component-security.md).</span></span>

## <a name="authorization-and-authentication"></a><span data-ttu-id="73b84-138">授權和驗證</span><span class="sxs-lookup"><span data-stu-id="73b84-138">Authorization and Authentication</span></span>

<span data-ttu-id="73b84-139">有意義的授權 presupposes，您確信用戶端實際上是他們所聲稱的身分。</span><span class="sxs-lookup"><span data-stu-id="73b84-139">Meaningful authorization presupposes that you are confident that clients are actually who they say they are.</span></span> <span data-ttu-id="73b84-140">驗證服務會分別處理用戶端身分識別的驗證。</span><span class="sxs-lookup"><span data-stu-id="73b84-140">The verification of client identity is handled separately by an authentication service.</span></span> <span data-ttu-id="73b84-141">在沒有驗證的情況下，基本上是讓呼叫者在接受系統上。</span><span class="sxs-lookup"><span data-stu-id="73b84-141">Without authentication, you are basically letting callers in on the honor system.</span></span> <span data-ttu-id="73b84-142">如需在影響 COM + 應用程式時進行驗證的說明，請參閱 [用戶端驗證](client-authentication.md)。</span><span class="sxs-lookup"><span data-stu-id="73b84-142">For descriptions of authentication as it impacts COM+ applications, see [Client Authentication](client-authentication.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="73b84-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="73b84-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73b84-144">有效設計角色</span><span class="sxs-lookup"><span data-stu-id="73b84-144">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="73b84-145">安全性界限</span><span class="sxs-lookup"><span data-stu-id="73b84-145">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="73b84-146">安全性呼叫內容資訊</span><span class="sxs-lookup"><span data-stu-id="73b84-146">Security Call Context Information</span></span>](security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="73b84-147">資訊安全內容屬性</span><span class="sxs-lookup"><span data-stu-id="73b84-147">Security Context Property</span></span>](security-context-property.md)
</dt> </dl>

 

 



