---
title: ClosedCaption 物件
description: ClosedCaption 物件提供一種方式，可包含媒體剪輯的標題。 字幕文字位於已同步處理的可存取媒體交換 (薩米) 檔。
ms.assetid: 5e192aa4-0ecd-4bda-8dad-1750039c7898
keywords:
- ClosedCaption 物件 Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85e53468e8d5cc2694555b9a05d8b207d1660618
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104022693"
---
# <a name="closedcaption-object"></a>ClosedCaption 物件

**ClosedCaption** 物件提供一種方式，可包含媒體剪輯的標題。 字幕文字位於已同步處理的可存取媒體交換 (薩米) 檔。

**ClosedCaption** 物件支援下列屬性。



| 屬性                                           | 描述                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [captioningID](closedcaption-captioningid.md)     | 指定或抓取顯示字幕的框架或控制項名稱。                   |
| [SAMIFileName](closedcaption-samifilename.md)     | 指定或抓取包含隱藏式輔助字幕所需資訊的檔案名。 |
| [SAMILang](closedcaption-samilang.md)             | 指定或抓取隱藏式輔助字幕所顯示的語言。                                 |
| [SAMILangCount](closedcaption-samilangcount.md)   | 抓取目前的薩米文檔案所支援的語言數目。                                |
| [SAMIStyle](closedcaption-samistyle.md)           | 指定或抓取隱藏式輔助字幕樣式。                                                  |
| [SAMIStyleCount](closedcaption-samistylecount.md) | 抓取目前的薩米文檔案所支援的樣式數目。                                   |



 

**ClosedCaption** 物件支援下列方法。



| 方法                                                 | 描述                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [getSAMILangID](closedcaption-getsamilangid.md)       | 抓取目前薩米文檔案所支援之語言 (LCID) 的地區設定識別碼。 |
| [getSAMILangName](closedcaption-getsamilangname.md)   | 抓取目前的薩米文檔案所支援的語言名稱。                     |
| [getSAMIStyleName](closedcaption-getsamistylename.md) | 抓取目前的薩米文檔案所支援的樣式名稱。                        |



 

**ClosedCaption** 物件是透過下列屬性來存取。



| Object                      | 屬性                                  |
|-----------------------------|-------------------------------------------|
| [球員](player-object.md) | [closedCaption](player-closedcaption.md) |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**將隱藏式輔助字幕新增至數位媒體**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




