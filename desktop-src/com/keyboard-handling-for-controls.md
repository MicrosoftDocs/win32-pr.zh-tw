---
title: 控制項的鍵盤處理
description: 控制項會回應鍵盤快速鍵，讓終端使用者可以起始控制項所執行的動作。
ms.assetid: 59aca5cb-f109-49ee-897d-43610501f7f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26081d36c62b11163ceb8c41421ea0370d18b3ce9bf16be68e4e8a06a5f1a489
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736555"
---
# <a name="keyboard-handling-for-controls"></a>控制項的鍵盤處理

控制項會回應鍵盤快速鍵，讓終端使用者可以起始控制項所執行的動作。 容器會管理其所有內嵌控制項的鍵盤活動。 使用複合檔案時，鍵盤快速鍵只會套用至目前作用中的物件。 使用控制項時，已新增一個機制，讓控制項可以回應其鍵盤助憶鍵，即使它目前不是 UI 作用中也一樣。

[**IOleControl：： GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo)和 [**IOleControl：： OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)方法和 [**>iolecontrolsite：： OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged)方法會處理控制項的鍵盤助憶鍵。 [**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo)結構描述控制項的助憶鍵加速器，而且透過 **GetControlInfo** 方法傳遞給它的旗標會以 Enter 和 Esc 鍵描述控制項行為。 當控制項變更其助憶鍵時，它會呼叫 **OnControlInfoChanged** ，讓容器可以在必要時重載結構。

當控制項是 UI 作用中時，它也是具有焦點的控制項。 當控制項在就地作用中和 UI 作用中狀態之間啟用和停用時，控制項會呼叫 [**>iolecontrolsite：： OnFocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) 來告訴容器這類變更。

此外，當控制項是 UI 作用中時，它會先有機會處理任何擊鍵。 為了讓容器有機會在控制項之前處理按鍵，控制項會呼叫 [**>iolecontrolsite：： TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)。 如果容器沒有處理按鍵，控制項接著會處理它。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ActiveX控制](activex-controls.md)
</dt> </dl>

 

 




