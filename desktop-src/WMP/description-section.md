---
title: 描述區段
description: 描述區段
ms.assetid: 280a9a4d-935f-440d-a606-94aeba0007db
keywords:
- Windows Media Player行動外觀、描述區段
- 外觀，描述區段
- 建立外觀，描述區段
- 撰寫面板的程式碼，描述區段
- 外觀中的描述區段
- 外觀定義檔，描述區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96735f07432f8075fe1842d97a4ff1737c65c25ae7ac75ddd61b805460ba6293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118839540"
---
# <a name="description-section"></a>描述區段

接下來，您必須在建立適用于 Windows Mobile 2003 和更新版本的 Windows Media Player 9 系列面板時，提供描述面板大小和方向的區段：


```C++
[ Description ]
//              <X,Y>       <DPI>
//              ------      -----
    Dimensions  240, 320    96

//    <Orientation>
//    -------------
    Orientation Portrait

```



[描述] 區段的開頭必須是以括弧括住的單字描述，然後再包含指定面板之尺寸和顯示解析度的行。

開頭為兩個正斜線的行不會經過處理，而且可以用於批註或（如先前的程式碼所示），以協助您記住一節中的內容。 您也可以使用範本來協助將所有專案對齊資料行。

如需 [描述] 區段的詳細資訊，請參閱面板參考中的 [描述](description.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**撰寫程式碼**](writing-the-code.md)
</dt> </dl>

 

 




