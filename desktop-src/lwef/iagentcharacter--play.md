---
title: IAgentCharacter Play
description: IAgentCharacter Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 996929271156254377f08b9fc41da3932aee9da4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022136"
---
# <a name="iagentcharacterplay"></a><span data-ttu-id="06d35-103">IAgentCharacter：:P 的版面配置</span><span class="sxs-lookup"><span data-stu-id="06d35-103">IAgentCharacter::Play</span></span>

<span data-ttu-id="06d35-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="06d35-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

<span data-ttu-id="06d35-105">播放指定的動畫。</span><span class="sxs-lookup"><span data-stu-id="06d35-105">Plays the specified animation.</span></span>

-   <span data-ttu-id="06d35-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="06d35-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="06d35-107">當函式傳回時， *pdwReqID* 會包含要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="06d35-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="06d35-108"><span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*</span><span class="sxs-lookup"><span data-stu-id="06d35-108"><span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*</span></span>
</dt> <dd>

<span data-ttu-id="06d35-109">動畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d35-109">The name of an animation.</span></span>

</dd> <dt>

<span data-ttu-id="06d35-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="06d35-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="06d35-111">接收 **IAgentCharacter：:P** 配置要求識別碼之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="06d35-111">Address of a variable that receives the **IAgentCharacter::Play** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="06d35-112">使用 Microsoft Agent 字元編輯器來編譯字元時，會定義動畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d35-112">An animation's name is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="06d35-113">在播放指定的動畫之前，伺服器會嘗試播放先前 **動畫的傳回動畫 (** 如果已指派) 的話）。</span><span class="sxs-lookup"><span data-stu-id="06d35-113">Before playing the specified animation, the server attempts to play the **Return** animation for the previous animation (if one has been assigned).</span></span>

<span data-ttu-id="06d35-114">當字元的動畫資料儲存在使用者的本機電腦上時，您可以使用 **IAgentCharacter：:P** 配置方法，並指定動畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d35-114">When a character's animation data is stored on the user's local machine, you can use the **IAgentCharacter::Play** method and specify the name of the animation.</span></span> <span data-ttu-id="06d35-115">使用 HTTP 通訊協定來存取動畫資料時，請在呼叫這個方法之前，先使用 [**Prepare**](iagentcharacter--prepare.md) 方法來確保動畫的可用性。</span><span class="sxs-lookup"><span data-stu-id="06d35-115">When using the HTTP protocol to access animation data, use the [**Prepare**](iagentcharacter--prepare.md) method to ensure the availability of the animation before calling this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="06d35-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06d35-116">See Also</span></span>

[<span data-ttu-id="06d35-117">**IAgentCharacter：:P 準備**</span><span class="sxs-lookup"><span data-stu-id="06d35-117">**IAgentCharacter::Prepare**</span></span>](iagentcharacter--prepare.md)


 

 




