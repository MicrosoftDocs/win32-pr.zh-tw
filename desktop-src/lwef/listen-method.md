---
title: 接聽方法
description: 接聽方法
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813fb155074c4cc47a51ec7241eddd332edbcc3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023347"
---
# <a name="listen-method"></a><span data-ttu-id="bef70-103">接聽方法</span><span class="sxs-lookup"><span data-stu-id="bef70-103">Listen Method</span></span>

<span data-ttu-id="bef70-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="bef70-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bef70-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="bef70-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bef70-106">開啟接聽模式 (語音辨識在一段時間內) 。</span><span class="sxs-lookup"><span data-stu-id="bef70-106">Turns on Listening mode (speech recognition) for a timed period.</span></span>

</dd> <dt>

<span data-ttu-id="bef70-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="bef70-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bef70-108">*代理程式。\*\*\*字元 \* \*\*\*\* \* \* (」CharacterID \* \* \* ) 。接聽* \*  *狀態*</span><span class="sxs-lookup"><span data-stu-id="bef70-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").Listen** *State*</span></span>



| <span data-ttu-id="bef70-109">部分</span><span class="sxs-lookup"><span data-stu-id="bef70-109">Part</span></span>    | <span data-ttu-id="bef70-110">描述</span><span class="sxs-lookup"><span data-stu-id="bef70-110">Description</span></span>                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bef70-111">*State*</span><span class="sxs-lookup"><span data-stu-id="bef70-111">*State*</span></span> | <span data-ttu-id="bef70-112">必要。</span><span class="sxs-lookup"><span data-stu-id="bef70-112">Required.</span></span> <span data-ttu-id="bef70-113">判斷要開啟或關閉接聽模式的布林值。</span><span class="sxs-lookup"><span data-stu-id="bef70-113">A Boolean value that determines whether to turn Listening mode on or off.</span></span> <span data-ttu-id="bef70-114">**True** 開啟接聽模式。</span><span class="sxs-lookup"><span data-stu-id="bef70-114">**True** Turns Listening mode on.</span></span> <br/> <span data-ttu-id="bef70-115">**False** 關閉接聽模式。</span><span class="sxs-lookup"><span data-stu-id="bef70-115">**False** Turns Listening mode off.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bef70-116">備註</span><span class="sxs-lookup"><span data-stu-id="bef70-116">Remarks</span></span>

<span data-ttu-id="bef70-117">將此方法設為 **True** 可啟用接聽模式 (在一段固定時間內開啟語音辨識)  (10 秒) 。</span><span class="sxs-lookup"><span data-stu-id="bef70-117">Setting this method to **True** enables Listening mode (turns on speech recognition) for a fixed period of time (10 seconds).</span></span> <span data-ttu-id="bef70-118">當您無法設定超時值時，您可以在超時時間到期之前關閉接聽模式。</span><span class="sxs-lookup"><span data-stu-id="bef70-118">While you cannot set the value of the time-out, you can turn off Listening mode before the time-out expires.</span></span> <span data-ttu-id="bef70-119">如果您 (或其他用戶端) 成功設定接聽模式，而您嘗試在到期前將此屬性設定為 **True** ，則方法會成功，並重設超時時間。但是，如果接聽模式因為使用者按下接聽鍵而開啟，方法會成功，但是會忽略超時，而且接聽模式會根據使用者與接聽鍵的互動而結束。</span><span class="sxs-lookup"><span data-stu-id="bef70-119">If you (or another client) successfully set Listening mode on and you attempt to set this property to **True** before the time-out expires, the method succeeds and resets the time-out. However, if the Listening mode is on because the user is pressing the Listening key, the method succeeds, but the time-out is ignored and the Listening mode ends based on the user's interaction with the Listening key.</span></span>

<span data-ttu-id="bef70-120">只有當輸入-主動用戶端呼叫，且已啟動語音服務時，此方法才會成功。</span><span class="sxs-lookup"><span data-stu-id="bef70-120">This method succeeds only when called by the input-active client and if speech services have been started.</span></span> <span data-ttu-id="bef70-121">若要確保語音服務已啟動，請查詢或設定 [**SRModeID**](srmodeid-property.md) ，或在您呼叫 **接聽** 之前設定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**語音**](voice-property.md)設定，否則方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="bef70-121">To ensure that speech services have been started, query or set the [**SRModeID**](srmodeid-property.md) or set the [**Voice**](voice-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) before you call **Listen** otherwise the method will fail.</span></span> <span data-ttu-id="bef70-122">若要偵測這個方法是否成功，請呼叫它作為函式，它會傳回布林值，指出方法是否成功。</span><span class="sxs-lookup"><span data-stu-id="bef70-122">To detect the success of this method, call it as a function and it will return a Boolean value indicating whether the method succeeded.</span></span>


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



<span data-ttu-id="bef70-123">如果使用者按下接聽鍵，而您嘗試將 **聆聽** 設定為 **False**，則此方法也會失敗。</span><span class="sxs-lookup"><span data-stu-id="bef70-123">The method also fails if the user is pressing the Listening key and you attempt to set **Listen** to **False**.</span></span> <span data-ttu-id="bef70-124">不過，如果使用者已發行接聽金鑰，且接聽模式尚未超時，則會成功。</span><span class="sxs-lookup"><span data-stu-id="bef70-124">However, if the user has released the Listening key and Listening mode has not timed out, it will succeed.</span></span>

<span data-ttu-id="bef70-125">如果沒有相容的語音引擎可符合字元的 [**LanguageID**](languageid-property.md)設定、使用者已使用 Microsoft Agent 屬性工作表停用語音輸入，或是音訊裝置忙碌中，則 **接聽** 也會失敗。</span><span class="sxs-lookup"><span data-stu-id="bef70-125">**Listen** also fails if there is no compatible speech engine available that matches the character's [**LanguageID**](languageid-property.md) setting, the user has disabled speech input using the Microsoft Agent property sheet, or the audio device is busy.</span></span>

<span data-ttu-id="bef70-126">當您成功將此方法設定為 **True** 時，伺服器會觸發 [**ListenStart**](listenstart-event.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="bef70-126">When you successfully set this method to **True**, the server triggers the [**ListenStart**](listenstart-event.md) event.</span></span> <span data-ttu-id="bef70-127">當接聽模式超時時間完成或您將 [**接聽**] 設定為 [ **False**] 時，伺服器就會傳送 [**ListenComplete**](listencomplete-event.md) 。</span><span class="sxs-lookup"><span data-stu-id="bef70-127">The server sends [**ListenComplete**](listencomplete-event.md) when the Listening mode time-out completes or when you set **Listen** to **False**.</span></span>

<span data-ttu-id="bef70-128">當按下接聽鍵時，此方法不會自動呼叫 [**Stop**](stop-method.md) 並播放接聽狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="bef70-128">This method does not automatically call [**Stop**](stop-method.md) and play a Listening state animation as the server does when the Listening key is pressed.</span></span> <span data-ttu-id="bef70-129">這可讓您藉由呼叫「**停止**」並播放自己的適當動畫，判斷是否要使用 [**ListenStart**](listenstart-event.md)動畫來中斷目前的動畫。</span><span class="sxs-lookup"><span data-stu-id="bef70-129">This enables you to determine whether to interrupt the current animation using the [**ListenStart**](listenstart-event.md) animation by calling **Stop** and playing your own appropriate animation.</span></span> <span data-ttu-id="bef70-130">但是，當偵測到使用者語句時，伺服器會呼叫 **Stop** 並播放聽力狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="bef70-130">However, the server does call **Stop** and plays a Hearing state animation when a user utterance is detected.</span></span>

## <a name="see-also"></a><span data-ttu-id="bef70-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bef70-131">See Also</span></span>

<span data-ttu-id="bef70-132">[**LanguageID 屬性**](languageid-property.md)、 [**ListenComplete 事件**](listencomplete-event.md)、 [**ListenStart 事件**](listenstart-event.md)</span><span class="sxs-lookup"><span data-stu-id="bef70-132">[**LanguageID property**](languageid-property.md), [**ListenComplete event**](listencomplete-event.md), [**ListenStart event**](listenstart-event.md)</span></span>


 

