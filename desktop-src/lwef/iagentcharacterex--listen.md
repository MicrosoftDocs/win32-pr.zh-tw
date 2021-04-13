---
title: IAgentCharacterEx 接聽
description: IAgentCharacterEx 接聽
ms.assetid: 8d4cdb6c-04e1-498c-867f-fddbe6e2791a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c479936a8d2dc43e2f2da5a680a51705af2885
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301227"
---
# <a name="iagentcharacterexlisten"></a><span data-ttu-id="6a9ec-103">IAgentCharacterEx：：接聽</span><span class="sxs-lookup"><span data-stu-id="6a9ec-103">IAgentCharacterEx::Listen</span></span>

<span data-ttu-id="6a9ec-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="6a9ec-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Listen(
   long bListen  // listening mode flag
);
```

<span data-ttu-id="6a9ec-105">開啟或關閉語音辨識輸入 () 的接聽模式。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-105">Turns Listening mode (speech recognition input) on or off.</span></span>

-   <span data-ttu-id="6a9ec-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="6a9ec-107"><span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*</span><span class="sxs-lookup"><span data-stu-id="6a9ec-107"><span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*</span></span>
</dt> <dd>

<span data-ttu-id="6a9ec-108">接聽模式旗標。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-108">Listening mode flag.</span></span> <span data-ttu-id="6a9ec-109">如果此參數為 **True**，則會開啟接聽模式;如果 **為 False**，則表示接聽模式為關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-109">If this parameter is **True**, the Listening mode is turned on; if **False**, Listening mode is turned off.</span></span>

</dd> </dl>

<span data-ttu-id="6a9ec-110">將此方法設定為 **True** ，可讓接聽模式 (在一段固定時間內開啟語音辨識) 。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-110">Setting this method to **True** enables the Listening mode (turns on speech recognition) for a fixed period of time.</span></span> <span data-ttu-id="6a9ec-111">當您無法設定超時值時，您可以在超時時間到期之前關閉接聽模式。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-111">While you cannot set the value of the time-out, you can turn off Listening mode before the time-out expires.</span></span> <span data-ttu-id="6a9ec-112">此外，如果已開啟接聽模式，因為您 (或其他用戶端) 成功將方法設為 **True** ，在超時時間到期之前，方法會成功，並重設超時時間。不過，如果已開啟接聽模式，因為使用者按下接聽鍵，方法會成功，但是會忽略超時，而且接聽模式會根據使用者與接聽鍵的互動而結束。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-112">In addition, if the Listening mode is already on because you (or another client) successfully set the method to **True** before the time-out expires, the method succeeds and resets the time-out. However, if Listening mode is already on because the user is pressing the Listening key, the method succeeds, but the time-out is ignored and the Listening mode ends based on the user's interaction with the Listening key.</span></span>

<span data-ttu-id="6a9ec-113">只有當輸入-主動用戶端呼叫這個方法時，此方法才會成功。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-113">This method will succeed only when called by the input-active client.</span></span> <span data-ttu-id="6a9ec-114">因此，如果您的用戶端不是最上層字元的作用中用戶端，方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-114">Therefore, the method will fail if your client is not the active client of the topmost character.</span></span> <span data-ttu-id="6a9ec-115">如果您嘗試將方法設為 **False** ，且使用者按下接聽鍵，方法也會失敗。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-115">The method will also fail if you attempt to set the method to **False** and the user is pressing the Listening key.</span></span> <span data-ttu-id="6a9ec-116">如果沒有相容的語音引擎可符合字元的語言識別項設定，或使用者已使用 Microsoft Agent 屬性工作表停用語音輸入，則也可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-116">It can also fail if there is no compatible speech engine available that matches the character's language ID setting or the user has disabled speech input using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="6a9ec-117">不過，若音訊裝置忙碌中，此方法將不會失敗。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-117">However, the method will not fail if the audio device is busy.</span></span>

<span data-ttu-id="6a9ec-118">當您成功將此方法設定為 **True** 時，伺服器會觸發 [**IAgentNotifySinkEx：： ListeningState**](iagentnotifysinkex--listeningstate.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-118">When you successfully set this method to **True**, the server triggers the [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) event.</span></span> <span data-ttu-id="6a9ec-119">當接聽模式超時時間完成時，或當您將 [**IAgentCharacterEx：：接聽**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**)設為 **False** 時，伺服器也會傳送 **IAgentNotifySinkEx：： ListeningState** 。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-119">The server also sends **IAgentNotifySinkEx::ListeningState** when the Listening mode time-out completes or when you set [**IAgentCharacterEx::Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) to **False**.</span></span>

<span data-ttu-id="6a9ec-120">這個方法不會自動呼叫 [**IAgentCharacter：： StopAll**](iagentcharacter--stopall.md) ，並且播放當使用者按下接聽鍵時所發生的字元接聽狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-120">This method does not automatically call [**IAgentCharacter::StopAll**](iagentcharacter--stopall.md) and play a Listening state animation of the character as occurs when the user presses the Listening key.</span></span> <span data-ttu-id="6a9ec-121">這可讓您使用 [**IAgentNotifySinkEx：： ListeningState**](iagentnotifysinkex--listeningstate.md) 事件來判斷是否要停止目前的動畫，並播放您自己的適當動畫。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-121">This enables you to use the [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) event to determine whether you wish to stop the current animation and play your own appropriate animation.</span></span> <span data-ttu-id="6a9ec-122">不過，一旦偵測到使用者語句，伺服器就會自動呼叫 **IAgentCharacter：： StopAll** 並播放聽力狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="6a9ec-122">However, once a user utterance is detected, the server automatically calls **IAgentCharacter::StopAll** and plays a Hearing state animation.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a9ec-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a9ec-123">See Also</span></span>

<span data-ttu-id="6a9ec-124">[**IAgentNotifySinkEx：： ListeningState**](iagentnotifysinkex--listeningstate.md)、 [ **IAgentSpeechInputProperties：： GetEnabled**](iagentspeechinputproperties--getenabled.md)</span><span class="sxs-lookup"><span data-stu-id="6a9ec-124">[**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md), [**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)</span></span>


 

 




