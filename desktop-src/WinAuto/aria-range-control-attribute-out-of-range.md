---
title: ARIA 範圍控制項屬性不相容
description: ARIA 範圍控制項屬性不相容
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- AriaRangeControlAttributesIncompatibleId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991f5de18be88682046cac6c4d4156f48fd3e4994d2e7b9ab1bbdc52f0a2e768
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326744"
---
# <a name="aria-range-control-attributes-incompatible"></a>ARIA 範圍控制項屬性不相容

## <a name="text"></a>Text

元素具有 **progressbar** 或 **滑杆** 角色，但公開的 **aria-valuenow** 值位於 **aria valuemin** 的 **aria valuemax** 範圍之外。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤適用于 [**角色**](https://developer.mozilla.org/docs/Web/HTML/Reference) (隱含或明確) 等於 **progressbar**、**滑杆** 或數值 **調整的元素。**

此錯誤表示公開的 [**aria valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 值不在 [**valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 和 [**aria valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性所定義的範圍內。

若要修正這個錯誤，請檢查您的執行，以確定已正確設定 [**aria valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 和 [**aria valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性，並已正確維護 [**aria valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[缺少 ARIA 範圍控制項屬性](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




