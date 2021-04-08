---
title: CallFailureLoggingLevel
description: 設定有關元件呼叫失敗的事件記錄檔專案詳細程度。
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- CallFailureLoggingLevel 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4432f21f333d5aa5f8b3cebbd6f0fa339cf0f13a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839771"
---
# <a name="callfailurelogginglevel"></a><span data-ttu-id="9a6cd-104">CallFailureLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="9a6cd-104">CallFailureLoggingLevel</span></span>

<span data-ttu-id="9a6cd-105">設定有關元件呼叫失敗的事件記錄檔專案詳細程度。</span><span class="sxs-lookup"><span data-stu-id="9a6cd-105">Sets the verbosity of event log entries about failed calls to components.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="9a6cd-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="9a6cd-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="9a6cd-107">備註</span><span class="sxs-lookup"><span data-stu-id="9a6cd-107">Remarks</span></span>

<span data-ttu-id="9a6cd-108">這是 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="9a6cd-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="9a6cd-109">值</span><span class="sxs-lookup"><span data-stu-id="9a6cd-109">Value</span></span> | <span data-ttu-id="9a6cd-110">描述</span><span class="sxs-lookup"><span data-stu-id="9a6cd-110">Description</span></span>                                                                            |
|-------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a6cd-111">1</span><span class="sxs-lookup"><span data-stu-id="9a6cd-111">1</span></span>     | <span data-ttu-id="9a6cd-112">在 COM 伺服器進程中進行呼叫時，一律會記錄失敗。</span><span class="sxs-lookup"><span data-stu-id="9a6cd-112">Always log failures during a call in the COM Server process.</span></span>                           |
| <span data-ttu-id="9a6cd-113">2</span><span class="sxs-lookup"><span data-stu-id="9a6cd-113">2</span></span>     | <span data-ttu-id="9a6cd-114">絕對不要在 COM 伺服器進程的呼叫期間記錄失敗。</span><span class="sxs-lookup"><span data-stu-id="9a6cd-114">Never log failures during a call in the COM Server process.</span></span> <span data-ttu-id="9a6cd-115">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="9a6cd-115">This is the default value.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9a6cd-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="9a6cd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a6cd-117">設定 COM 應用程式的安全性</span><span class="sxs-lookup"><span data-stu-id="9a6cd-117">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




