---
description: 下列程式碼片段說明指定的 ILS 伺服器上的會議列舉。 此片段假設已經執行連接到 ILS 伺服器。
ms.assetid: da01c534-c700-4b4f-ac22-cede9930f80d
title: 列舉會議目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eedffb44d92f52293dc9d1add8b53588503282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469292"
---
# <a name="enumerating-conference-directories"></a><span data-ttu-id="71c84-104">列舉會議目錄</span><span class="sxs-lookup"><span data-stu-id="71c84-104">Enumerating Conference Directories</span></span>

<span data-ttu-id="71c84-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="71c84-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="71c84-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="71c84-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="71c84-107">下列程式碼片段說明指定的 ILS 伺服器上的會議列舉。</span><span class="sxs-lookup"><span data-stu-id="71c84-107">The following code fragment illustrates the enumeration of conferences on a specified ILS server.</span></span> <span data-ttu-id="71c84-108">此片段假設已經執行 [連接到 ILS 伺服器](connecting-to-an-ils-server.md) 。</span><span class="sxs-lookup"><span data-stu-id="71c84-108">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span>


```C++
SysFreeString( bNameToSearch );
```



## <a name="related-topics"></a><span data-ttu-id="71c84-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="71c84-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71c84-110">**IEnumDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="71c84-110">**IEnumDirectoryObject**</span></span>](/windows/desktop/api/Rend/nn-rend-ienumdirectoryobject)
</dt> </dl>

 

 



