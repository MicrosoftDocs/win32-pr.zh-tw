---
title: AutoPopupMenu 屬性
description: AutoPopupMenu 屬性
ms.assetid: 499092cb-0990-4edb-915c-12e3011de142
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d4ebfc559c88c3750a338f30b5dee4aad66ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301644"
---
# <a name="autopopupmenu-property"></a>AutoPopupMenu 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定以滑鼠右鍵按一下字元或其工作列圖示，是否會自動顯示字元的快顯功能表。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式。***字元 * **** * * (」CharacterID * * * ) 。AutoPopupMenu* *  \[  =  *布林值*\]



| 部分      | 描述                                                                                                                                                                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | 布林運算式，指定伺服器是否在按一下滑鼠右鍵時，自動顯示該字元的快顯功能表。 **True** (預設) 在滑鼠右鍵按一下時顯示功能表。 <br/> **False** 在滑鼠右鍵按一下時，不會顯示功能表。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

藉由將這個屬性設定為 **False**，您就可以建立自己的功能表處理行為。 若要在將這個屬性設定為 **False** 之後顯示功能表，請使用 [**ShowPopupMenu**](showpopupmenu-method.md) 方法。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**ShowPopupMenu 方法**](showpopupmenu-method.md)


 

 





