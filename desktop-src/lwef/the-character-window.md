---
title: 字元視窗
description: 字元視窗
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426aab4cbd6e0ad536135cb47ec9a636ea56a0509f3fb0cb75ad6440addc62da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474884"
---
# <a name="the-character-window"></a>字元視窗

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

Microsoft Agent 會在自己的視窗中顯示動畫字元，這些字元一律會出現在視窗迭置順序的最上方， (也就是一律在最上層) 。 使用者可以拖曳字元與滑鼠左鍵，以移動字元的視窗。 字元影像會隨著指標移動。 此外，應用程式可以使用 [**MoveTo**](moveto-method.md) 方法移動字元。

當使用者以滑鼠右鍵按一下某個字元時，會出現顯示下列命令的快顯功能表：

開啟 \| Close <span class="underline">V</span>oice 命令視窗

<span class="underline">H</span>ide

----------------------------…

命令\*


*OtherHostingApplicationCaption\*\**

\*列出的命令是以輸入-主動用戶端為基礎。 如需有關定義快顯功能表中所顯示命令的詳細資訊，請參閱 Microsoft Agent 程式設計介面總覽。

\*\*列出的專案是目前裝載該字元的其他所有應用程式。 如需定義此專案的詳細資訊，請參閱 Microsoft Agent 程式設計介面總覽。

[開啟 \| 關閉語音命令] 視窗命令會控制目前作用中字元的 [命令] 視窗的顯示。 如果已停用語音辨識服務，則會停用此命令。 如果未安裝語音辨識服務，則不會出現此命令。

隱藏命令會隱藏字元。 指派給字元 **隱藏** 狀態的動畫會播放並隱藏該字元。 [隱藏] 中的字母 "H" 是命令的存取金鑰 (助憶鍵) 。

應用程式 (s 的命令) 目前裝載字元在 Hide 命令後面，前面會加上分隔符號。 然後，其他使用該字元的應用程式名稱也會出現在分隔符號前面。

 

 




