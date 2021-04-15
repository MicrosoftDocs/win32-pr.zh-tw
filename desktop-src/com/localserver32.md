---
title: LocalServer32
description: 指定32位本機伺服器應用程式的完整路徑。
ms.assetid: 5d922230-f53d-4bf9-be50-c8c00f45b7a8
keywords:
- LocalServer32 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd068f51f33b6c283384198c0206bc9c3b6357f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104508167"
---
# <a name="localserver32"></a><span data-ttu-id="e84d4-104">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="e84d4-104">LocalServer32</span></span>

<span data-ttu-id="e84d4-105">指定32位本機伺服器應用程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e84d4-105">Specifies the full path to a 32-bit local server application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e84d4-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="e84d4-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer32
         (Default) = path
         ServerExecutable = path
```

## <a name="remarks"></a><span data-ttu-id="e84d4-107">備註</span><span class="sxs-lookup"><span data-stu-id="e84d4-107">Remarks</span></span>

<span data-ttu-id="e84d4-108">從 Windows Server 2003 開始， **ServerExecutable** 值的類型是 **REG \_ SZ** 且支援的值，可搭配 **LocalServer32** 子機碼使用，以避免在使用 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數時出現任何混淆。</span><span class="sxs-lookup"><span data-stu-id="e84d4-108">The **ServerExecutable** value, which is of type **REG\_SZ** and is supported starting with Windows Server 2003, works in conjunction with the **LocalServer32** subkey to prevent any ambiguity when using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span> <span data-ttu-id="e84d4-109">**LocalServer32** 指定要啟動的 COM 伺服器應用程式的位置，這項資訊會以 **CreateProcess** 的第一個參數 *lpApplicationName* 來傳遞。</span><span class="sxs-lookup"><span data-stu-id="e84d4-109">**LocalServer32** specifies the location of the COM server application to launch, and this information is passed as the first parameter *lpApplicationName* for **CreateProcess**.</span></span> <span data-ttu-id="e84d4-110">根據 **CreateProcess** 的執行，這項資訊可能不明確。</span><span class="sxs-lookup"><span data-stu-id="e84d4-110">Depending on the implementation of **CreateProcess**, this information might be ambiguous.</span></span> <span data-ttu-id="e84d4-111">基於這個理由，如果指定 **ServerExecutable** ，COM 會將 **ServerExecutable** 的命名值傳遞給 **CreateProcess** 的 *lpApplicationName* 參數。</span><span class="sxs-lookup"><span data-stu-id="e84d4-111">For this reason, if **ServerExecutable** is specified, COM passes the **ServerExecutable** named value to the *lpApplicationName* parameter of **CreateProcess**.</span></span> <span data-ttu-id="e84d4-112">如果未指定 **ServerExecutable** ，COM 會傳遞 **Null** 做為 **CreateProcess** 第一個參數的值。</span><span class="sxs-lookup"><span data-stu-id="e84d4-112">If **ServerExecutable** is not specified, COM passes **NULL** as the value for the first parameter of **CreateProcess**.</span></span>

<span data-ttu-id="e84d4-113">若要協助提供系統安全性，請在路徑中使用加上引號的字串，以指出可執行檔尾和引數的開始位置。</span><span class="sxs-lookup"><span data-stu-id="e84d4-113">To help provide system security, use quoted strings in the path to indicate where the executable filename ends and the arguments begin.</span></span> <span data-ttu-id="e84d4-114">例如，不要將下列路徑指定為 **LocalServer32** 專案：</span><span class="sxs-lookup"><span data-stu-id="e84d4-114">For example, instead of specifying the following path as the **LocalServer32** entry:</span></span>

<span data-ttu-id="e84d4-115">"C： \\ Program files \\ Company files \\Application.exe param1 param2"</span><span class="sxs-lookup"><span data-stu-id="e84d4-115">"C:\\Program Files\\Company Files\\Application.exe param1 param2"</span></span>

<span data-ttu-id="e84d4-116">使用下列語法指定路徑：</span><span class="sxs-lookup"><span data-stu-id="e84d4-116">specify the path using the following syntax:</span></span>

<span data-ttu-id="e84d4-117">" \\ " C： \\ Program Files \\ Company files \\Application.exe\\ "param1 param2"</span><span class="sxs-lookup"><span data-stu-id="e84d4-117">"\\"C:\\Program Files\\Company Files\\Application.exe\\" param1 param2"</span></span>

<span data-ttu-id="e84d4-118">COM 會將 "-內嵌" 旗標附加至字串，因此使用旗標的應用程式需要剖析整個字串並檢查內嵌旗標。</span><span class="sxs-lookup"><span data-stu-id="e84d4-118">COM appends the "-Embedding" flag to the string, so the application that uses flags needs to parse the whole string and check for the -Embedding flag.</span></span>

<span data-ttu-id="e84d4-119">當 COM 啟動32位本機伺服器時，伺服器必須在使用者所設定的經過時間內註冊類別物件。</span><span class="sxs-lookup"><span data-stu-id="e84d4-119">When COM starts a 32-bit local server, the server must register a class object within an elapsed time set by the user.</span></span> <span data-ttu-id="e84d4-120">根據預設，經過時間值必須至少為5分鐘（以毫秒為單位），但不能超過30天的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="e84d4-120">By default, the elapsed time value must be at least 5 minutes, in milliseconds, but cannot exceed the number of milliseconds in 30 days.</span></span> <span data-ttu-id="e84d4-121">應用程式通常不應設定此值，其位於 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ COM2 \\ ServerStartElapsedTime** 專案中。</span><span class="sxs-lookup"><span data-stu-id="e84d4-121">Applications typically should not set this value, which is in the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\COM2\\ServerStartElapsedTime** entry.</span></span>

<span data-ttu-id="e84d4-122">32位本機伺服器的必要專案為 [**InprocHandler32**](inprochandler32.md)、 [**LocalServer**](localserver.md)、 **LocalServer32** 和可 [**插入**](insertable.md)。</span><span class="sxs-lookup"><span data-stu-id="e84d4-122">The required entries for 32-bit local servers are [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32**, and [**Insertable**](insertable.md).</span></span>

<span data-ttu-id="e84d4-123">如果容器正在搜尋本機伺服器的登錄，則32位本機伺服器的優先順序會高於16位本機伺服器。</span><span class="sxs-lookup"><span data-stu-id="e84d4-123">If a container is searching the registry for a local server, a 32-bit local server has priority over a 16-bit local server.</span></span>

<span data-ttu-id="e84d4-124">如果您要將類別實作為服務，您應該要注意， [**LocalService**](localservice.md) 名稱值是用於本機和遠端啟用之 **LocalServer32** 索引鍵的喜好設定。如果 **LocalService** 存在且參考有效的服務，則會忽略 **LocalServer32** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="e84d4-124">If you are implementing classes as services, you should be aware that the [**LocalService**](localservice.md) named value is used in preference to the **LocalServer32** key for local and remote activation requestsâ€”if **LocalService** exists and refers to a valid service, the **LocalServer32** key is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e84d4-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="e84d4-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e84d4-126">**LocalServer**</span><span class="sxs-lookup"><span data-stu-id="e84d4-126">**LocalServer**</span></span>](localserver.md)
</dt> <dt>

[<span data-ttu-id="e84d4-127">**LocalService**</span><span class="sxs-lookup"><span data-stu-id="e84d4-127">**LocalService**</span></span>](localservice.md)
</dt> </dl>

 

 