---
title: CustomControlTypeWithoutLocalizedControlType
description: CustomControlTypeWithoutLocalizedControlType
ms.assetid: F52E37AB-607B-4899-B59A-3E6EE87FFDA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1970c8e0d4b97de6098f92c8182bfc0045a9e50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507084"
---
# <a name="customcontroltypewithoutlocalizedcontroltype"></a>CustomControlTypeWithoutLocalizedControlType

## <a name="text"></a>Text

元素沒有設定 LocalizedControlType 屬性

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

未設定元素的 [**LocalizedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentlocalizedcontroltype) 屬性。

大部分的螢幕閱讀程式都會讀取當地語系化的控制項類型，以描述元素的本質。 如果未設定當地語系化的控制項類型，螢幕讀取器會切換回以讀取主要控制項類型（一律為英文），而且對所有使用者而言可能沒什麼意義。

## <a name="possible-causes"></a>可能的原因

## <a name="related-topics"></a>相關主題

<dl> <dt>

[LocalizedControlType 屬性](uiauto-controltypesoverview.md)
</dt> <dt>

[**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md)
</dt> </dl>

 

 




