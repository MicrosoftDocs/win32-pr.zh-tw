---
description: 下列程式碼片段說明如何在 ILS 伺服器中發行使用者物件。 在使用者物件發佈之後，遠端合作物件就可以使用 user 物件來呼叫指定的使用者。
ms.assetid: 8b68886c-0df5-4005-bcd5-1a18336f5192
title: 將使用者物件加入至 ILS 伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b15dcdbca47187cf4155dfbf7535d06718c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690068"
---
# <a name="adding-a-user-object-to-an-ils-server"></a><span data-ttu-id="ccd37-104">將使用者物件加入至 ILS 伺服器</span><span class="sxs-lookup"><span data-stu-id="ccd37-104">Adding a User Object to an ILS Server</span></span>

<span data-ttu-id="ccd37-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="ccd37-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ccd37-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="ccd37-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ccd37-107">下列程式碼片段說明如何在 ILS 伺服器中發行使用者物件。</span><span class="sxs-lookup"><span data-stu-id="ccd37-107">The following code fragment illustrates publishing a user object in an ILS server.</span></span> <span data-ttu-id="ccd37-108">在使用者物件發佈之後，遠端合作物件就可以使用 user 物件來呼叫指定的使用者。</span><span class="sxs-lookup"><span data-stu-id="ccd37-108">After a user object is published, remote parties can use the user object to make calls to the specified user.</span></span>

<span data-ttu-id="ccd37-109">此片段假設已經執行 [連接到 ILS 伺服器](connecting-to-an-ils-server.md) 。</span><span class="sxs-lookup"><span data-stu-id="ccd37-109">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span>


```C++
hr = pDirectory->AddDirectoryObject(pDirectoryObject);
```



## <a name="related-topics"></a><span data-ttu-id="ccd37-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="ccd37-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccd37-111">**ITDirectory**</span><span class="sxs-lookup"><span data-stu-id="ccd37-111">**ITDirectory**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[<span data-ttu-id="ccd37-112">**ITDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="ccd37-112">**ITDirectoryObject**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[<span data-ttu-id="ccd37-113">**ITDirectoryObjectUser**</span><span class="sxs-lookup"><span data-stu-id="ccd37-113">**ITDirectoryObjectUser**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)
</dt> </dl>

 

 



