---
title: LegacySecureReferences
description: 判斷是否針對未呼叫 CoInitializeSecurity 的應用程式保護 AddRef/發行調用的安全。
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- LegacySecureReferences 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2776bf3661013f1e622bbc2e1c553f2551c62808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968642"
---
# <a name="legacysecurereferences"></a><span data-ttu-id="3e971-104">LegacySecureReferences</span><span class="sxs-lookup"><span data-stu-id="3e971-104">LegacySecureReferences</span></span>

<span data-ttu-id="3e971-105">判斷是否 / 針對未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的應用程式保護 AddRef **發行** 調用。</span><span class="sxs-lookup"><span data-stu-id="3e971-105">Determines whether **AddRef**/**Release** invocations are secured for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3e971-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="3e971-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a><span data-ttu-id="3e971-107">備註</span><span class="sxs-lookup"><span data-stu-id="3e971-107">Remarks</span></span>

<span data-ttu-id="3e971-108">這是 **REG \_ SZ** 值。</span><span class="sxs-lookup"><span data-stu-id="3e971-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="3e971-109">值為 ' Y ' 或 ' y ' 表示 **AddRef** 和 **發行** 是安全的。</span><span class="sxs-lookup"><span data-stu-id="3e971-109">A value of 'Y' or 'y' indicate that **AddRef** and **Release** are secured.</span></span> <span data-ttu-id="3e971-110">如果此登錄值不存在或設定為 ' Y ' 或 ' y ' 以外的值，則不會保護 **AddRef** 和 **發行** 。</span><span class="sxs-lookup"><span data-stu-id="3e971-110">If this registry value is not present or is set to a value other than 'Y' or 'y', **AddRef** and **Release** are not secured.</span></span> <span data-ttu-id="3e971-111">啟用安全參考會減緩遠端呼叫。</span><span class="sxs-lookup"><span data-stu-id="3e971-111">Enabling secure references slows remote calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e971-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e971-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e971-113">註冊 COM 伺服器</span><span class="sxs-lookup"><span data-stu-id="3e971-113">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="3e971-114">設定整個進程的安全性</span><span class="sxs-lookup"><span data-stu-id="3e971-114">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




