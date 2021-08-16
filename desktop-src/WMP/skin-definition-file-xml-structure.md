---
title: 外觀定義檔案 XML 結構
description: 外觀定義檔案 XML 結構
ms.assetid: 93325b94-667a-42a6-92f8-78288d36da81
keywords:
- 建立外觀、面板定義檔
- 面板定義檔 Windows Media Player 的外觀
- 外觀、面板定義檔
- 面板的檔案、外觀定義
- 外觀定義檔案，XML 結構
- 外觀定義檔案的 XML 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc3506ab03d3af7445e75983299577c713412fbeb0899d39c7098c55be2450a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995248"
---
# <a name="skin-definition-file-xml-structure"></a>外觀定義檔案 XML 結構

面板定義檔是以 XML 撰寫的。 XML 的其中一個重要功能是完整結構化，而且類似于大綱。 XML 程式碼只是一系列的元素，例如 **VIEW** 和 **BUTTONGROUP**。 您將從元素開始，然後使用屬性來定義它們。 本教學課程的其餘部分將提供屬性的詳細資料，但以下是將使用的元素大綱：


```C++
<THEME>
    <VIEW>
        <BUTTONGROUP>
            <BUTTONELEMENT/>
            <BUTTONELEMENT/>
        </BUTTONGROUP>
    </VIEW>
<THEME>

```



請記住專案的簡單結構，讓每個專案都能成為唯一的屬性。 本節的其餘主題將涵蓋每個元素的詳細資料。 如需有關元素和屬性的詳細資訊，請參閱面板程式 [設計參考](skin-programming-reference.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立外觀定義檔**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




