---
title: 伺服器 Stub
description: 伺服器 stub 會針對輸入 IDL 檔案中定義的每個作業，在伺服器上提供代理的進入點。
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- MIDL 編譯器 MIDL、MIDL 和 RPC MIDL、介面、伺服器 stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b351c53fa9e1d1716e1240ddf4febdccdadda46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021882"
---
# <a name="the-server-stub"></a><span data-ttu-id="628a9-104">伺服器 Stub</span><span class="sxs-lookup"><span data-stu-id="628a9-104">The Server Stub</span></span>

<span data-ttu-id="628a9-105">伺服器 stub 會針對輸入 IDL 檔案中定義的每個作業，在伺服器上提供代理的進入點。</span><span class="sxs-lookup"><span data-stu-id="628a9-105">The server stub provides surrogate entry points on the server for each of the operations defined in the input IDL file.</span></span>

<span data-ttu-id="628a9-106">當 RPC 執行時間程式庫叫用伺服器 stub 常式時，它會執行下列功能：</span><span class="sxs-lookup"><span data-stu-id="628a9-106">When a server stub routine is invoked by the RPC run-time library, it performs the following functions:</span></span>

-   <span data-ttu-id="628a9-107">拆收輸入引數 (從) 的傳輸格式中解壓縮引數。</span><span class="sxs-lookup"><span data-stu-id="628a9-107">Unmarshals input arguments (unpacks the arguments from their transmitted formats).</span></span>
-   <span data-ttu-id="628a9-108">呼叫伺服器上程式的實際執行。</span><span class="sxs-lookup"><span data-stu-id="628a9-108">Calls the actual implementation of the procedure on the server.</span></span>
-   <span data-ttu-id="628a9-109">封送處理輸出引數 (將引數封裝到傳送的表單) 。</span><span class="sxs-lookup"><span data-stu-id="628a9-109">Marshals output arguments (packages the arguments into the transmitted forms).</span></span>

<span data-ttu-id="628a9-110">MIDL 編譯器會將 [**/server**](-server.md)、 [**/sstub**](-sstub.md)和 [**/out**](-out.md) 切換為伺服器存根檔案。</span><span class="sxs-lookup"><span data-stu-id="628a9-110">The MIDL compiler switches [**/server**](-server.md), [**/sstub**](-sstub.md), and [**/out**](-out.md) affect the server stub file.</span></span>

 

 




