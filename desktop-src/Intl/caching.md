---
description: Uniscribe 會將 Unicode (cmap 儲存) 對應、圖像寬度和 OpenType 腳本成形資料表。
ms.assetid: c06c0eaf-41cb-4fd1-9750-a78355217f12
title: '快取 (國際化) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf8bf7dd10fe414bc170086ff9b8c34142dc197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992206"
---
# <a name="caching-internationalization"></a>快取 (國際化) 

Uniscribe 會將 Unicode (cmap 儲存) 對應、圖像寬度和 OpenType 腳本成形資料表。 特定大小之特定字型的資料表控制碼稱為「腳本快取」。 許多 Uniscribe 函式會呼叫裝置內容控制碼參數和腳本快取結構 [**\_**](script-cache.md) 的指標。 這些函式會先查看腳本快取的資訊，只有在需要的資料表尚未快取時，才會使用裝置內容。 呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)、 [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)或 [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) 函式時，應用程式必須將指標傳遞至腳本快 **取 \_** 結構。 當應用程式第一次將它傳遞給 Uniscribe 函式之前，應該將控制碼初始化為 **Null** 。 應用程式絕對不應針對不同的字型或不同的大小傳遞相同的控制碼。

應用程式可以在任何時間釋放腳本快取。 Uniscribe 會維護其字型和整形程式快取中的參考計數，只有在所有字型的大小都釋出時，才會釋出字型資料，而且只有當支援程式的所有字型都釋出時，才會釋出資料。 當應用程式使用樣式完成時，應該呼叫 [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache) 函式來釋放樣式的腳本快取。

針對 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) 和 [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)，應用程式有效地傳遞 null 裝置內容。 最常呼叫會成功，因為已快取所需的資料表。 如果成形或位置需要存取裝置內容， **ScriptShape** 或 **ScriptPlace** 會立即傳回電子 \_ 暫止錯誤碼。 然後，應用程式必須選取裝置內容中的字型。 在大部分的應用程式中，這可避免重複使用 [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject)的呼叫來準備裝置內容控制碼，以協助效能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
