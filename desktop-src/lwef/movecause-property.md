---
title: MoveCause 屬性
description: MoveCause 屬性
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa797338e64edfd67ae2347f2983df624464df923a64883e3adc5143671b15dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883829"
---
# <a name="movecause-property"></a>MoveCause 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回整數值，指定造成字元上一次移動的原因。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式*。**( "**_CharacterID_*_" ) 的字元。MoveCause_*



| 值 | 描述                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| 0     | 尚未移動字元。                                                          |
| 1     | 使用者移動字元。                                                              |
| 2     | 您的應用程式移動了該字元。                                                      |
| 3     | 另一個用戶端應用程式移動字元。                                            |
| 4     | 代理程式伺服器移動字元，以在螢幕解析度變更之後讓它保持在畫面上。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

當有多個應用程式正在共用 (載入) 相同的字元時，您可以使用這個屬性來判斷造成字元移動的原因。 這些值與 [**移動**](move-event.md) 事件所傳回的值相同。

## <a name="see-also"></a>另請參閱

[**移動事件**](move-event.md)， [ **MoveTo 方法**](moveto-method.md)


 

 




