---
title: 關於 Settings 物件
description: 關於 Settings 物件
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Windows Media Player，Settings 物件
- Windows Media Player 物件模型，Settings 物件
- 物件模型，設定物件
- Windows Media Player ActiveX 控制項，Settings 物件
- ActiveX 控制項，Settings 物件
- Windows Media Player 行動 ActiveX 控制項，Settings 物件
- Windows Media Player Mobile，Settings 物件
- Settings 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20dae51d42e6c67a59ddc23dca19bc7f4180001
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839452"
---
# <a name="about-the-settings-object"></a><span data-ttu-id="485d2-111">關於 Settings 物件</span><span class="sxs-lookup"><span data-stu-id="485d2-111">About the Settings Object</span></span>

<span data-ttu-id="485d2-112">[ **設定** ] 物件控制控制項的設定，例如音量、播放次數、靜音等等。</span><span class="sxs-lookup"><span data-stu-id="485d2-112">The **Settings** object governs the settings of the control such as volume, play count, mute, and so on.</span></span> <span data-ttu-id="485d2-113">它只能透過 **Player** 物件的 **Settings** 屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="485d2-113">It is accessed only through the **Settings** property of the **Player** object.</span></span> <span data-ttu-id="485d2-114">**Settings** 屬性會傳回 **settings** 物件。</span><span class="sxs-lookup"><span data-stu-id="485d2-114">The **Settings** property returns the **Settings** object.</span></span> <span data-ttu-id="485d2-115">建立之後，您只能存取 **設定** 物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="485d2-115">You can only access the properties of the **Settings** object after you have created it.</span></span> <span data-ttu-id="485d2-116">例如，若要取得 **Volume** 屬性的值，您必須使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="485d2-116">For example, to get the value of the **Volume** property, you must use the following code:</span></span>


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a><span data-ttu-id="485d2-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="485d2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="485d2-118">**指令碼語言的播放程式物件模型**</span><span class="sxs-lookup"><span data-stu-id="485d2-118">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="485d2-119">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="485d2-119">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 




