---
description: ViewSpaces 限定詞會定義來源實例所在之命名空間的名稱和位置。 您可以在本機或遠端電腦上指定任何命名空間的組合。
ms.assetid: 15d71bb6-842d-4f5a-b2e3-e9f60f0aea3b
ms.tgt_platform: multiple
title: ViewSpaces 辨識符號
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSpaces
api_type:
- NA
api_location: ''
ms.openlocfilehash: edaec0328d67ad540a12e3393aabf5b973112bbf00f64f735d6a5f64cf338365
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049896"
---
# <a name="viewspaces-qualifier"></a>ViewSpaces 辨識符號

**ViewSpaces 限定詞** 會定義來源實例所在之命名空間的名稱和位置。 您可以在本機或遠端電腦上指定任何命名空間的組合。

下列範例會列出本機電腦上的兩個命名空間。


```mof
ViewSpaces{"\\\\.\\root\\LocalNamespace",
     "\\\\.\\root\\RemoteNamespace"}
```



[視圖提供者](view-provider.md)會依列出查詢和命名空間的順序，將 [ViewSources 限定詞](viewsources-qualifier.md)中的來源查詢與 **ViewSpaces** 辨識符號中列出的命名空間相符。 一般來說， **ViewSpaces** 限定詞中所列的命名空間數目和 **ViewSources** 辨識符號中列出的查詢之間有一對一關聯性。 在某些情況下，您可能會想要針對兩個或多個命名空間來執行 ViewSources 限定詞中所列的查詢。 您可以使用雙冒號 "：：" 來分隔多個命名空間，此命名空間會由 **ViewSources** 陣列中的其中一個查詢來評估。

在下列範例中， [**ViewSources**](viewsources-qualifier.md) 陣列中的第一個查詢會針對第一對引號中的命名空間執行，第二個查詢則針對第二對引號中的三個命名空間，而第三個查詢則是針對第三對引號中的兩個命名空間進行。


```mof
ViewSpaces
    {
    "\\\\.\\root\\LocalNamespace",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace2::
        \\\\.\\root\\RemoteNamespace3",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace3"
    }
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**視圖提供者專用的限定詞**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




