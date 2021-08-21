---
title: Visual Basic私用介面
description: Visual Basic私用介面
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd69e70d351245ebafa62d521a133726be568a0437f4e04ece4ef761535f4625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047706"
---
# <a name="visual-basic-private-interfaces"></a>Visual Basic私用介面

在這裡會為元件類別識別 Visual Basic 所執行的兩個介面。 控制項應該不需要這些類別，因為控制項可能會在無法使用時提供替代功能。

[**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat)介面可讓控制項在格式化資料時，更妥善地整合到 Visual Basic 環境中。

CATID-{02496840-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBFormat

[**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol)介面可讓控制項列舉 VB 表單上的其他控制項。

CATID-{02496841-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBGetControl

另外還有兩個額外的私用介面（ [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) 和 [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject)），雖然它們並未定義元件類別。 不建議使用這四個介面，因為 Visual Basic 以外的容器不支援這些介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[元件類別](component-categories.md)
</dt> </dl>

 

 




