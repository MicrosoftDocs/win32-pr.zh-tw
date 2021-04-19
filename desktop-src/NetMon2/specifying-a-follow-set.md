---
description: 下列集合會指定遵循通訊協定的通訊協定。 當剖析器無法從通訊協定實例中的資料識別下一個通訊協定時，網路監視器會使用下列資料集。
ms.assetid: 9e73c724-a540-42f8-b273-4f02c39d81c4
title: 指定追蹤集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9e36268be82d2fed7c3d0c56a078e41dff1733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972247"
---
# <a name="specifying-a-follow-set"></a><span data-ttu-id="ca14b-104">指定追蹤集</span><span class="sxs-lookup"><span data-stu-id="ca14b-104">Specifying a Follow Set</span></span>

<span data-ttu-id="ca14b-105">下列集合會指定遵循通訊協定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ca14b-105">A follow set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="ca14b-106">當剖析器無法從通訊協定實例中的資料識別下一個通訊協定時，網路監視器會使用下列資料集。</span><span class="sxs-lookup"><span data-stu-id="ca14b-106">Network Monitor uses a follow set when the parser cannot identify the next protocol from the data in a protocol instance.</span></span>

<span data-ttu-id="ca14b-107">例如，NetBIOS 剖析器會指定下列設定，因為 NetBIOS 通訊協定中的資料不會識別下一個通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ca14b-107">For example, the NetBIOS parser specifies a follow set because the data in the NetBIOS protocol does not identify which protocol is next.</span></span> <span data-ttu-id="ca14b-108">如此一來，NetBIOS 剖析器必須建立一組後續可能會遵循的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ca14b-108">As a result the NetBIOS parser must create a follow set of all the protocols that may follow.</span></span>

<span data-ttu-id="ca14b-109">下列程式碼範例會識別 [*Parser.ini*](p.md) 檔中所設定的 NetBIOS 遵循。</span><span class="sxs-lookup"><span data-stu-id="ca14b-109">The following code example identifies the NetBIOS follow set in the [*Parser.ini*](p.md) file.</span></span> <span data-ttu-id="ca14b-110">下列集合包含 server message block (SMB) 和 Microsoft 遠端程序呼叫 (MSRPC) 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ca14b-110">The follow set contains server message block (SMB), and Microsoft remote procedure call (MSRPC) protocols.</span></span> <span data-ttu-id="ca14b-111">這些是可接在 NetBIOS 通訊協定實例後面的唯一通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ca14b-111">These are the only protocols that can follow an instance of the NetBIOS protocol.</span></span>

``` syntax
[NETBIOS]
   Comment    = "Network Basic Input/Output System protocol"
   FollowSet  = SMB, MSRPC
   HelpFile   =
```

<span data-ttu-id="ca14b-112">剖析器會在 [**ParserAutoInstallInfo**](parserautoinstallinfo.md) 函數的執行期間指定下列設定。</span><span class="sxs-lookup"><span data-stu-id="ca14b-112">A parser specifies a follow set during the implementation of the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) function.</span></span> <span data-ttu-id="ca14b-113">剖析器可以指定之前的通訊協定，以及接下來的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ca14b-113">A parser can specify which protocols precede, and which protocols follow.</span></span> <span data-ttu-id="ca14b-114">當剖析器指定之前的通訊協定時，網路監視器會將剖析器通訊協定新增至指定通訊協定的下列集合。</span><span class="sxs-lookup"><span data-stu-id="ca14b-114">When a parser specifies the protocols that precede, Network Monitor adds the parser protocol to the follow sets of the specified protocols.</span></span> <span data-ttu-id="ca14b-115">當剖析器指定接下來的通訊協定時，網路監視器會在 Parser.ini 檔案中建立新的區段，其中包含下列剖析器集合。</span><span class="sxs-lookup"><span data-stu-id="ca14b-115">When a parser specifies the protocols that follow, Network Monitor creates a new section in the Parser.ini file that includes the follow set of the parser.</span></span>

 

 



