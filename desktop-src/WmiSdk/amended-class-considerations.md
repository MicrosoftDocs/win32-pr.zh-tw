---
description: 您無法在當地語系化的命名空間中建立修改過之類別的實例。 當地語系化的命名空間中修改過的類別會被視為抽象類別，但它們不包含抽象限定詞。
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: 修改過的類別考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cd38bc6134c4fd3596cc36e8a7638eaa1fd6ed264c90302d921a391982e5d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320237"
---
# <a name="amended-class-considerations"></a>修改過的類別考慮

您無法在當地語系化的命名空間中建立修改過之類別的實例。 當地語系化的命名空間中修改過的類別會被視為抽象類別，但它們不包含 [**抽象**](standard-qualifiers.md) 限定詞。

如果您使用 WBEM 旗標從當地語系化的命名空間抓取修改過的類別 \_ \_ \_ ，請使用修改過的限定詞旗標， \_ 並從中產生實例，此實例就會包含修改過之類別的所有修改過的限定詞。 除非您使用 WBEM 旗標執行 **put** 作業 \_ 使用修改過的 \_ \_ \_ 限定詞旗標，否則您無法將這個新類別儲存在包含基本類別定義的命名空間中。 此旗標會指示 WMI 先移除任何修改過的限定詞，再儲存物件。 如果您未指定 WBEM \_ 旗標 \_ \_ ，請使用修改過的 \_ 限定詞， **put** 作業會失敗，並出現 WBEM E 修改過的 \_ \_ \_ 物件錯誤。

 

 



