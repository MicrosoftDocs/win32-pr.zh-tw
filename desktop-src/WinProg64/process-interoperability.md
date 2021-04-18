---
title: 進程互通性
description: 您可以使用模擬層，在64位的 Windows 上執行 Win32 應用程式。 ARM 上的 Windows 10 包含 ARM64 的 x86 模擬層。 如需詳細資訊，請參閱執行32位應用程式。
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- 處理互通性64位 Windows 程式設計
- 互通性 64-位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023be0dafabfa8b17cf460542ae06467db517c11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106964973"
---
# <a name="process-interoperability"></a><span data-ttu-id="c7663-107">進程互通性</span><span class="sxs-lookup"><span data-stu-id="c7663-107">Process Interoperability</span></span>

<span data-ttu-id="c7663-108">您可以使用模擬層，在64位的 Windows 上執行 Win32 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c7663-108">You can run Win32-based applications on 64-bit Windows using an emulation layer.</span></span> <span data-ttu-id="c7663-109">ARM 上的 Windows 10 包含 ARM64 的 x86 模擬層。</span><span class="sxs-lookup"><span data-stu-id="c7663-109">Windows 10 on ARM includes an x86-on-ARM64 emulation layer.</span></span> <span data-ttu-id="c7663-110">如需詳細資訊，請參閱執行 [32 位應用程式](running-32-bit-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="c7663-110">For more information, see [Running 32-bit Applications](running-32-bit-applications.md).</span></span>

<span data-ttu-id="c7663-111">在64位的 Windows 上，64位進程無法 (DLL) 載入32位動態連結程式庫。</span><span class="sxs-lookup"><span data-stu-id="c7663-111">On 64-bit Windows, a 64-bit process cannot load a 32-bit dynamic-link library (DLL).</span></span> <span data-ttu-id="c7663-112">此外，32位進程無法載入64位 DLL。</span><span class="sxs-lookup"><span data-stu-id="c7663-112">Additionally, a 32-bit process cannot load a 64-bit DLL.</span></span> <span data-ttu-id="c7663-113">但是，64位 Windows 支援在64位和32位程式之間 (RPC) 的遠端程序呼叫， (同時在同一部電腦上與) 之間的電腦上。</span><span class="sxs-lookup"><span data-stu-id="c7663-113">However, 64-bit Windows supports remote procedure calls (RPC) between 64-bit and 32-bit processes (both on the same computer and across computers).</span></span> <span data-ttu-id="c7663-114">在64位的 Windows 上，跨進程的32位 COM 伺服器可以與64位用戶端通訊，而跨進程的64位 COM 伺服器則可以與32位用戶端通訊。</span><span class="sxs-lookup"><span data-stu-id="c7663-114">On 64-bit Windows, an out-of-process 32-bit COM server can communicate with a 64-bit client, and an out-of-process 64-bit COM server can communicate with a 32-bit client.</span></span> <span data-ttu-id="c7663-115">因此，如果您有一個不是 COM 感知的32位 DLL，您可以將它包裝在跨進程 COM 伺服器，並使用 COM 將呼叫封送處理至64位進程。</span><span class="sxs-lookup"><span data-stu-id="c7663-115">Therefore, if you have a 32-bit DLL that is not COM-aware, you can wrap it in an out-of-process COM server and use COM to marshal calls to and from a 64-bit process.</span></span>

<span data-ttu-id="c7663-116">同進程伺服器目前使用 **InprocServer** 登錄專案註冊。</span><span class="sxs-lookup"><span data-stu-id="c7663-116">In-process servers are currently registered using the **InprocServer** registry entry.</span></span> <span data-ttu-id="c7663-117">在64位的 Windows 上，64與32位的同進程伺服器應該使用 **InprocServer32** 專案。</span><span class="sxs-lookup"><span data-stu-id="c7663-117">On 64-bit Windows, 64- and 32-bit in-process servers should use the **InprocServer32** entry.</span></span>

<span data-ttu-id="c7663-118">如果通訊埠控制碼的本質是電腦的本機電腦，而且永遠不會使用在32位到64位界限上，請使用 **控制碼 \_ ptr** 類型，而不是 **INT \_ ptr** 或 **DWORD \_ ptr** 類型。</span><span class="sxs-lookup"><span data-stu-id="c7663-118">To port handles, which by their nature are local to the computer and would never be used across the 32-bit to 64-bit boundary, use the **HANDLE\_PTR** type instead of the **INT\_PTR** or **DWORD\_PTR** type.</span></span> <span data-ttu-id="c7663-119">這包括將這類控制碼傳遞為 **DWORD** 值的移植 RPC 介面。</span><span class="sxs-lookup"><span data-stu-id="c7663-119">This includes porting RPC interfaces passing such handles as **DWORD** values.</span></span> <span data-ttu-id="c7663-120">64位 **控制碼 \_ PTR** 是網路上的64位 (不會被截斷) ，因此不需要對應。</span><span class="sxs-lookup"><span data-stu-id="c7663-120">The 64-bit **HANDLE\_PTR** is 64 bits on the wire (not truncated) and thus does not need mapping.</span></span> <span data-ttu-id="c7663-121"> (32 位 **控制碼 \_ PTR** 是網路上的32位。 ) </span><span class="sxs-lookup"><span data-stu-id="c7663-121">(The 32-bit **HANDLE\_PTR** is 32 bits on the wire.)</span></span>

<span data-ttu-id="c7663-122">如需詳細資訊，請參閱 [設計與64位相容的介面](designing-64-bit-compatible-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="c7663-122">For more information, see [Designing 64-bit-Compatible Interfaces](designing-64-bit-compatible-interfaces.md).</span></span>

 

 




