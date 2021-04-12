---
title: VisibilityCause 屬性
description: VisibilityCause 屬性
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6e21e2cda201f8d04837d2b10efc757b93f824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372226"
---
# <a name="visibilitycause-property"></a>VisibilityCause 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回整數值，指定造成字元可見狀態的原因。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式*。**( "***CharacterID***" ) 的字元。VisibilityCause**



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


 

 




