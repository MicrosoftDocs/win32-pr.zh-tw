---
description: 命名 mailslots，並將訊息放入 mailslots。
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: 郵筒名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03718a7e603fe891e00d82c2b0b06fab63f8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689520"
---
# <a name="mailslot-names"></a><span data-ttu-id="9be5b-103">郵筒名稱</span><span class="sxs-lookup"><span data-stu-id="9be5b-103">Mailslot Names</span></span>

<span data-ttu-id="9be5b-104">當進程建立信箱時，mailslot 名稱必須具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="9be5b-104">When a process creates a mailslot, the mailslot name must have the following form.</span></span>

<span data-ttu-id="9be5b-105">\\\\.\\郵筒 \\ \[ *路徑* \\ \] *名稱*</span><span class="sxs-lookup"><span data-stu-id="9be5b-105">\\\\.\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="9be5b-106">郵筒名稱需要下列元素：兩個反斜線來開始名稱、句號、句點之後的反斜線、"郵筒" 和 "尾端反斜線" 一字。</span><span class="sxs-lookup"><span data-stu-id="9be5b-106">A mailslot name requires the following elements: two backslashes to begin the name, a period, a backslash following the period, the word "mailslot", and a trailing backslash.</span></span> <span data-ttu-id="9be5b-107">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="9be5b-107">Names are not case sensitive.</span></span> <span data-ttu-id="9be5b-108">郵筒名稱前面可以有一個路徑，其中包含一個或多個目錄的名稱（以反斜線分隔）。</span><span class="sxs-lookup"><span data-stu-id="9be5b-108">A mailslot name can be preceded by a path consisting of the names of one or more directories, separated by backslashes.</span></span> <span data-ttu-id="9be5b-109">例如，如果使用者預期來自 Bob、Pete 和 Sue 之稅金的訊息，使用者的郵筒應用程式可能會允許使用者為每個寄件者建立個別的 mailslots，如下所示：</span><span class="sxs-lookup"><span data-stu-id="9be5b-109">For example, if a user expects messages on the subject of taxes from Bob, Pete, and Sue, the user's mailslot application might allow the user to create individual mailslots for each sender, as shown here:</span></span><dl> <span data-ttu-id="9be5b-110">\\\\.\\郵筒 \\ \\ bobs-machine \_ 批註</span><span class="sxs-lookup"><span data-stu-id="9be5b-110">\\\\.\\mailslot\\taxes\\bobs\_comments</span></span>  
<span data-ttu-id="9be5b-111">\\\\.\\郵筒 \\ \\ petes \_ 批註</span><span class="sxs-lookup"><span data-stu-id="9be5b-111">\\\\.\\mailslot\\taxes\\petes\_comments</span></span>  
<span data-ttu-id="9be5b-112">\\\\.\\郵筒 \\ \\ 使用 \_ 批註</span><span class="sxs-lookup"><span data-stu-id="9be5b-112">\\\\.\\mailslot\\taxes\\sues\_comments</span></span>  
</dl>

<span data-ttu-id="9be5b-113">為了將訊息放入郵筒，進程會依名稱開啟信箱。</span><span class="sxs-lookup"><span data-stu-id="9be5b-113">To put a message into a mailslot, a process opens a mailslot by name.</span></span> <span data-ttu-id="9be5b-114">若要寫入本機電腦上的信箱，處理常式可以使用具有相同表單的郵筒名稱來建立郵筒。</span><span class="sxs-lookup"><span data-stu-id="9be5b-114">To write to a mailslot on the local computer, a process can use a mailslot name that has the same form used for creating a mailslot.</span></span> <span data-ttu-id="9be5b-115">不過，這種情況相當罕見。</span><span class="sxs-lookup"><span data-stu-id="9be5b-115">This situation, however, is relatively uncommon.</span></span> <span data-ttu-id="9be5b-116">更頻繁地，您可以使用下列格式來寫入特定遠端電腦上的信箱：</span><span class="sxs-lookup"><span data-stu-id="9be5b-116">More frequently, you would use the following form to write to a mailslot on a specific remote computer:</span></span>

<span data-ttu-id="9be5b-117">\\\\*ComputerName* \\郵筒 \\ \[ *路徑* \\ \] *名稱*</span><span class="sxs-lookup"><span data-stu-id="9be5b-117">\\\\*ComputerName*\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="9be5b-118">若要使用指定的名稱將訊息放入指定網域中的每個信箱，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="9be5b-118">To put a message into every mailslot in the specified domain with a given name, use the following form:</span></span>

<span data-ttu-id="9be5b-119">\\\\*DomainName* \\郵筒 \\ \[ *路徑* \\ \] *名稱*</span><span class="sxs-lookup"><span data-stu-id="9be5b-119">\\\\*DomainName*\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="9be5b-120">若要將訊息放入系統的主要網域中具有指定名稱的每個信箱，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="9be5b-120">To put a message into every mailslot with a given name in the system's primary domain, use the following form:</span></span>

<span data-ttu-id="9be5b-121">\\\\\*\\郵筒 \\ \[ *路徑* \\ \] *名稱*</span><span class="sxs-lookup"><span data-stu-id="9be5b-121">\\\\\*\\mailslot\\\[*path*\\\]*name*</span></span>

 

 



