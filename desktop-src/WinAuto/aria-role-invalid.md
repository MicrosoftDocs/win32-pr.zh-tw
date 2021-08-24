---
title: ARIA 角色錯誤
description: ARIA 角色錯誤
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- AriaRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c0fcef639a54bcd805bcb3f239e8d42cfeda8c5111d128c5f54157db75d7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134011"
---
# <a name="aria-role-error"></a>ARIA 角色錯誤

## <a name="text"></a>Text

元素有不正確 WAI-ARIA 角色。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤適用于具有 [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) 屬性的所有元素。 這表示 **role** 屬性不是有效的 Web 協助工具計畫可存取的豐富網際網路應用程式， (WAI-aria) 角色值，如 WAI-aria 規格所定義。 設定有效的角色有助於確保螢幕讀取器和其他輔助技術工具可以正確地解讀元素。

若要修正這個錯誤，請將 [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) 屬性設為有效的 WAI-ARIA 角色值。 請注意，abstract WAI-ARIA 角色無效。

## <a name="example"></a>範例


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ARIA 容器角色錯誤](aria-container-role.md)
</dt> </dl>

 

 




