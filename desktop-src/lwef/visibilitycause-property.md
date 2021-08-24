---
title: VisibilityCause 屬性
description: VisibilityCause 屬性
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1e90b77dfdfae364761254676d0867a43aebacf516d4f2adad2973700d7e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398788"
---
# <a name="visibilitycause-property"></a>VisibilityCause 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回整數值，指定造成字元可見狀態的原因。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式*。**( "**_CharacterID_*_" ) 的字元。VisibilityCause_*



| 值 | 描述                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| 0     | 未顯示字元。                                                                            |
| 1     | 使用者會在字元的工作列圖示快顯功能表上使用命令或使用語音輸入來隱藏字元。 |
| 2     | 使用者顯示字元。                                                                               |
| 3     | 您的應用程式會隱藏該字元。                                                                          |
| 4     | 您的應用程式會顯示該字元。                                                                       |
| 5     | 另一個用戶端應用程式會隱藏該字元。                                                                |
| 6     | 另一個用戶端應用程式會顯示該字元。                                                             |
| 7     | 使用者會使用字元快顯功能表上的命令，將字元隱藏起來。                                 |



 

</dd> </dl>

## <a name="remarks"></a>備註

您可以使用這個屬性來判斷當有多個應用程式正在共用 (載入) 相同字元時，造成字元移動的原因。 這些值與 [**顯示**](show-event.md) 和 [**隱藏**](hide-event.md) 事件所傳回的值相同。

## <a name="see-also"></a>另請參閱

[**隱藏事件**](hide-event.md)、 [**顯示事件**](show-event.md)、 [**隱藏方法**](hide-method.md)、 [**顯示方法**](show-method.md)


 

 




