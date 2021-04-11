---
title: IAgentCharacter 隱藏
description: IAgentCharacter 隱藏
ms.assetid: a8128fe8-9a3b-41a3-bfe3-82ace1baff6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd0ef91eb4d2738f19fb594ac1ab186efaec6e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023399"
---
# <a name="iagentcharacterhide"></a><span data-ttu-id="5f587-103">IAgentCharacter：： Hide</span><span class="sxs-lookup"><span data-stu-id="5f587-103">IAgentCharacter::Hide</span></span>

<span data-ttu-id="5f587-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="5f587-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Hide(
   long bFast,      // play Hiding state animation flag
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="5f587-105">隱藏字元。</span><span class="sxs-lookup"><span data-stu-id="5f587-105">Hides the character.</span></span>

-   <span data-ttu-id="5f587-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="5f587-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="5f587-107">當函式傳回時， *pdwReqID* 會包含要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f587-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="5f587-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span><span class="sxs-lookup"><span data-stu-id="5f587-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span></span>
</dt> <dd>

<span data-ttu-id="5f587-109">**隱藏** 狀態動畫旗標。</span><span class="sxs-lookup"><span data-stu-id="5f587-109">**Hiding** state animation flag.</span></span> <span data-ttu-id="5f587-110">如果此參數為 **True** **，隱藏的動畫不** 會在隱藏字元框架之前播放;如果 **為 False**，則會播放動畫。</span><span class="sxs-lookup"><span data-stu-id="5f587-110">If this parameter is **True**, the **Hiding** animation does not play before the character frame is hidden; if **False**, the animation plays.</span></span>

</dd> <dt>

<span data-ttu-id="5f587-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="5f587-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="5f587-112">接收 **隱藏** 要求識別碼之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="5f587-112">Address of a variable that receives the **Hide** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="5f587-113">伺服器會將與字元佇列中的 **Hide** 方法相關聯的動畫排入佇列。</span><span class="sxs-lookup"><span data-stu-id="5f587-113">The server queues the animation associated with the **Hide** method in the character's queue.</span></span> <span data-ttu-id="5f587-114">這可讓您使用它來隱藏其他動畫序列之後的字元。</span><span class="sxs-lookup"><span data-stu-id="5f587-114">This allows you to use it to hide the character after a sequence of other animations.</span></span> <span data-ttu-id="5f587-115">您可以在呼叫 **Hide** 方法之前，使用 [**Stop**](iagentcharacter--stop.md)方法立即播放動作。</span><span class="sxs-lookup"><span data-stu-id="5f587-115">You can play the action immediately by using the [**Stop**](iagentcharacter--stop.md) method before calling the **Hide** method.</span></span>

<span data-ttu-id="5f587-116">使用 HTTP 通訊協定來存取字元和動畫資料時，請在呼叫這個方法之前，先使用 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 方法來確保 **隱藏** 狀態動畫的可用性。</span><span class="sxs-lookup"><span data-stu-id="5f587-116">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Hiding** state animation before calling this method.</span></span>

<span data-ttu-id="5f587-117">隱藏字元也可能導致觸發另一個可見字元的 [**IAgentNotifySink：： ActivateInputState**](iagentnotifysink--activateinputstate.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="5f587-117">Hiding a character can also result in triggering the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md) event of another visible character.</span></span>

<span data-ttu-id="5f587-118">隱藏的字元無法存取音訊通道。</span><span class="sxs-lookup"><span data-stu-id="5f587-118">Hidden characters cannot access the audio channel.</span></span> <span data-ttu-id="5f587-119">如果您產生動畫要求且隱藏字元，伺服器將會在 [**RequestComplete**](iagentnotifysink--requestcomplete.md) 事件中傳回失敗狀態。</span><span class="sxs-lookup"><span data-stu-id="5f587-119">The server will pass back a failure status in the [**RequestComplete**](iagentnotifysink--requestcomplete.md) event if you generate an animation request and the character is hidden.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f587-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f587-120">See Also</span></span>

[<span data-ttu-id="5f587-121">**IAgentCharacter：： Show**</span><span class="sxs-lookup"><span data-stu-id="5f587-121">**IAgentCharacter::Show**</span></span>](iagentcharacter--show.md)


 

 