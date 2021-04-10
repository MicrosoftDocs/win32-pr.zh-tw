---
title: 'VariantNotInt (CheckState) '
description: 'VariantNotInt (CheckState) '
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d951a51ae6aa3f4d9454fc95a56c76cfe30500c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183516"
---
# <a name="variantnotint-checkstate"></a>VariantNotInt (CheckState) 

## <a name="text"></a>Text

從傳回的變異數 {0} 應為， {1} 但為 {2} 。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

元素報告的 MSAA 狀態無效。 例如，用來取出專案之 MSAA 狀態的 [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) 方法，應該傳回代表其中一個 msaa 狀態常數的整數值，但改為傳回另一個 variant。

這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員遇到問題，因為可能會向使用者回報不正確的元素狀態。

## <a name="possible-causes"></a>可能的原因

元素或其父系的 MSAA 狀態設定不當。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IAccessible：： get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**物件狀態常數**](object-state-constants.md)
</dt> </dl>

 

 




