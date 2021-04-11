---
title: IAgentCharacter Show
description: IAgentCharacter Show
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997a9879d564644085bd92e4515460c3dde33208
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023479"
---
# <a name="iagentcharactershow"></a><span data-ttu-id="ae09b-103">IAgentCharacter：： Show</span><span class="sxs-lookup"><span data-stu-id="ae09b-103">IAgentCharacter::Show</span></span>

<span data-ttu-id="ae09b-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="ae09b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="ae09b-105">顯示字元。</span><span class="sxs-lookup"><span data-stu-id="ae09b-105">Displays a character.</span></span>

-   <span data-ttu-id="ae09b-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="ae09b-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="ae09b-107">當函式傳回時， *pdwReqID* 會包含要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae09b-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="ae09b-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span><span class="sxs-lookup"><span data-stu-id="ae09b-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span></span>
</dt> <dd>

<span data-ttu-id="ae09b-109">顯示狀態動畫旗標。</span><span class="sxs-lookup"><span data-stu-id="ae09b-109">Showing state animation flag.</span></span> <span data-ttu-id="ae09b-110">如果此參數為 **True**， **顯示** 狀態動畫會在讓字元變成可見之後播放;如果 **為 False**，則不播放動畫。</span><span class="sxs-lookup"><span data-stu-id="ae09b-110">If this parameter is **True**, the **Showing** state animation plays after making the character visible; if **False**, the animation does not play.</span></span>

</dd> <dt>

<span data-ttu-id="ae09b-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="ae09b-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="ae09b-112">接收 [**顯示**](/windows/desktop/lwef/iagentcharacter--show) 要求識別碼之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="ae09b-112">Address of a variable that receives the [**Show**](/windows/desktop/lwef/iagentcharacter--show) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="ae09b-113">避免將 *bFast* 參數設定為 **True** ，而不事先播放動畫，否則可能會顯示字元框架，但沒有可顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="ae09b-113">Avoid setting the *bFast* parameter to **True** without playing an animation beforehand, otherwise, the character frame may be displayed, but have no image to display.</span></span> <span data-ttu-id="ae09b-114">尤其要注意的是，如果您在字元未顯示時呼叫 [**MoveTo**](iagentcharacter--moveto.md) ，則不會播放任何動畫。</span><span class="sxs-lookup"><span data-stu-id="ae09b-114">In particular, note that if you call [**MoveTo**](iagentcharacter--moveto.md) when the character is not visible, it does not play any animation.</span></span> <span data-ttu-id="ae09b-115">因此，如果您呼叫 *bFast* 設為 **True** 的 **Show** 方法，則不會顯示任何影像。</span><span class="sxs-lookup"><span data-stu-id="ae09b-115">Therefore, if you call the **Show** method with *bFast* set to **True**, no image will be displayed.</span></span> <span data-ttu-id="ae09b-116">同樣地，如果您呼叫 [[**隱藏**](/windows/desktop/lwef/iagentcharacter--hide)]，並將 [ *bFast* ] 設定為 [ **True**]，就不會 **顯示** 影像。</span><span class="sxs-lookup"><span data-stu-id="ae09b-116">Similarly, if you call [**Hide**](/windows/desktop/lwef/iagentcharacter--hide), then **Show** with *bFast* set to **True**, there will be no visible image.</span></span>

<span data-ttu-id="ae09b-117">使用 HTTP 通訊協定來存取字元和動畫資料時，請使用 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 方法，以確保在呼叫這個方法之前， **顯示** 狀態動畫的可用性。</span><span class="sxs-lookup"><span data-stu-id="ae09b-117">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Showing** state animation before calling this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae09b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae09b-118">See Also</span></span>

[<span data-ttu-id="ae09b-119">**IAgentCharacter：： Hide**</span><span class="sxs-lookup"><span data-stu-id="ae09b-119">**IAgentCharacter::Hide**</span></span>](iagentcharacter--hide.md)


 

 