---
description: 資源的需求
ms.assetid: 6b654cd6-7e9f-4e12-a687-4110e600ba7b
title: 資源的需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca302fcd11abf4bbadc1adfafb1a1be67141055ea7f9a5366991f231cca44fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027145"
---
# <a name="requirements-for-resources"></a>資源的需求

Windows可攜式裝置會將下列資源類別定義為 **PROPERTYKEY** 值。 這些值是用來描述物件中的個別資源。 屬性索引鍵的 *pid* 成員可以不同，以描述相同類型之相同類型的不同資源，但 **WPD \_ 資源 \_ 預設** 除外，但只能描述一項資源。 每個資源類型的連結描述頁面會列出該資源所支援的屬性。



| 資源 PROPERTYKEY                                                | 描述                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**WPD \_ 資源 \_ 預設**](wpd-resource-default.md)              | 指定物件後方的整個檔案。 這是具有資源之任何物件的唯一必要資源。 |
| [**WPD \_ 資源 \_ 專輯 \_ 封面**](wpd-resource-album-art.md)         | 指定代表物件之專輯作品的影像。                                           |
| [**WPD \_ 資源 \_ 音訊 \_ 剪輯**](wpd-resource-audio-clip.md)       | 指定物件的音訊剪輯。                                                                        |
| [**WPD \_ 資源 \_ 連絡人 \_ 相片**](wpd-resource-contact-photo.md) | 指定代表 contact 物件中所參考之個別相片的影像。                |
| [**WPD \_ 資源 \_ 泛型**](wpd-resource-generic.md)              | 未定義資料類型的一般資源。 這應該被視為位元組陣列。                             |
| [**WPD \_ 資源 \_ 圖示**](wpd-resource-icon.md)                    | 圖示。                                                                                                       |
| [**WPD \_ 資源 \_ 縮圖**](wpd-resource-thumbnail.md)          | 縮圖影像。                                                                                             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計參考**](programming-reference.md)
</dt> </dl>

 

 



