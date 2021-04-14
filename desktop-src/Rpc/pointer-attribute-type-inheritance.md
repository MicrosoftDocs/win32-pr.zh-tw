---
title: Pointer-Attribute 類型繼承
description: 根據 DCE 規格，每個 IDL 檔案都必須定義其指標的屬性。
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182b7d46774484a9520424fd82bcff2d7103aa3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382497"
---
# <a name="pointer-attribute-type-inheritance"></a>Pointer-Attribute 類型繼承

根據 DCE 規格，每個 IDL 檔案都必須定義其指標的屬性。 如果未將明確的屬性指派給指標，指標會使用 \[ [指標 \_ default](/windows/desktop/Midl/pointer-default)關鍵字所指定的值 \] 。 某些 DCE 的執行不允許未歸屬指標。 如果指標沒有明確的屬性，IDL 檔案必須具有 **\[ 指標 \_ 預設 \]** 規格，才能設定指標屬性。

在預設的 (Microsoft 擴充功能) 模式中，您可以在匯入定義 IDL 檔案的 IDL 檔案中指定指標的屬性。 在一個 IDL 檔中定義的指標，可以繼承其他 IDL 檔案中指定的屬性。 此外，在預設模式下，IDL 檔案可以包含未歸屬指標。 如果基底和匯入的 IDL 檔案都沒有指定指標屬性或 **\[ 指標 \_ 預設值 \]**，則會將未歸屬指標解釋為唯一指標。

MIDL 編譯器會使用下列優先順序規則，將指標屬性指派給指標 (1 為最高) 。



| 優先順序 | 描述                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| 1        | 明確指標屬性會套用至定義或使用網站上的指標。                                      |
| 2        | 預設值是 IDL 檔案中定義型別的 **\[ 指標 \_ default \]** 屬性。                               |
| 3        | 預設值是匯入類型之 IDL 檔案中的 **\[ 指標 \_ 預設 \]** 屬性。                               |
| 4        | 預設值是 \[ [](/windows/desktop/Midl/ptr) \] DCE 相容性模式中的 Ptr，或 \[ [](/windows/desktop/Midl/unique) \] 在 Microsoft 擴充模式中是唯一的。 |



 

 

 