---
description: 描述在 Windows 下進行網路 i/o 作業的進程。
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: 網路 i/o 操作的描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371b72389554f1c3fa2ec43180b1a6e4c76dc012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319296"
---
# <a name="description-of-a-network-io-operation"></a><span data-ttu-id="b326d-103">網路 i/o 操作的描述</span><span class="sxs-lookup"><span data-stu-id="b326d-103">Description of a Network I/O Operation</span></span>

<span data-ttu-id="b326d-104">下圖說明 Windows 上的網路 i/o 作業的處理常式。</span><span class="sxs-lookup"><span data-stu-id="b326d-104">The following figure illustrates the process of a network I/O operation under Windows.</span></span>

![windows 下的網路 i/o 操作](images/fig4.png)

<span data-ttu-id="b326d-106">當應用程式呼叫檔案 i/o 函數來存取遠端電腦上的檔案時，會發生下列事件：</span><span class="sxs-lookup"><span data-stu-id="b326d-106">When an application calls a file I/O function to access a file on a remote computer, the following events occur:</span></span>

-   <span data-ttu-id="b326d-107">本機電腦上的 [網路](network-redirectors.md)重新導向器（也稱為重新導向程式）會攔截 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="b326d-107">The I/O request is intercepted by a [network redirector](network-redirectors.md), also referred to simply as a redirector, on the local computer.</span></span> <span data-ttu-id="b326d-108">在上圖中，這是由應用程式和用戶端重新導向器之間的實心箭號所描述。</span><span class="sxs-lookup"><span data-stu-id="b326d-108">This is depicted in the preceding figure by the solid arrow between the application and the client redirector.</span></span>
-   <span data-ttu-id="b326d-109">重新導向器會建立包含所有要求資訊的資料封包，並將其傳送至檔案所在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b326d-109">The redirector constructs a data packet containing all of the information about the request, and sends it to the server where the file is located.</span></span> <span data-ttu-id="b326d-110">在上圖中，這是由用戶端重新導向器和伺服器重新導向器之間的實心箭號所描述。</span><span class="sxs-lookup"><span data-stu-id="b326d-110">This is depicted in the preceding figure by the solid arrow between the client redirector and the server redirector.</span></span>
-   <span data-ttu-id="b326d-111">伺服器上的重新導向器會接收來自用戶端的封包、驗證 i/o 要求所需之檔案的存取權，而且如果經過驗證，則會代表用戶端執行要求。</span><span class="sxs-lookup"><span data-stu-id="b326d-111">The redirector on the server receives the packet from the client, authenticates the access to the file required by the I/O request, and, if authenticated, executes the request on behalf of the client.</span></span> <span data-ttu-id="b326d-112">如果沒有，則會將錯誤碼傳回至用戶端上的重新導向器。</span><span class="sxs-lookup"><span data-stu-id="b326d-112">If not, it returns an error code to the redirector on the client.</span></span> <span data-ttu-id="b326d-113">在上圖中，是由伺服器重新導向程式和檔案之間的彎曲實心箭號所描述。</span><span class="sxs-lookup"><span data-stu-id="b326d-113">This is depicted in the preceding figure by the curved solid arrow between the server redirector and the file.</span></span>
-   <span data-ttu-id="b326d-114">當要求執行時，伺服器上的重新導向器會將 i/o 要求所產生的任何資料，連同成功通知傳送至用戶端上的重新導向器。</span><span class="sxs-lookup"><span data-stu-id="b326d-114">When the request has been executed, the redirector on the server sends any data resulting from the I/O request to the redirector on the client along with a success notification.</span></span> <span data-ttu-id="b326d-115">在上圖中，這是由伺服器和用戶端重新導向器之間的點箭號所描述。</span><span class="sxs-lookup"><span data-stu-id="b326d-115">This is depicted in the preceding figure by the dotted arrow between the server and the client redirector.</span></span>
-   <span data-ttu-id="b326d-116">用戶端上的重新導向器會接收來自伺服器的封包，並將封包中的資料連同成功通知傳遞給應用程式。</span><span class="sxs-lookup"><span data-stu-id="b326d-116">The redirector on the client receives the packet from the server and passes the data in the packet to the application along with a success notification.</span></span> <span data-ttu-id="b326d-117">在上圖中，這是由用戶端重新導向器和應用程式之間的虛線箭號所描述。</span><span class="sxs-lookup"><span data-stu-id="b326d-117">This is depicted in the preceding figure by the dotted arrow between the client redirector and the application.</span></span>

<span data-ttu-id="b326d-118">Windows 可以使用各種網路通訊協定來執行網路 i/o 操作，包括 [MICROSOFT SMB 通訊協定和 CIFS 通訊協定總覽](microsoft-smb-protocol-and-cifs-protocol-overview.md) 和 NFS。</span><span class="sxs-lookup"><span data-stu-id="b326d-118">Windows can use a variety of networking protocols to perform a network I/O operation, including [Microsoft SMB Protocol and CIFS Protocol Overview](microsoft-smb-protocol-and-cifs-protocol-overview.md) and NFS.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b326d-119">本節內容</span><span class="sxs-lookup"><span data-stu-id="b326d-119">In this section</span></span>



| <span data-ttu-id="b326d-120">主題</span><span class="sxs-lookup"><span data-stu-id="b326d-120">Topic</span></span>                                                                                       | <span data-ttu-id="b326d-121">描述</span><span class="sxs-lookup"><span data-stu-id="b326d-121">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="b326d-122">本機和網路 i/o 的差異</span><span class="sxs-lookup"><span data-stu-id="b326d-122">Differences in Local and Network I/O</span></span>](differences-in-local-and-network-i-o.md)<br/> | <span data-ttu-id="b326d-123">Windows 上的本機 i/o 和網路 i/o 之間的差異。</span><span class="sxs-lookup"><span data-stu-id="b326d-123">Differences between local I/O and network I/O on Windows.</span></span><br/> |
| [<span data-ttu-id="b326d-124">網路重定向器</span><span class="sxs-lookup"><span data-stu-id="b326d-124">Network Redirectors</span></span>](network-redirectors.md)<br/>                                   | <span data-ttu-id="b326d-125">描述網路重新導向程式的功能。</span><span class="sxs-lookup"><span data-stu-id="b326d-125">Describes the functionality of a network redirector.</span></span><br/>      |



 

 

 




