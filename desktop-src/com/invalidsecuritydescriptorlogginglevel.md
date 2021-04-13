---
title: InvalidSecurityDescriptorLoggingLevel
description: 針對元件啟動和存取權限的無效安全描述項，設定事件記錄檔專案的詳細資訊。
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- InvalidSecurityDescriptorLoggingLevel 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ac333a7cb8b54f383f93a71131cbb0a9314466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300019"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a><span data-ttu-id="3cf6e-104">InvalidSecurityDescriptorLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="3cf6e-104">InvalidSecurityDescriptorLoggingLevel</span></span>

<span data-ttu-id="3cf6e-105">針對元件啟動和存取權限的無效安全描述項，設定事件記錄檔專案的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3cf6e-105">Sets the verbosity of event log entries about invalid security descriptors for component launch and access permissions.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3cf6e-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="3cf6e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="3cf6e-107">備註</span><span class="sxs-lookup"><span data-stu-id="3cf6e-107">Remarks</span></span>

<span data-ttu-id="3cf6e-108">這是 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="3cf6e-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="3cf6e-109">值</span><span class="sxs-lookup"><span data-stu-id="3cf6e-109">Value</span></span> | <span data-ttu-id="3cf6e-110">描述</span><span class="sxs-lookup"><span data-stu-id="3cf6e-110">Description</span></span>                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf6e-111">1</span><span class="sxs-lookup"><span data-stu-id="3cf6e-111">1</span></span>     | <span data-ttu-id="3cf6e-112">當 COM 找到不正確安全描述項時，一律會記錄失敗。</span><span class="sxs-lookup"><span data-stu-id="3cf6e-112">Always log failures when COM finds an invalid security descriptor.</span></span> <span data-ttu-id="3cf6e-113">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="3cf6e-113">This is the default value.</span></span>                                                                                  |
| <span data-ttu-id="3cf6e-114">2</span><span class="sxs-lookup"><span data-stu-id="3cf6e-114">2</span></span>     | <span data-ttu-id="3cf6e-115">當 COM 找不到不正確安全描述項時，永遠不會記錄失敗。</span><span class="sxs-lookup"><span data-stu-id="3cf6e-115">Never log failures when COM finds an invalid security descriptor.</span></span> <span data-ttu-id="3cf6e-116">不建議您停用事件記錄，因為它可以讓您更難診斷問題。</span><span class="sxs-lookup"><span data-stu-id="3cf6e-116">It is not recommended that you disable event logging, as it can make it more difficult to diagnose problems.</span></span> |



 

<span data-ttu-id="3cf6e-117">如果您將啟動和存取權限安全描述項 (通常稱為 Acl) 直接，則可以建立其意義無法明確解讀的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="3cf6e-117">If you set launch and access permission security descriptors (commonly called ACLs) directly, it is possible to construct a security descriptor whose meaning cannot be interpreted unambiguously.</span></span> <span data-ttu-id="3cf6e-118">當 COM 遇到這類不正確安全描述項時，會產生事件記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="3cf6e-118">COM makes an event log entry when it encounters such an invalid security descriptor.</span></span>

<span data-ttu-id="3cf6e-119">請注意， [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) 和 [**CallFailureLoggingLevel**](callfailurelogginglevel.md) 無法控制記錄不正確安全描述項錯誤。</span><span class="sxs-lookup"><span data-stu-id="3cf6e-119">Note that [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) and [**CallFailureLoggingLevel**](callfailurelogginglevel.md) have no control over logging invalid security descriptor errors.</span></span> <span data-ttu-id="3cf6e-120">使用 **InvalidSecurityDescriptorLoggingLevel** 可完整控制此功能。</span><span class="sxs-lookup"><span data-stu-id="3cf6e-120">Use **InvalidSecurityDescriptorLoggingLevel** for full control over this functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cf6e-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="3cf6e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cf6e-122">設定 COM 應用程式的安全性</span><span class="sxs-lookup"><span data-stu-id="3cf6e-122">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




