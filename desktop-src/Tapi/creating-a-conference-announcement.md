---
description: 下列程式碼片段說明如何建立簡單的會議公告。 此片段假設已經執行連接到 ILS 伺服器。
ms.assetid: d8ae90f3-37b0-4fc7-abf0-429f2bd97d66
title: 建立會議公告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f19deed2f002da5379cb8a44a02bd6543d4b36f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693823"
---
# <a name="creating-a-conference-announcement"></a><span data-ttu-id="30e1e-104">建立會議公告</span><span class="sxs-lookup"><span data-stu-id="30e1e-104">Creating a Conference Announcement</span></span>

<span data-ttu-id="30e1e-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="30e1e-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="30e1e-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="30e1e-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="30e1e-107">下列程式碼片段說明如何建立簡單的會議公告。</span><span class="sxs-lookup"><span data-stu-id="30e1e-107">The following code fragment illustrates the creation of a simple conference announcement.</span></span> <span data-ttu-id="30e1e-108">此片段假設已經執行 [連接到 ILS 伺服器](connecting-to-an-ils-server.md) 。</span><span class="sxs-lookup"><span data-stu-id="30e1e-108">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span>


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a><span data-ttu-id="30e1e-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="30e1e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30e1e-110">**ITDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="30e1e-110">**ITDirectoryObject**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[<span data-ttu-id="30e1e-111">修改已知會議</span><span class="sxs-lookup"><span data-stu-id="30e1e-111">Modifying a Known Conference</span></span>](modifying-a-known-conference.md)
</dt> <dt>

[<span data-ttu-id="30e1e-112">取得多播位址</span><span class="sxs-lookup"><span data-stu-id="30e1e-112">Acquiring a Multicast Address</span></span>](acquiring-a-multicast-address.md)
</dt> </dl>

 

 



