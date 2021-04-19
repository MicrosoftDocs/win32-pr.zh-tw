---
title: 64位 Windows 中的遠端登入存取
description: 登錄重新導向程式可透過 RegConnectRegistry 函式，在64位 Windows 上提供登錄的遠端存取。
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- 遠端登入存取 64-位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a139198ca08e0fdb9d7bcb070dcabf89dfa5403
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967482"
---
# <a name="remote-registry-access-in-64-bit-windows"></a><span data-ttu-id="de111-104">64位 Windows 中的遠端登入存取</span><span class="sxs-lookup"><span data-stu-id="de111-104">Remote Registry Access in 64-bit Windows</span></span>

<span data-ttu-id="de111-105">登錄重新導向程式可透過 [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) 函式，在64位 Windows 上提供登錄的遠端存取。</span><span class="sxs-lookup"><span data-stu-id="de111-105">The registry redirector provides remote access to the registry on 64-bit Windows through the [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) function.</span></span>

<span data-ttu-id="de111-106">如果用戶端是32位的應用程式，它會存取伺服器的預設32位登錄視圖。</span><span class="sxs-lookup"><span data-stu-id="de111-106">If the client is a 32-bit application, it accesses the server's default 32-bit registry view.</span></span> <span data-ttu-id="de111-107">如果用戶端是64位的應用程式，它會存取64位登錄視圖。</span><span class="sxs-lookup"><span data-stu-id="de111-107">If the client is a 64-bit application, it accesses the 64-bit registry view.</span></span>

<span data-ttu-id="de111-108">**Windows Server 2003：** 除非應用程式使用金鑰 \_ WOW64 32KEY 旗標，否則所有用戶端都會存取64位登錄視圖 \_ 。</span><span class="sxs-lookup"><span data-stu-id="de111-108">**Windows Server 2003:** All clients access the 64-bit registry view unless the application uses the KEY\_WOW64\_32KEY flag.</span></span> <span data-ttu-id="de111-109">此行為隨著 Windows Server 2003 Service Pack 1 (SP1) 和 Windows XP Professional x64 Edition 而變更，但前提是用戶端和伺服器都是執行這些版本的 Windows。</span><span class="sxs-lookup"><span data-stu-id="de111-109">This behavior changed with Windows Server 2003 with Service Pack 1 (SP1) and Windows XP Professional x64 Edition, provided that both the client and the server are running these versions of Windows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de111-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="de111-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de111-111">登錄重新導向程式</span><span class="sxs-lookup"><span data-stu-id="de111-111">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="de111-112">登錄反映</span><span class="sxs-lookup"><span data-stu-id="de111-112">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

 