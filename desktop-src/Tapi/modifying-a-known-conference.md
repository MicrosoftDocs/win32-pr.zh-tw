---
description: 下列程式碼片段說明如何修改會議時間範圍。 預設的時間範圍是三十分鐘。 在此片段中，時間範圍設定為一年。
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: 修改已知會議
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bd58003b276bd3cdd54da2e7ed0df4f154311e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191111"
---
# <a name="modifying-a-known-conference"></a><span data-ttu-id="b20b5-105">修改已知會議</span><span class="sxs-lookup"><span data-stu-id="b20b5-105">Modifying a Known Conference</span></span>

<span data-ttu-id="b20b5-106">\[在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="b20b5-106">\[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b20b5-107">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="b20b5-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b20b5-108">下列程式碼片段說明會議時間範圍的修改。</span><span class="sxs-lookup"><span data-stu-id="b20b5-108">The following code fragment illustrates modification of a conference's time span.</span></span> <span data-ttu-id="b20b5-109">預設的時間範圍是三十分鐘。</span><span class="sxs-lookup"><span data-stu-id="b20b5-109">The default time span is thirty minutes.</span></span> <span data-ttu-id="b20b5-110">在此片段中，時間範圍設定為一年。</span><span class="sxs-lookup"><span data-stu-id="b20b5-110">In this fragment, the time span is set to one year.</span></span>

<span data-ttu-id="b20b5-111">此片段假設已執行 [連接到 ILS 伺服器](connecting-to-an-ils-server.md) ，並已執行 [會議目錄列舉](enumerating-conference-directories.md) 來取得將修改的目錄專案。</span><span class="sxs-lookup"><span data-stu-id="b20b5-111">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed and that a [conference directory enumeration](enumerating-conference-directories.md) has been performed to obtain the directory entry that will be modified.</span></span>

<span data-ttu-id="b20b5-112">此片段也假設這不是多播會議。</span><span class="sxs-lookup"><span data-stu-id="b20b5-112">This fragment also assumes this is not a multicast conference.</span></span> <span data-ttu-id="b20b5-113">變更多播會議的時間需要多播位址佈建服務器的通知。</span><span class="sxs-lookup"><span data-stu-id="b20b5-113">Changing the times on a multicast conference requires notification of the multicast address allocation server.</span></span> <span data-ttu-id="b20b5-114">如需使用多播定址的範例，請參閱取得 [多播位址](acquiring-a-multicast-address.md) 。</span><span class="sxs-lookup"><span data-stu-id="b20b5-114">See [Acquiring a Multicast Address](acquiring-a-multicast-address.md) for an example of working with multicast addressing.</span></span>


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a><span data-ttu-id="b20b5-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="b20b5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b20b5-116">**ITDirectoryObjectConference**</span><span class="sxs-lookup"><span data-stu-id="b20b5-116">**ITDirectoryObjectConference**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



