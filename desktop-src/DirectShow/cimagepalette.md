---
description: CImagePalette 類別會管理影片轉譯器的調色板。 可以用來從影片格式建立邏輯調色板。 此類別的目的是要搭配 CBaseWindow 和 CDrawImage 類別使用，因此它有點特製化。
ms.assetid: dcbe5049-0e8c-4221-825a-0fd8e6efd2a5
title: CImagePalette 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette
api_type:
- COM
api_location: ''
ms.openlocfilehash: 696c51e4918815e18accbadd66c764493dc0b98e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970877"
---
# <a name="cimagepalette-class"></a>CImagePalette 類別

`CImagePalette`類別會管理影片轉譯器的調色板。 可以用來從影片格式建立邏輯調色板。 此類別的目的是要搭配 [**CBaseWindow**](cbasewindow.md) 和 [**CDrawImage**](cdrawimage.md) 類別使用，因此它有點特製化。



| 受保護的成員變數                                       | Description                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**m \_ hPalette**](cimagepalette-m-hpalette.md)                  | 這個物件管理的邏輯元件的控制碼。                                        |
| [**m \_ pBaseWindow**](cimagepalette-m-pbasewindow.md)            | 管理視窗之 **CBaseWindow** 物件的指標。                                 |
| [**m \_ pDrawImage**](cimagepalette-m-pdrawimage.md)              | **CDrawImage** 物件的指標，該物件會繪製影片影像。                               |
| [**m \_ pFilter**](cimagepalette-m-pfilter.md)                    | 擁有篩選準則的指標。                                                                  |
| 公用方法                                                   | Description                                                                                    |
| [**CImagePalette**](cimagepalette-cimagepalette.md)             | 函式方法。                                                                            |
| [**CopyPalette**](cimagepalette-copypalette.md)                 | 將 **VIDEOINFO** 結構中的元件複製到任何調色盤 **VIDEOINFO** 結構。 |
| [**MakeIdentityPalette**](cimagepalette-makeidentitypalette.md) | 嘗試建立直接對應至顯示裝置中所選取之調色板的調色板。   |
| [**MakePalette**](cimagepalette-makepalette.md)                 | 從色彩表以影片格式建立邏輯調色板。                              |
| [**PreparePalette**](cimagepalette-preparepalette.md)           | 根據擁有篩選器中的媒體類型，設定調色板。                               |
| [**RemovePalette**](cimagepalette-removepalette.md)             | 刪除現有的邏輯調色板。                                                          |



 

 

 



