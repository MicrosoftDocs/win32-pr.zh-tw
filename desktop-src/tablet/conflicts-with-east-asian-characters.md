---
description: 某些應用程式手勢可能與東亞字元或東亞字元組合相衝突。
ms.assetid: 56ff773f-ef95-47f8-ba04-2593330867ee
title: 與 East-Asian 字元衝突
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb12b9fab1389395b249f35da3dc5ffbfc91af83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112012"
---
# <a name="conflicts-with-east-asian-characters"></a>與 East-Asian 字元衝突

某些 *應用程式手勢* 可能與東亞字元或東亞字元組合相衝突。 下表列出應用程式中具有特定東亞字元輸入之應用程式的手勢和字元之間可能發生的衝突。



| 手勢                 | 簡體中文 | 繁體中文 | 日文     | 韓文       |
|-------------------------|----------------------|-----------------------|--------------|--------------|
| Down<br/>         | X<br/>         | X<br/>          | X<br/> | X<br/> |
| Right<br/>        | X<br/>         | X<br/>          | X<br/> | X<br/> |
| DownRight<br/>    | -<br/>         | X<br/>          | -<br/> | X<br/> |
| RightDown<br/>    | -<br/>         | -<br/>          | X<br/> | X<br/> |
| Circle<br/>       | -<br/>         | -<br/>          | -<br/> | X<br/> |
| ChevronRight<br/> | -<br/>         | -<br/>          | -<br/> | X<br/> |



 

Microsoft 持續致力於開發 *手勢*。 Microsoft 認為在組建應用程式、獨立軟體廠商 (Isv) 需要知道哪些動作會對應到手勢。 未執行的字元[會列出一](unimplemented-glyphs.md)組 Microsoft 計畫對應手勢的畫筆動作，以及要保留給動作的手勢。 系統會提供這項資訊，讓您知道未來將提供哪些動作和手勢。

除了使用 Microsoft Windows XP Tablet PC Edition 中提供的手勢之外，應用程式也可以自由建立自己的手勢。 然後，應用程式開發人員所建立的 *Microsoft 手勢辨識器* 可以辨識這些手勢。 如果您想要執行任何自己的手勢，請參考未執行的字元，以避免與 Microsoft 計畫要實施的 [手勢重迭](unimplemented-glyphs.md) 。

 

 




