---
title: InprocServer32
description: 註冊32位的同進程伺服器，並指定伺服器可以在其中執行之單元的執行緒模型。
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- InprocServer32 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daae9d495ad588e0dc710b63fe7d7ae9f48c11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507364"
---
# <a name="inprocserver32"></a><span data-ttu-id="31a44-104">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="31a44-104">InprocServer32</span></span>

<span data-ttu-id="31a44-105">註冊32位的同進程伺服器，並指定伺服器可以在其中執行之單元的執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="31a44-105">Registers a 32-bit in-process server and specifies the threading model of the apartment the server can run in.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="31a44-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="31a44-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a><span data-ttu-id="31a44-107">備註</span><span class="sxs-lookup"><span data-stu-id="31a44-107">Remarks</span></span>

<span data-ttu-id="31a44-108">**>threadingmodel** 是指定執行緒模型的 **REG \_ SZ** 值。</span><span class="sxs-lookup"><span data-stu-id="31a44-108">**ThreadingModel** is a **REG\_SZ** value the specifies the threading model.</span></span> <span data-ttu-id="31a44-109">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="31a44-109">The possible values are shown in the following table.</span></span>



| <span data-ttu-id="31a44-110">值</span><span class="sxs-lookup"><span data-stu-id="31a44-110">Value</span></span>     | <span data-ttu-id="31a44-111">描述</span><span class="sxs-lookup"><span data-stu-id="31a44-111">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="31a44-112">公寓</span><span class="sxs-lookup"><span data-stu-id="31a44-112">Apartment</span></span> | <span data-ttu-id="31a44-113">單一執行緒單元</span><span class="sxs-lookup"><span data-stu-id="31a44-113">Single-threaded apartment</span></span>                  |
| <span data-ttu-id="31a44-114">兩者</span><span class="sxs-lookup"><span data-stu-id="31a44-114">Both</span></span>      | <span data-ttu-id="31a44-115">單一執行緒或多執行緒單元</span><span class="sxs-lookup"><span data-stu-id="31a44-115">Single-threaded or multithreaded apartment</span></span> |
| <span data-ttu-id="31a44-116">免費</span><span class="sxs-lookup"><span data-stu-id="31a44-116">Free</span></span>      | <span data-ttu-id="31a44-117">多執行緒單元</span><span class="sxs-lookup"><span data-stu-id="31a44-117">Multithreaded apartment</span></span>                    |
| <span data-ttu-id="31a44-118">中性</span><span class="sxs-lookup"><span data-stu-id="31a44-118">Neutral</span></span>   | <span data-ttu-id="31a44-119">中立的單元</span><span class="sxs-lookup"><span data-stu-id="31a44-119">Neutral apartment</span></span>                          |



 

<span data-ttu-id="31a44-120">同進程伺服器所提供的每個物件都必須使用相同的值。</span><span class="sxs-lookup"><span data-stu-id="31a44-120">You must use the same value for every object provided by the in-process server.</span></span>

<span data-ttu-id="31a44-121">如果 **>threadingmodel** 不存在或未設定為值，則會將伺服器載入至在進程中初始化的第一個單元。</span><span class="sxs-lookup"><span data-stu-id="31a44-121">If **ThreadingModel** is not present or is not set to a value, the server is loaded into the first apartment that was initialized in the process.</span></span> <span data-ttu-id="31a44-122">此單元有時稱為主要單一執行緒的單元 (STA) 。</span><span class="sxs-lookup"><span data-stu-id="31a44-122">This apartment is sometimes referred to as the main single-threaded apartment (STA).</span></span> <span data-ttu-id="31a44-123">如果進程中的第一個 STA 是由 COM 初始化，而不是明確呼叫 [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)，就稱為主機 STA。</span><span class="sxs-lookup"><span data-stu-id="31a44-123">If the first STA in a process is initialized by COM, rather than by an explicit call to [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), it is called the host STA.</span></span> <span data-ttu-id="31a44-124">例如，如果要載入的內含式伺服器需要 STA 但進程中目前沒有 STA，COM 就會建立主機 STA。</span><span class="sxs-lookup"><span data-stu-id="31a44-124">For example, COM creates a host STA if an in-process server to be loaded requires an STA but there is currently no STA in the process.</span></span>

<span data-ttu-id="31a44-125">在可能的情況下，同進程伺服器會載入至載入它的用戶端所在的相同單元中。</span><span class="sxs-lookup"><span data-stu-id="31a44-125">Whenever possible, the in-process server is loaded in the same apartment as the client that loads it.</span></span> <span data-ttu-id="31a44-126">如果用戶端單元的執行緒模型與指定的模型不相容，則會載入伺服器，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="31a44-126">If the threading model of the client apartment is not compatible with the model specified, the server is loaded as indicated in the following table.</span></span>



| <span data-ttu-id="31a44-127">伺服器的執行緒模型</span><span class="sxs-lookup"><span data-stu-id="31a44-127">Threading model of server</span></span> | <span data-ttu-id="31a44-128">執行中的單元伺服器</span><span class="sxs-lookup"><span data-stu-id="31a44-128">Apartment server is run in</span></span> |
|---------------------------|----------------------------|
| <not specified>     | <span data-ttu-id="31a44-129">主要 STA</span><span class="sxs-lookup"><span data-stu-id="31a44-129">Main STA</span></span>                   |
| <span data-ttu-id="31a44-130">兩者</span><span class="sxs-lookup"><span data-stu-id="31a44-130">Both</span></span>                      | <span data-ttu-id="31a44-131">與用戶端相同的單元</span><span class="sxs-lookup"><span data-stu-id="31a44-131">Same apartment as client</span></span>   |
| <span data-ttu-id="31a44-132">免費</span><span class="sxs-lookup"><span data-stu-id="31a44-132">Free</span></span>                      | <span data-ttu-id="31a44-133">多執行緒單元</span><span class="sxs-lookup"><span data-stu-id="31a44-133">Multithreaded apartment</span></span>    |
| <span data-ttu-id="31a44-134">中性</span><span class="sxs-lookup"><span data-stu-id="31a44-134">Neutral</span></span>                   | <span data-ttu-id="31a44-135">中立的單元</span><span class="sxs-lookup"><span data-stu-id="31a44-135">Neutral apartment</span></span>          |



 

<span data-ttu-id="31a44-136">如果伺服器的執行緒模型為「單元」，則載入伺服器的單元取決於用戶端執行所在的部門，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="31a44-136">If the threading model of the server is Apartment, the apartment the server is loaded in depends on the apartment the client is running in, as indicated in the following table.</span></span>



| <span data-ttu-id="31a44-137">執行中的單元用戶端</span><span class="sxs-lookup"><span data-stu-id="31a44-137">Apartment client is run in</span></span> | <span data-ttu-id="31a44-138">執行中的單元伺服器</span><span class="sxs-lookup"><span data-stu-id="31a44-138">Apartment server is run in</span></span> |
|----------------------------|----------------------------|
| <span data-ttu-id="31a44-139">多執行緒</span><span class="sxs-lookup"><span data-stu-id="31a44-139">Multithreaded</span></span>              | <span data-ttu-id="31a44-140">主機 STA</span><span class="sxs-lookup"><span data-stu-id="31a44-140">Host STA</span></span>                   |
| <span data-ttu-id="31a44-141">STA 執行緒上的中性 () </span><span class="sxs-lookup"><span data-stu-id="31a44-141">Neutral (on STA thread)</span></span>    | <span data-ttu-id="31a44-142">與用戶端相同的單元</span><span class="sxs-lookup"><span data-stu-id="31a44-142">Same apartment as client</span></span>   |
| <span data-ttu-id="31a44-143">MTA 執行緒上的中性 () </span><span class="sxs-lookup"><span data-stu-id="31a44-143">Neutral (on MTA thread)</span></span>    | <span data-ttu-id="31a44-144">主機 STA</span><span class="sxs-lookup"><span data-stu-id="31a44-144">Host STA</span></span>                   |



 

<span data-ttu-id="31a44-145">COM 也可以建立主控制項多執行緒單元 (MTA) 。</span><span class="sxs-lookup"><span data-stu-id="31a44-145">COM can also create a host multithreaded apartment (MTA).</span></span> <span data-ttu-id="31a44-146">如果單一執行緒中的用戶端要求執行緒模型在進程中沒有 MTA 時為可用的同進程伺服器，COM 會建立主機 MTA 並將伺服器載入其中。</span><span class="sxs-lookup"><span data-stu-id="31a44-146">If a client in a single-threaded apartment requests an in-process server whose threading model is Free when there is no MTA in the process, COM creates a host MTA and loads the server into it.</span></span>

<span data-ttu-id="31a44-147">若為32位的同進程伺服器，則必須註冊 [**InprocHandler32**](inprochandler32.md)、 [**InprocServer**](inprocserver.md)、 **InprocServer32** 和可 [**插入**](insertable.md) 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="31a44-147">For a 32-bit in-process server, the [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InprocServer32**, and [**Insertable**](insertable.md) keys must be registered.</span></span> <span data-ttu-id="31a44-148">**InprocServer** 專案只是為了回溯相容性所需。</span><span class="sxs-lookup"><span data-stu-id="31a44-148">The **InprocServer** entry is needed only for backward compatibility.</span></span> <span data-ttu-id="31a44-149">如果遺漏，類別仍可運作，但無法在16位應用程式中載入。</span><span class="sxs-lookup"><span data-stu-id="31a44-149">If it is missing, the class still works but it cannot be loaded in 16-bit applications.</span></span>

<span data-ttu-id="31a44-150">如果容器正在搜尋內含式伺服器的登錄，16位版本的優先順序會和16位容器相同，且32位版本的優先順序會與32位容器相同。</span><span class="sxs-lookup"><span data-stu-id="31a44-150">If a container is searching the registry for an in-process server, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31a44-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="31a44-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31a44-152">**InprocServer**</span><span class="sxs-lookup"><span data-stu-id="31a44-152">**InprocServer**</span></span>](inprocserver.md)
</dt> </dl>

 

 




