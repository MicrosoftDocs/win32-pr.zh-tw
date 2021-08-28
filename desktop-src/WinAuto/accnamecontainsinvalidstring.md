---
title: AccNameContainsInvalidString
description: AccNameContainsInvalidString
ms.assetid: 392E4D10-4A8E-4118-B0E7-F74571812043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681f9829f3675c469801e8f40325e83865e625b5f3496e865d1ec383c033b7f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955978"
---
# <a name="accnamecontainsinvalidstring"></a>AccNameContainsInvalidString

## <a name="text"></a>Text

accName 不能包含字串 {0}

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

專案名稱包含不正確字元 (這些字元會取代為 AccChecker) 。 例如，用來抓取專案之 MSAA 名稱的 [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) 方法會傳回字串，其中包含定位字元、換行字元或連字號字元。

這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員遇到問題，因為元素可能有 unpronounceable、非直覺的名稱。

## <a name="possible-causes"></a>可能的原因

元素或其父系有不正確指派的名稱或標籤。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IAccessible：： get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name 屬性](name-property.md)
</dt> </dl>

 

 




