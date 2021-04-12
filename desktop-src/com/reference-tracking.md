---
title: 參考追蹤
description: 參考追蹤
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45607a495e973ec33acde6d97cb1f83259a27c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463741"
---
# <a name="reference-tracking"></a><span data-ttu-id="95098-103">參考追蹤</span><span class="sxs-lookup"><span data-stu-id="95098-103">Reference Tracking</span></span>

<span data-ttu-id="95098-104">參考追蹤可以防止意外或惡意的物件早期發行版本。</span><span class="sxs-lookup"><span data-stu-id="95098-104">Reference tracking can prevent the unintentional or malicious early release of objects.</span></span>

<span data-ttu-id="95098-105">當您啟用參考追蹤時，會要求由 COM 驗證分散式 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 和 [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="95098-105">When you enable reference tracking, you are requesting that distributed [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) calls be authenticated by COM.</span></span> <span data-ttu-id="95098-106">啟用參考追蹤時，COM 會持續追蹤每個使用者的參考計數，讓使用者只能在使用者先前呼叫 **AddRef** 的物件上呼叫 **Release** 。</span><span class="sxs-lookup"><span data-stu-id="95098-106">When reference tracking is enabled, COM keeps track of per-user reference counts so that a user can call **Release** only on objects that the user previously called **AddRef** on.</span></span> <span data-ttu-id="95098-107">雖然參考追蹤可能會降低效能，但這可確保不論指定的使用者呼叫 **釋放** 多少次，如果其他人有參考，物件和存根仍會存在。</span><span class="sxs-lookup"><span data-stu-id="95098-107">Although reference tracking can decrease performance, it ensures that no matter how many times a given user calls **Release**, the objects and stubs will still exist if someone else has a reference to them.</span></span>

<span data-ttu-id="95098-108">用戶端可以藉由 \_ \_ 在 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的呼叫中傳遞 EOAC SECURE REFS 功能旗標，來設定進程的參考追蹤。</span><span class="sxs-lookup"><span data-stu-id="95098-108">The client can set reference tracking for a process by passing the EOAC\_SECURE\_REFS capability flag in a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="95098-109">您也可以使用 Dcomcnfg.exe 來啟用或停用電腦上所有應用程式的參考追蹤。</span><span class="sxs-lookup"><span data-stu-id="95098-109">You can also enable or disable reference tracking for all applications on a computer by using Dcomcnfg.exe.</span></span>

<span data-ttu-id="95098-110">如果已啟用參考追蹤， [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 一律會使用預設安全性設定。</span><span class="sxs-lookup"><span data-stu-id="95098-110">If reference tracking is enabled, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) always uses default security settings.</span></span> <span data-ttu-id="95098-111">在此情況下，對 **IUnknown** 的 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="95098-111">In this case, calls to [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) on **IUnknown** will fail.</span></span>

 

 