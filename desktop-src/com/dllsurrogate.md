---
title: DllSurrogate
description: 讓 DLL 伺服器在代理進程中執行。 如果指定了空字串，則會使用系統提供的代理;否則，此值會指定要使用的代理路徑。
ms.assetid: ae02d828-9cdb-4faa-8fa9-971da97e27b1
keywords:
- DllSurrogate 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9854f3c4e4390d64d97c8ab829ac2e7fe34488e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382954"
---
# <a name="dllsurrogate"></a><span data-ttu-id="38bc1-105">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="38bc1-105">DllSurrogate</span></span>

<span data-ttu-id="38bc1-106">讓 DLL 伺服器在代理進程中執行。</span><span class="sxs-lookup"><span data-stu-id="38bc1-106">Enables DLL servers to run in a surrogate process.</span></span> <span data-ttu-id="38bc1-107">如果指定了空字串，則會使用系統提供的代理;否則，此值會指定要使用的代理路徑。</span><span class="sxs-lookup"><span data-stu-id="38bc1-107">If an empty string is specified, the system-supplied surrogate is used; otherwise, the value specifies the path of the surrogate to be used.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="38bc1-108">登錄項目</span><span class="sxs-lookup"><span data-stu-id="38bc1-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogate = path
```

## <a name="remarks"></a><span data-ttu-id="38bc1-109">備註</span><span class="sxs-lookup"><span data-stu-id="38bc1-109">Remarks</span></span>

<span data-ttu-id="38bc1-110">這是 **REG \_ SZ** 值，可指定類別是要在代理程式中啟動的 DLL，以及要使用的代理程式。</span><span class="sxs-lookup"><span data-stu-id="38bc1-110">This is a **REG\_SZ** value that specifies that the class is a DLL that is to be activated in a surrogate process, and the surrogate process to be used.</span></span> <span data-ttu-id="38bc1-111">若要使用系統提供的一般代理進程，請將 *路徑* 設定為空字串或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="38bc1-111">To use the system-supplied generic surrogate process, set *path* to an empty string or **NULL**.</span></span> <span data-ttu-id="38bc1-112">若要指定其他代理程式，請將 *路徑* 設定為代理的路徑。</span><span class="sxs-lookup"><span data-stu-id="38bc1-112">To specify another surrogate process, set *path* to the path of the surrogate.</span></span> <span data-ttu-id="38bc1-113">如同 [**LocalServer32**](localserver32.md) 機碼下伺服器的路徑規格，不需要完整路徑規格。</span><span class="sxs-lookup"><span data-stu-id="38bc1-113">As in the specification of the path of a server under the [**LocalServer32**](localserver32.md) key, a full path specification is not necessary.</span></span> <span data-ttu-id="38bc1-114">必須撰寫代理，才能與 DCOM 服務正確地通訊，如 [撰寫自訂代理](writing-a-custom-surrogate.md)所述。</span><span class="sxs-lookup"><span data-stu-id="38bc1-114">The surrogate must be written to properly communicate with the DCOM service as described in [Writing a Custom Surrogate](writing-a-custom-surrogate.md).</span></span>

<span data-ttu-id="38bc1-115">必須要有 **DllSurrogate** 值，才能在代理程式中啟用 DLL 伺服器。</span><span class="sxs-lookup"><span data-stu-id="38bc1-115">The **DllSurrogate** value must be present for a DLL server to be activated in a surrogate.</span></span> <span data-ttu-id="38bc1-116">啟用指的是呼叫 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)、 [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)、 **CoCreateInstanceEx**、 [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)、 [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)或 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)。</span><span class="sxs-lookup"><span data-stu-id="38bc1-116">Activation refers to a call to [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **CoCreateInstanceEx**, [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage), or [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span></span> <span data-ttu-id="38bc1-117">在代理程式中執行 Dll 提供可執行檔的優點，包括錯誤隔離、同時提供多個用戶端的能力，以及允許伺服器在分散式環境中提供服務給遠端用戶端。</span><span class="sxs-lookup"><span data-stu-id="38bc1-117">Running DLLs in a surrogate process provides the benefits of an executable implementation, including fault isolation, the ability to serve multiple clients simultaneously, and allowing the server to provide services to remote clients in a distributed environment.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38bc1-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="38bc1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38bc1-119">**CoRegisterSurrogate**</span><span class="sxs-lookup"><span data-stu-id="38bc1-119">**CoRegisterSurrogate**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[<span data-ttu-id="38bc1-120">DLL 代理</span><span class="sxs-lookup"><span data-stu-id="38bc1-120">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> <dt>

[<span data-ttu-id="38bc1-121">**DllSurrogateExecutable**</span><span class="sxs-lookup"><span data-stu-id="38bc1-121">**DllSurrogateExecutable**</span></span>](dllsurrogateexecutable.md)
</dt> <dt>

[<span data-ttu-id="38bc1-122">**ISurrogate**</span><span class="sxs-lookup"><span data-stu-id="38bc1-122">**ISurrogate**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 