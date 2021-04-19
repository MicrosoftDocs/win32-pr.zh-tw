---
description: 為了協助支援應用程式中的筆跡，有兩個物件可以內嵌，而且任何 OLE 容器都支援這些物件，文字筆墨物件 (tInk) 和草圖筆墨物件 (接收) 。
ms.assetid: 0202e91c-c7a0-4e7b-a1c6-a2f58c11c0be
title: 使用文字筆墨物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082323f7e67e76f7ae39c6b592a86f2be0945a86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972445"
---
# <a name="working-with-the-text-ink-object"></a>使用文字筆墨物件

為了協助支援應用程式中的筆跡，有兩個物件可以內嵌，而且任何 OLE 容器都支援這些物件，文字筆墨物件 (tInk) 和草圖筆墨物件 (接收) 。

文字筆墨物件是代表預期會形成單字之筆墨的 OLE 物件。 文字筆墨物件可從替代清單中選擇，以將手寫筆墨轉換成文字。 您可以透過程式設計方式設定文字筆墨物件的色彩和大小，而且可以根據物件周圍文字的屬性來設定。 文字筆墨物件的目的是要包含單一單字。

文字筆墨物件支援內嵌和剪貼簿支援所需的一組標準 OLE 介面。 [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)介面會以筆跡序列化格式讀取和寫入資料流程， (ISF) 。 文字筆墨物件提供 [**IInkLineInfo**](/windows/desktop/api/msinkaut/nn-msinkaut-iinklineinfo) 介面，可存取其顯示內容和辨識結果清單。

文字筆墨物件可用於應用程式之間的互通性，方法是將它放在剪貼簿上的 OLE 物件位置，或將它內嵌在 .RTF 資料流程中，或將它保存在 ISF 資料流程中。

您可以透過下列方式產生文字筆墨物件。

-   [InkEdit](inkedit-control-reference.md)控制項會使用文字筆墨物件。 InkEdit 控制項的功能是標準 RichEdit 控制項功能的超級集合。 筆墨會以文字筆墨物件的形式插入 InkEdit 控制項的 RTF 資料流程中。
-   當應用程式將 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 或 [InkEdit](inkedit-control-reference.md) 物件複製到剪貼簿，並設定 [**INKCLIPBOARDFORMATS 列舉**](/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardformats) 格式時，ole 物件剪貼簿位置會包含文字筆墨 OLE 物件。
-   Tablet PC 輸入面板可以產生文字筆墨物件。

例如，您的應用程式可以辨識手寫，並將辨識結果新增至筆劃。 然後，如果您將筆劃複製並貼入 Microsoft Word 作為文字筆墨物件，Word 2003 和更新版本中就會提供該單字的替代項。

為了成功包含文字筆墨物件，應用程式必須針對内嵌物件執行 OLE 容器支援。 然後，若要讓容器完全支援文字筆墨，您必須建立：

-   修改應用程式以進行尋找和取代。 這些物件的類型必須是查核，而不是略過搜尋中的內嵌物件。 如果它們是文字筆墨物件，則必須將它們具現化並針對其對應的文字進行查詢。
-   修改選取行為。 文字筆墨物件的選取範圍絕對不能與調整大小控點一起出現。 它們的選取方式應該與檔中選取文字的方式相同。 物件的選取程式碼必須偵測型別是否為文字筆墨，並適當地顯示選取範圍。
-   環境屬性的使用。 字型大小、色彩和粗體格式等環境屬性必須傳送至文字筆墨物件。 這些屬性的應用會變更手寫筆跡的寬度，因此需要透過呼叫 [**IInkLineInfo：： GetInkExtent**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) 或 [**IOleObject：： GetExtent**](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent) 方法來更新大小。

## <a name="in-this-section"></a>本節內容

-   [將文字筆墨物件轉換成筆墨](converting-a-text-ink-object-to-ink.md)
-   [文字筆墨 Api](text-ink-apis.md)
-   [sInk 和 tInk 物件](sink-and-tink-objects.md)

 

 
