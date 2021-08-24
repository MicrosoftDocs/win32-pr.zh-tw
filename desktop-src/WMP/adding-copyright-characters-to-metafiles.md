---
title: 將著作權字元新增至中繼檔
description: 著作權和商標注冊符號的字元 ( \ 169;或 \ 174;如果未使用 UTF-8 編碼配置來編碼中繼檔，) 可能無法正確顯示。
ms.assetid: 9124c8d4-1fc1-4163-ada9-d96af58f8b98
keywords:
- 將著作權字元新增至中繼檔 Windows Media Player
topic_type:
- apiref
api_name:
- Adding Copyright Characters to Metafiles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b0ab5fc4e539331406bb776a4bcdacbed6578a234dd9e84a3c358cdbe9936ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865158"
---
# <a name="adding-copyright-characters-to-metafiles"></a>將著作權字元新增至中繼檔

如果未使用 UTF-8 編碼配置來編碼中繼檔，則著作權和商標注冊符號 ( ©或® ) 的字元可能無法正確顯示。 在此情況下，若要為所有使用者適當地顯示這些符號的其中一個，您可以使用 (c) 的 ASCII 對等專案，並在 **著作權** 元素內 (r) ，如下列程式碼所示。


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



如果中繼檔是使用 UTF-8 編碼，則著作權和商標符號將會正確顯示。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Windows媒體中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




