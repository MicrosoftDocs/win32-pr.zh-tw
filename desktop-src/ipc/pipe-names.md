---
description: 每個具名管道都有唯一的名稱，可在命名物件的系統清單中區分它與其他具名管道。 當管道伺服器呼叫 CreateNamedPipe 函式來建立具名管道的一或多個實例時，會指定該管道的名稱。
ms.assetid: 8f7e717a-648b-421e-ab79-a4abbae670be
title: 管道名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e470a09fa4cfe1b2f259ca3fd5b53f79045787fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000176"
---
# <a name="pipe-names"></a><span data-ttu-id="6acba-104">管道名稱</span><span class="sxs-lookup"><span data-stu-id="6acba-104">Pipe Names</span></span>

<span data-ttu-id="6acba-105">每個具名管道都有唯一的名稱，可區別系統的命名物件清單中的其他具名管道。</span><span class="sxs-lookup"><span data-stu-id="6acba-105">Each named pipe has a unique name that distinguishes it from other named pipes in the system's list of named objects.</span></span> <span data-ttu-id="6acba-106">當管道伺服器呼叫 [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) 函式來建立具名管道的一或多個實例時，會指定該管道的名稱。</span><span class="sxs-lookup"><span data-stu-id="6acba-106">A pipe server specifies a name for the pipe when it calls the [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) function to create one or more instances of a named pipe.</span></span> <span data-ttu-id="6acba-107">管道用戶端會在呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 或 [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) 函式以連接到具名管道的實例時，指定管道名稱。</span><span class="sxs-lookup"><span data-stu-id="6acba-107">Pipe clients specify the pipe name when they call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function to connect to an instance of the named pipe.</span></span>

<span data-ttu-id="6acba-108">在 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)、 [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)或 [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) 函數中指定管道的名稱時，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="6acba-108">Use the following form when specifying the name of a pipe in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea), or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function:</span></span>

<span data-ttu-id="6acba-109">\\\\*ServerName* \\管道 \\ *PipeName*</span><span class="sxs-lookup"><span data-stu-id="6acba-109">\\\\*ServerName*\\pipe\\*PipeName*</span></span>

<span data-ttu-id="6acba-110">其中 *ServerName* 是遠端電腦的名稱或句號，以指定本機電腦。</span><span class="sxs-lookup"><span data-stu-id="6acba-110">where *ServerName* is either the name of a remote computer or a period, to specify the local computer.</span></span> <span data-ttu-id="6acba-111">*PipeName* 指定的管道名稱字串可以包含反斜線以外的任何字元，包括數位和特殊字元。</span><span class="sxs-lookup"><span data-stu-id="6acba-111">The pipe name string specified by *PipeName* can include any character other than a backslash, including numbers and special characters.</span></span> <span data-ttu-id="6acba-112">整個管道名稱字串的長度最多可達256個字元。</span><span class="sxs-lookup"><span data-stu-id="6acba-112">The entire pipe name string can be up to 256 characters long.</span></span> <span data-ttu-id="6acba-113">管道名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6acba-113">Pipe names are not case-sensitive.</span></span>

<span data-ttu-id="6acba-114">管道伺服器無法在另一部電腦上建立管道，因此 [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) 必須使用句點做為伺服器名稱，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="6acba-114">The pipe server cannot create a pipe on another computer, so [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) must use a period for the server name, as shown in the following example.</span></span>

<span data-ttu-id="6acba-115">\\\\.\\管道 \\ *PipeName*</span><span class="sxs-lookup"><span data-stu-id="6acba-115">\\\\.\\pipe\\*PipeName*</span></span>

<span data-ttu-id="6acba-116">管道伺服器可以提供管道用戶端的管道名稱，讓它們可以連接到管道。</span><span class="sxs-lookup"><span data-stu-id="6acba-116">A pipe server can provide the pipe name to its pipe clients, so they can connect to the pipe.</span></span> <span data-ttu-id="6acba-117">管道用戶端會從某個持續性來源（例如登錄專案、檔案或其他應用程式）探索管道名稱。</span><span class="sxs-lookup"><span data-stu-id="6acba-117">The pipe client discovers the pipe name from some persistent source, such as a registry entry, a file, or another application.</span></span> <span data-ttu-id="6acba-118">否則，用戶端必須知道編譯時期的管道名稱。</span><span class="sxs-lookup"><span data-stu-id="6acba-118">Otherwise, the clients must know the pipe name at compile time.</span></span>

 

 
