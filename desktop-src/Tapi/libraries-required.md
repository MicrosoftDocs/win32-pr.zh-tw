---
description: 以下是編譯各種 TAPI 3 應用程式所需的 .lib 檔案清單，1/22/01。
ms.assetid: f1765829-9a5d-4e85-b898-6679279aa6d9
title: 需要的程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0948599041c466a337d2d6828750a9996dc8d813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974085"
---
# <a name="libraries-required"></a><span data-ttu-id="644e8-103">需要的程式庫</span><span class="sxs-lookup"><span data-stu-id="644e8-103">Libraries Required</span></span>

<span data-ttu-id="644e8-104">編譯各種 TAPI 3 應用程式所需的 .lib 檔案清單，1/22/01：</span><span class="sxs-lookup"><span data-stu-id="644e8-104">A list of .lib files required to compile various TAPI 3 applications, as of 1/22/01:</span></span>

-   <span data-ttu-id="644e8-105">Advapi32.dll .lib</span><span class="sxs-lookup"><span data-stu-id="644e8-105">Advapi32.lib</span></span>
-   <span data-ttu-id="644e8-106">Amstrmid .lib (ActiveMovie Guid) </span><span class="sxs-lookup"><span data-stu-id="644e8-106">Amstrmid.lib (ActiveMovie GUIDs)</span></span>
-   <span data-ttu-id="644e8-107">Kernel32.lib</span><span class="sxs-lookup"><span data-stu-id="644e8-107">Kernel32.lib</span></span>
-   <span data-ttu-id="644e8-108">Mdhcpid .lib (多播 Guid) </span><span class="sxs-lookup"><span data-stu-id="644e8-108">Mdhcpid.lib (multicast GUIDs)</span></span>
-   <span data-ttu-id="644e8-109">Ole32.lib .lib (COM) </span><span class="sxs-lookup"><span data-stu-id="644e8-109">Ole32.lib (COM)</span></span>
-   <span data-ttu-id="644e8-110">Oleaut32.lib .lib (COM Automation) </span><span class="sxs-lookup"><span data-stu-id="644e8-110">Oleaut32.lib (COM Automation)</span></span>
-   <span data-ttu-id="644e8-111">Rendid .lib (會合 Guid) </span><span class="sxs-lookup"><span data-stu-id="644e8-111">Rendid.lib (Rendezvous GUIDs)</span></span>
-   <span data-ttu-id="644e8-112">Rpcndr .lib</span><span class="sxs-lookup"><span data-stu-id="644e8-112">Rpcndr.lib</span></span>
-   <span data-ttu-id="644e8-113">Rpcns4 .lib</span><span class="sxs-lookup"><span data-stu-id="644e8-113">Rpcns4.lib</span></span>
-   <span data-ttu-id="644e8-114">Rpcrt4 .lib</span><span class="sxs-lookup"><span data-stu-id="644e8-114">Rpcrt4.lib</span></span>
-   <span data-ttu-id="644e8-115">Sdpblbid .lib (會話描述項通訊協定 (SDP) Guid) </span><span class="sxs-lookup"><span data-stu-id="644e8-115">Sdpblbid.lib (Session Descriptor Protocol (SDP) GUIDs)</span></span>
-   <span data-ttu-id="644e8-116">Strmiids .lib</span><span class="sxs-lookup"><span data-stu-id="644e8-116">Strmiids.lib</span></span>
-   <span data-ttu-id="644e8-117">User32</span><span class="sxs-lookup"><span data-stu-id="644e8-117">User32.lib</span></span>
-   <span data-ttu-id="644e8-118">Uuid</span><span class="sxs-lookup"><span data-stu-id="644e8-118">Uuid.lib</span></span>
-   <span data-ttu-id="644e8-119">Wldap32.dll .lib</span><span class="sxs-lookup"><span data-stu-id="644e8-119">Wldap32.lib</span></span>
-   <span data-ttu-id="644e8-120">Ws2 \_ 32 .lib</span><span class="sxs-lookup"><span data-stu-id="644e8-120">Ws2\_32.lib</span></span>

<span data-ttu-id="644e8-121">如果您使用 Microsoft Visual Studio，可能需要更新您的版本。</span><span class="sxs-lookup"><span data-stu-id="644e8-121">If you are using Microsoft Visual Studio, you may need to update your version.</span></span> <span data-ttu-id="644e8-122">尤其是 Link.exe 必須執行3/19/98 或更新版本的日期。</span><span class="sxs-lookup"><span data-stu-id="644e8-122">In particular, Link.exe must carry a date of 3/19/98 or later.</span></span>

<span data-ttu-id="644e8-123">編譯器定義必須包含 \_ \_ 至少設定為0x500 和 win32 DCOM 的 win32 WINNT \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="644e8-123">Compiler defines must include \_WIN32\_WINNT set to at least 0x500 and \_WIN32\_DCOM.</span></span>

 

 



