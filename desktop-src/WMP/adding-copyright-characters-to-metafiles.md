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
ms.openlocfilehash: 6e71b116a3500fdb4217613c81bd4f041af75a66
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312506"
---
# <a name="adding-copyright-characters-to-metafiles"></a><span data-ttu-id="a63f1-104">將著作權字元新增至中繼檔</span><span class="sxs-lookup"><span data-stu-id="a63f1-104">Adding Copyright Characters to Metafiles</span></span>

<span data-ttu-id="a63f1-105">如果未使用 UTF-8 編碼配置來編碼中繼檔，則著作權和商標注冊符號 ( ©或® ) 的字元可能無法正確顯示。</span><span class="sxs-lookup"><span data-stu-id="a63f1-105">The characters for copyright and trademark registration symbols ( © or ® ) may not display correctly if the metafile is not encoded using the UTF-8 encoding scheme.</span></span> <span data-ttu-id="a63f1-106">在此情況下，若要為所有使用者適當地顯示這些符號的其中一個，您可以使用 (c) 的 ASCII 對等專案，並在 **著作權** 元素內 (r) ，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="a63f1-106">In this case, to display either of these symbols properly for all users, you can use the ASCII equivalents (c) and (r) inside the **COPYRIGHT** element, as shown in the following code.</span></span>


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



<span data-ttu-id="a63f1-107">如果中繼檔是使用 UTF-8 編碼，則著作權和商標符號將會正確顯示。</span><span class="sxs-lookup"><span data-stu-id="a63f1-107">If the metafile is encoded using UTF-8, copyright and trademark symbols will display correctly.</span></span>

## <a name="see-also"></a><span data-ttu-id="a63f1-108">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a63f1-108">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a63f1-109">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="a63f1-109">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




