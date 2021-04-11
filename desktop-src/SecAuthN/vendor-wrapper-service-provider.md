---
description: 廠商包裝函式的目的是要封裝並使用智慧卡製造商 (提供的低層級 COM 介面) 用於特定智慧卡。 這些介面不是由 Microsoft 提供。
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: 廠商包裝函式服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b7d22fea8e450111e1611f2ec069697c229a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112789"
---
# <a name="vendor-wrapper-service-provider"></a><span data-ttu-id="68f7e-104">廠商包裝函式服務提供者</span><span class="sxs-lookup"><span data-stu-id="68f7e-104">Vendor Wrapper Service Provider</span></span>

<span data-ttu-id="68f7e-105">廠商包裝函式的目的是要封裝並使用智慧卡製造商 (提供的低層級 COM 介面) 用於特定智慧卡。</span><span class="sxs-lookup"><span data-stu-id="68f7e-105">The purpose of the vendor wrapper is to encapsulate and use the low-level COM interfaces (supplied by the smart card manufacturers) for a particular smart card.</span></span> <span data-ttu-id="68f7e-106">這些介面不是由 Microsoft 提供。</span><span class="sxs-lookup"><span data-stu-id="68f7e-106">These interfaces are not supplied by Microsoft.</span></span>

![廠商包裝函式](images/scspart1.png)

<span data-ttu-id="68f7e-108">如 *ICCs 和個人電腦系統之互通性規格* 的第6部分所述 (請參閱) 的規格 [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ，此包裝函式所公開的功能比四個不同服務提供者的功能更容易使用。</span><span class="sxs-lookup"><span data-stu-id="68f7e-108">As described in part 6 of the *Interoperability Specification for ICCs and Personal Computer Systems* (see specifications at [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/)), the functionality exposed by this wrapper is easier to use than the functionality of four separate service providers.</span></span> <span data-ttu-id="68f7e-109">包裝函式的功能可以分成四個主要區域：</span><span class="sxs-lookup"><span data-stu-id="68f7e-109">The wrapper's functionality can be divided into four main areas:</span></span>

-   <span data-ttu-id="68f7e-110">智慧卡驗證服務，例如取得挑戰和卡片驗證。</span><span class="sxs-lookup"><span data-stu-id="68f7e-110">Smart card authentication services, such as get challenge and card authentication.</span></span>
-   <span data-ttu-id="68f7e-111">智慧卡檔案存取或檔案系統服務，例如開啟、關閉、讀取及寫入。</span><span class="sxs-lookup"><span data-stu-id="68f7e-111">Smart card file access or file system services, such as open, close, read, and write.</span></span>
-   <span data-ttu-id="68f7e-112">智慧卡管理，例如附加和卸離。</span><span class="sxs-lookup"><span data-stu-id="68f7e-112">Smart card management, such as attach and detach.</span></span>
-   <span data-ttu-id="68f7e-113">智慧卡驗證服務，例如驗證及變更程式碼。</span><span class="sxs-lookup"><span data-stu-id="68f7e-113">Smart card verification services, such as verify and change code.</span></span>

> [!Note]  
> <span data-ttu-id="68f7e-114">某些語言和國家或地區可能無法使用此規格。</span><span class="sxs-lookup"><span data-stu-id="68f7e-114">This specification may not be available in some languages and countries or regions.</span></span>

 

<span data-ttu-id="68f7e-115">這項功能僅適用于使用的卡片類型 (該卡片支援的功能、通訊協定等) ，而且每張卡片都有不同的功能。</span><span class="sxs-lookup"><span data-stu-id="68f7e-115">The functionality is specific to the type of card being used (which functions the card supports, protocols, and so on) and will be different for each card.</span></span>

<span data-ttu-id="68f7e-116">Microsoft SCardCOM 範例包裝函式會使用 ATL COM 程式庫來執行簡單的包裝函式，並為其他包裝函式配置範本。</span><span class="sxs-lookup"><span data-stu-id="68f7e-116">The Microsoft SCardCOM example wrapper uses the ATL COM library to implement a simple wrapper and lay down a template for other wrappers.</span></span> <span data-ttu-id="68f7e-117">它會執行下列介面。</span><span class="sxs-lookup"><span data-stu-id="68f7e-117">It implements the following interfaces.</span></span>



| <span data-ttu-id="68f7e-118">介面或物件</span><span class="sxs-lookup"><span data-stu-id="68f7e-118">Interface or object</span></span>                                     | <span data-ttu-id="68f7e-119">Description</span><span class="sxs-lookup"><span data-stu-id="68f7e-119">Description</span></span>                         |
|---------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="68f7e-120">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="68f7e-120">**ISCardAuth**</span></span>](iscardauth.md)<br/>             | <span data-ttu-id="68f7e-121">驗證服務。</span><span class="sxs-lookup"><span data-stu-id="68f7e-121">Authentication services.</span></span><br/> |
| [<span data-ttu-id="68f7e-122">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="68f7e-122">**ISCardFileAccess**</span></span>](iscardfileaccess.md)<br/> | <span data-ttu-id="68f7e-123">檔案系統服務。</span><span class="sxs-lookup"><span data-stu-id="68f7e-123">File system services.</span></span><br/>    |
| [<span data-ttu-id="68f7e-124">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="68f7e-124">**ISCardManage**</span></span>](iscardmanage.md)<br/>         | <span data-ttu-id="68f7e-125">管理服務。</span><span class="sxs-lookup"><span data-stu-id="68f7e-125">Management services.</span></span><br/>     |
| [<span data-ttu-id="68f7e-126">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="68f7e-126">**ISCardVerify**</span></span>](iscardverify.md)<br/>         | <span data-ttu-id="68f7e-127">驗證服務。</span><span class="sxs-lookup"><span data-stu-id="68f7e-127">Verification services.</span></span><br/>   |



 

> [!Note]  
> <span data-ttu-id="68f7e-128">SCardCOM 範例僅提供作為執行包裝函式介面的範例。</span><span class="sxs-lookup"><span data-stu-id="68f7e-128">The SCardCOM example is provided only as an example of implementing the wrapper interfaces.</span></span> <span data-ttu-id="68f7e-129">若要避免與其他廠商產生 DLL 名稱衝突，您不能使用 SCardCOM.dll 做為您所建立之任何 Dll 的名稱。</span><span class="sxs-lookup"><span data-stu-id="68f7e-129">To prevent DLL name collision with other vendors, you must not use SCardCOM.dll as the name of any DLLs you create.</span></span>

 

<span data-ttu-id="68f7e-130">以下是廠商包裝函式的典型用法。</span><span class="sxs-lookup"><span data-stu-id="68f7e-130">Following is a typical use of the vendor wrapper.</span></span> <span data-ttu-id="68f7e-131">這個範例會使用 [**ISCardManage**](iscardmanage.md) 介面來建立將包裝到服務提供者的介面實例，以及用來驗證其作業的 [**ISCardVerify**](iscardverify.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="68f7e-131">This example uses the [**ISCardManage**](iscardmanage.md) interface to create instances of the interfaces that will be wrapped into the service provider and the [**ISCardVerify**](iscardverify.md) interface to verify their operation.</span></span>

<span data-ttu-id="68f7e-132">**若要建立包裝函式服務提供者**</span><span class="sxs-lookup"><span data-stu-id="68f7e-132">**To build a wrapper service provider**</span></span>

1.  <span data-ttu-id="68f7e-133">建立 [**ISCardManage**](iscardmanage.md) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="68f7e-133">Create an instance of the [**ISCardManage**](iscardmanage.md) interface.</span></span> <span data-ttu-id="68f7e-134">您可以使用此介面來建立必要介面 (實例，例如 [**ISCardFileAccess**](iscardfileaccess.md) 或 [**ISCardVerify**](iscardverify.md)) 。</span><span class="sxs-lookup"><span data-stu-id="68f7e-134">Use this interface to create an instance of required interfaces (for example, [**ISCardFileAccess**](iscardfileaccess.md) or [**ISCardVerify**](iscardverify.md)).</span></span> <span data-ttu-id="68f7e-135">建立這些介面時，也會建立任何對應的低層級 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="68f7e-135">When creating these interfaces, any corresponding low-level COM interfaces would also be created.</span></span>
2.  <span data-ttu-id="68f7e-136">透過適當的 [**ISCardManage**](iscardmanage.md) 方法來連接或連接到卡片。</span><span class="sxs-lookup"><span data-stu-id="68f7e-136">Attach/connect to a card through the appropriate [**ISCardManage**](iscardmanage.md) method.</span></span>
3.  <span data-ttu-id="68f7e-137">透過適當的 [**ISCardVerify**](iscardverify.md) 方法執行所需的作業 (這可能會呼叫多個低層級的 COM 介面和方法，以完成) 。</span><span class="sxs-lookup"><span data-stu-id="68f7e-137">Perform required operations through the appropriate [**ISCardVerify**](iscardverify.md) method (which may call multiple low-level COM interfaces and methods to complete).</span></span>
4.  <span data-ttu-id="68f7e-138">針對其他作業重複執行。</span><span class="sxs-lookup"><span data-stu-id="68f7e-138">Repeat for other operations.</span></span>
5.  <span data-ttu-id="68f7e-139">完成時釋放。</span><span class="sxs-lookup"><span data-stu-id="68f7e-139">Release when complete.</span></span>

<span data-ttu-id="68f7e-140">COM 介面名稱和介面識別碼 (GUID) 不應該從程式碼或範例包裝函式中所使用的識別碼變更。</span><span class="sxs-lookup"><span data-stu-id="68f7e-140">The COM interface name and interface identifier (GUID) should not change from those used in the code or example wrapper.</span></span> <span data-ttu-id="68f7e-141">不過，類別 GUID (也就是，介面的實際實作為所在的) 必須從使用的位置進行變更。</span><span class="sxs-lookup"><span data-stu-id="68f7e-141">However, the class GUID (that is, where an actual implementation of an interface resides) must be changed from those used.</span></span> <span data-ttu-id="68f7e-142">這在執行廠商包裝函式時特別重要。</span><span class="sxs-lookup"><span data-stu-id="68f7e-142">This is especially important when implementing a vendor wrapper.</span></span> <span data-ttu-id="68f7e-143">其中一個範例是在特定電腦上使用多個廠商包裝函式。</span><span class="sxs-lookup"><span data-stu-id="68f7e-143">One example would be using multiple vendor wrappers on a particular computer.</span></span> <span data-ttu-id="68f7e-144">這些包裝函式應該會執行相同的 COM 介面，但一律會使用不同的執行策略。</span><span class="sxs-lookup"><span data-stu-id="68f7e-144">These wrappers should implement the same COM interfaces, but will always use different implementation strategies.</span></span> <span data-ttu-id="68f7e-145">因此，需要不同的類別 (和類別識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="68f7e-145">Therefore, different classes (and class IDs) are required.</span></span>

 

 




