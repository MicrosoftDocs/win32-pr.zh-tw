---
title: IAgentNotifySink 命令
description: IAgentNotifySink 命令
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690d2914db9d284cd4ba4b826905d3169b83f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933175"
---
# <a name="iagentnotifysinkcommand"></a><span data-ttu-id="00a10-103">IAgentNotifySink：： Command</span><span class="sxs-lookup"><span data-stu-id="00a10-103">IAgentNotifySink::Command</span></span>

<span data-ttu-id="00a10-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="00a10-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

<span data-ttu-id="00a10-105">通知用戶端應用程式已選取使用者的 [**命令**](/windows/desktop/lwef/the-command-object) 。</span><span class="sxs-lookup"><span data-stu-id="00a10-105">Notifies a client application that a [**Command**](/windows/desktop/lwef/the-command-object) was selected by the user.</span></span>

-   <span data-ttu-id="00a10-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="00a10-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="00a10-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span><span class="sxs-lookup"><span data-stu-id="00a10-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="00a10-108">最符合命令替代選項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="00a10-108">Identifier of the best match command alternative.</span></span>

</dd> <dt>

<span data-ttu-id="00a10-109"><span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*</span><span class="sxs-lookup"><span data-stu-id="00a10-109"><span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*</span></span>
</dt> <dd>

<span data-ttu-id="00a10-110">[**IAgentUserInput**](iagentuserinput.md)物件的 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面位址。</span><span class="sxs-lookup"><span data-stu-id="00a10-110">Address of the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface for the [**IAgentUserInput**](iagentuserinput.md) object.</span></span>

</dd> </dl>

<span data-ttu-id="00a10-111">使用 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 取出 [**IAgentUserInput**](iagentuserinput.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="00a10-111">Use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to retrieve the [**IAgentUserInput**](iagentuserinput.md) interface.</span></span>

<span data-ttu-id="00a10-112">當使用者以語音選擇命令或從字元的快顯功能表中選取命令時，伺服器會通知輸入-主動用戶端。</span><span class="sxs-lookup"><span data-stu-id="00a10-112">The server notifies the input-active client when the user chooses a command by voice or by selecting a command from the character's pop-up menu.</span></span> <span data-ttu-id="00a10-113">即使使用者選取其中一個伺服器的命令，也會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="00a10-113">The event occurs even when the user selects one of the server's commands.</span></span> <span data-ttu-id="00a10-114">在此情況下，伺服器會傳回 null 命令識別碼、信賴分數，以及該專案的語音引擎所傳回的語音文字。</span><span class="sxs-lookup"><span data-stu-id="00a10-114">In this case the server returns a null command ID, the confidence score, and the voice text returned by the speech engine for that entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="00a10-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00a10-115">See Also</span></span>

[<span data-ttu-id="00a10-116">**IAgentUserInput**</span><span class="sxs-lookup"><span data-stu-id="00a10-116">**IAgentUserInput**</span></span>](iagentuserinput.md)


 

 