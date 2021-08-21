---
title: AccNameLengthTooLong
description: AccNameLengthTooLong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9df4b9001460b9ad96cf5c987a0e8c744ec8df183901494311275052ea4146
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327704"
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

 

 




