---
title: 在裝置內容之外使用的 Advanced 函數
description: 這些函式會在裝置內容之外提供先進的色彩管理功能。
ms.assetid: 2f742743-094a-44b8-816b-24246607caeb
keywords:
- Windows色彩系統 (WCS) ，函數
- WCS (Windows 色彩系統) ，函數
- 影像色彩管理，函數
- 色彩管理，函數
- 色彩，函數
- WCS 參考，函數
- WCS、函數的參考
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685b9fe1c7139be1c54e1b158a03c1de54d01b2b80ec4cab4b86603680c6d957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814610"
---
# <a name="advanced-functions-for-use-outside-of-a-device-context"></a>在裝置內容之外使用的 Advanced 函數

這些函式會在裝置內容之外提供先進的色彩管理功能。



| 函式                                                           | 描述                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (或 **ApplyCallbackFunction**) 是一種回呼函式，您會在執行 [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) 函式所顯示的對話方塊時，執行此函數來更新 WCS 設定資料。 |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | 檢查指定點陣圖中的圖元是否位於指定轉換 [的輸出範圍](g.md) 內。 |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | 判斷陣列中的色彩是否位於指定轉換 [的輸出範圍](g.md) 內。 |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | 將命名色彩空間中的色彩名稱轉換成 (ICC) 色彩設定檔的國際色彩協會中的索引編號。 |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | 將色彩空間中的索引轉換為命名色彩空間中的名稱陣列。 |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | 將色彩空間中的索引轉換為命名色彩空間中的名稱陣列。 |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | 接受設定檔的陣列或單一 [裝置連結設定檔](d.md) ，並建立應用程式可用來執行色彩對應的色彩轉換。 |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | 刪除指定的色彩轉換。 |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | 抓取有關建立指定的色彩轉換 (CMM) 之色彩管理模組的各種資訊。 |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | 抓取第一個參數中所指定的「國際色彩協會」 (ICC) 命名色彩設定檔的相關資訊。 |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)         | 用來報告進度的應用程式提供回呼函數。 這個函式的名稱也是由應用程式所定義。                                                 |
| [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) | 可讓您選取慣用的色彩管理模組 (要使用的 CMM) 。 |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                   | 以對話方塊的方式，提供使用者控制項的色彩管理。                                                                                                      |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                 | 使用色彩轉換來轉換點陣圖色彩。                                                                                                                          |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | 將色彩的陣列從來源 [色彩空間](c.md) 轉譯為目的色彩空間，如色彩轉換所定義。 |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                           | 判斷陣列中的色彩是否在指定之 WCS 色彩轉換的輸出範圍內。                                                                |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | 將色彩的陣列從來源色彩空間轉譯為目的色彩空間，如色彩轉換所定義。                                                |



 

 

 




