---
title: Parent-Child 視窗互動
description: Parent-Child 視窗互動
ms.assetid: de10bf12-4ba4-4c6b-be56-489e4e2b26b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da43ab5ebe1aa24d8d67b8c901cd3302d8db48ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681998"
---
# <a name="parent-child-window-interaction"></a>Parent-Child 視窗互動

某些系統層級的訊息，例如 [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) 和 [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette)，只會傳送到最上層和重迭的視窗。 如果捕捉視窗是子視窗，其父系必須轉送這些訊息。

同樣地，如果父視窗變更大小，可能需要將通知訊息傳送至 [捕獲] 視窗。 相反地，如果已捕捉的影片的維度變更，則 [捕獲] 視窗可能需要將通知訊息傳送至父視窗。 管理這項工作最簡單的方式，就是一律讓 [捕捉視窗] 維度等於已捕捉的影片資料流程大小，並在這些維度變更時通知父代。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[捕獲 Windows](capture-windows.md)
</dt> </dl>

 

 