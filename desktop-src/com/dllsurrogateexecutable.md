---
title: DllSurrogateExecutable
description: 讓 DLL 伺服器能夠在自訂的代理程式中執行，並與 DllSurrogate 登錄值搭配使用。 如果未指定 DllSurrogateExecutable，COM 會將 Null 傳遞為 CreateProcess 函數的第一個參數值。
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- DllSurrogateExecutable 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877297673b0a518006ecf903f447984f9023da34
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106978587"
---
# <a name="dllsurrogateexecutable"></a><span data-ttu-id="064a6-105">DllSurrogateExecutable</span><span class="sxs-lookup"><span data-stu-id="064a6-105">DllSurrogateExecutable</span></span>

<span data-ttu-id="064a6-106">讓 DLL 伺服器能夠在自訂的代理程式中執行，並與 [**DllSurrogate**](dllsurrogate.md) 登錄值搭配使用。</span><span class="sxs-lookup"><span data-stu-id="064a6-106">Enables DLL servers to run in a custom surrogate process, in conjunction with the [**DllSurrogate**](dllsurrogate.md) registry value.</span></span> <span data-ttu-id="064a6-107">如果未指定 **DllSurrogateExecutable** ，COM 會將 **Null** 傳遞為 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數的第一個參數值。</span><span class="sxs-lookup"><span data-stu-id="064a6-107">If **DllSurrogateExecutable** is not specified, COM passes **NULL** as the value for the first parameter of the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="064a6-108">登錄項目</span><span class="sxs-lookup"><span data-stu-id="064a6-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a><span data-ttu-id="064a6-109">備註</span><span class="sxs-lookup"><span data-stu-id="064a6-109">Remarks</span></span>

<span data-ttu-id="064a6-110">此值的型別為 **REG \_ SZ**。</span><span class="sxs-lookup"><span data-stu-id="064a6-110">This value is of type **REG\_SZ**.</span></span> <span data-ttu-id="064a6-111">它會與 [**DllSurrogate**](dllsurrogate.md) 值搭配使用，以避免在使用 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數時出現任何不明確的情況。</span><span class="sxs-lookup"><span data-stu-id="064a6-111">It works in conjunction with the [**DllSurrogate**](dllsurrogate.md) value to prevent any ambiguity when using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span> <span data-ttu-id="064a6-112">**DllSurrogate** 指出是否需要使用自訂代理，並將此資訊當做 **CreateProcess** 的第一個參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="064a6-112">**DllSurrogate** indicates whether a custom surrogate needs to be used, and this information is passed as the first parameter for **CreateProcess**.</span></span> <span data-ttu-id="064a6-113">根據 **CreateProcess** 的執行，這項資訊可能不明確。</span><span class="sxs-lookup"><span data-stu-id="064a6-113">Depending on the implementation of **CreateProcess**, this information might be ambiguous.</span></span> <span data-ttu-id="064a6-114">如果指定 **DllSurrogateExecutable** ，COM 會將此值傳遞為 **CreateProcess** 的第一個參數。</span><span class="sxs-lookup"><span data-stu-id="064a6-114">If **DllSurrogateExecutable** is specified, COM passes the value as the first parameter of **CreateProcess**.</span></span> <span data-ttu-id="064a6-115">如果未指定 **DllSurrogateExecutable** ，COM 會傳遞 **Null** 做為 **CreateProcess** 第一個參數的值。</span><span class="sxs-lookup"><span data-stu-id="064a6-115">If **DllSurrogateExecutable** is not specified, COM passes **NULL** as the value for the first parameter of **CreateProcess**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="064a6-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="064a6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="064a6-117">**CoRegisterSurrogate**</span><span class="sxs-lookup"><span data-stu-id="064a6-117">**CoRegisterSurrogate**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[<span data-ttu-id="064a6-118">DLL 代理</span><span class="sxs-lookup"><span data-stu-id="064a6-118">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> <dt>

[<span data-ttu-id="064a6-119">**DllSurrogate**</span><span class="sxs-lookup"><span data-stu-id="064a6-119">**DllSurrogate**</span></span>](dllsurrogate.md)
</dt> <dt>

[<span data-ttu-id="064a6-120">**ISurrogate**</span><span class="sxs-lookup"><span data-stu-id="064a6-120">**ISurrogate**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 