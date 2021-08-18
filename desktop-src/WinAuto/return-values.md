---
title: '傳回值 (Windows 協助工具功能) '
description: 本主題說明最常見的傳回值，以及您可能較不常看到的其他傳回值。
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71595f7a21d932ee961f9fa5f2a9443cf4d63e38de42f3d5b8c89fa8e9f84e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122058"
---
# <a name="return-values-windows-accessibility-features"></a>傳回值 (Windows 協助工具功能) 

本主題說明最常見的傳回值，以及您可能較不常看到的其他傳回值。

## <a name="common-return-values"></a>一般傳回值

[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)方法會傳回下列其中一個值（定義于 winerror.h 中），或另一個標準元件物件模型 (COM) 錯誤碼：



|   值                      |   描述                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ 確定                   | 此方法已成功。                                                                                                                                                                                                                                                                                                                                                                     |
| S \_ FALSE                | 此方法已成功在部分中。 當方法成功時，就會發生這種情況，但無法使用要求的資訊。 例如， \_ 如果您呼叫 [**IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) 在指定的點上抓取子物件，而指定的點不在物件或物件的子系中，Microsoft Active Accessibility 會傳回 S FALSE。 |
| 將 \_ 電子 \_ MEMBERNOTFOUND | 物件不支援要求的屬性或動作。 例如，如果您要求 [值屬性](value-property.md)，則 push 按鈕會傳回這個值，因為它沒有值屬性。                                                                                                                                                                           |
| E \_ >NOTIMPL              | 此方法尚未實作。 當用戶端呼叫該作業系統尚未支援的方法時，就會出現這個值。                                                                                                                                                                                                                                                         |
| E \_ INVALIDARG           | 一或多個引數無效。 當呼叫端嘗試使用伺服器無法辨識的識別碼來識別子物件時，就會發生這個錯誤。 當用戶端嘗試識別沒有子系的物件內的子物件時，也會產生這個錯誤。                                                                                                      |
| E \_ OUTOFMEMORY          | 方法無法配置完成作業所需的記憶體，以順利完成作業。                                                                                                                                                                                                                                                                                        |
| E \_ 失敗                 | 發生不明或一般錯誤。                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a>其他傳回值

以下是 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法可能會傳回的傳回值。 這些傳回值和先前的值並不常見，但您應該注意它們。



|    值                    |    描述                                                                                  |
|------------------------|--------------------------------------------------------------------------------------|
| E \_ ACCESSDENIED        | 當您呼叫 get \_ accValue 來取得密碼控制項的值時，就會傳回此值。 |
| 出現 \_ E \_ 例外狀況     |                                                                                      |
| 共同 \_ 電子 \_ OBJNOTCONNECTED |                                                                                      |



 

 

 




