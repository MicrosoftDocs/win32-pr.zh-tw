---
title: AccNameLengthTooLong
description: AccNameLengthTooLong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1efcb2b7d13c83a5972cb6e100d70500f9c5ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967446"
---
# <a name="accnamelengthtoolong"></a>AccNameLengthTooLong

## <a name="text"></a>Text

元素的名稱不應傳回長度超過字元的字串 {0}

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

元素名稱包含太多字元。 例如，用來取出元素之 MSAA 名稱的 [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) 方法會傳回大於32000個字元限制的字串。

這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員遇到問題，因為元素可能有 unpronounceable、非直覺的名稱。

## <a name="possible-causes"></a>可能的原因

元素或其父系有不正確指派的名稱或標籤。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IAccessible：： get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name 屬性](name-property.md)
</dt> </dl>

 

 




