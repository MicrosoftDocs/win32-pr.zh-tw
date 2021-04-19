---
title: '色彩管理模組的 WCS 函式 (要執行的 Cmm) '
description: 下列函式是由彩色管理模組執行 (Cmm) ，並針對作業系統進行匯出以供呼叫。
ms.assetid: e05129ec-9128-44f0-82c7-f4e01536d7a8
keywords:
- Windows Color System (WCS) ，函數
- WCS (Windows 色彩系統) ，函數
- 影像色彩管理，函數
- 色彩管理，函數
- 色彩，函數
- WCS 參考，函數
- WCS、函數的參考
- 'Windows Color System (WCS) 、色彩管理模組 (CMM) '
- 'WCS (Windows 色彩系統) 、色彩管理模組 (CMM) '
- '影像色彩管理、色彩管理模組 (CMM) '
- '色彩管理、色彩管理模組 (CMM) '
- '色彩、色彩管理模組 (CMM) '
- 'WCS 參考、色彩管理模組 (CMM) '
- 'WCS 的參考、色彩管理模組 (CMM) '
- '色彩管理模組 (CMM) '
- " (色彩管理模組) 的 CMM"
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e9092c49077b1b4dda9e06829329194ec2e261
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106986679"
---
# <a name="wcs-functions-for-color-management-modules-cmms-to-implement"></a>色彩管理模組的 WCS 函式 (要執行的 Cmm) 

下列函式是由彩色管理模組執行 (Cmm) ，並針對作業系統進行匯出以供呼叫。



| 函式                                                                     | 描述                                                                               |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**CMCheckColors**](/windows/win32/api/icm/nf-icm-cmcheckcolors) | 判斷指定的色彩是否位於指定轉換 [的輸出範圍](./g.md) 內。 |
| [**CMCheckColorsInGamut**](/windows/win32/api/icm/nf-icm-cmcheckcolorsingamut) | 判斷指定的 RGB 三合一是否位於指定轉換 [的輸出範圍](./g.md) 中。 |
| [**CMCheckRGBs**](/windows/desktop/api/Wingdi/)                                           | 針對輸出範圍檢查點陣圖色彩。                                             |
| [**CMConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-cmconvertcolornametoindex) | 將命名色彩空間中的色彩名稱轉換成色彩設定檔中的索引編號 |
| [**CMConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-cmconvertindextocolorname) | 將色彩空間中的索引轉換為命名色彩空間中的名稱陣列。 |
| [**CMCreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-cmcreatedevicelinkprofile) | 以國際色彩協會在其 ICC 配置檔案格式規格中指定的格式建立 [裝置連結設定檔](./d.md) 。 |
| [**CMCreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-cmcreatemultiprofiletransform) | 接受設定檔的陣列或單一 [裝置連結設定檔](./d.md) ，並建立色彩轉換。 這項轉換是從第一個設定檔所指定的色彩空間到第二個設定檔的對應，依此類推到最後一個設定檔的對應。 |
| [**CMCreateProfile**](/windows/win32/api/icm/nf-icm-cmcreateprofile) | 從 [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) 結構建立顯示色彩設定檔。 |
| [**CMCreateProfileW**](/windows/win32/api/icm/nf-icm-cmcreateprofilew) | 從 [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) 結構建立顯示色彩設定檔。 |
| [**CMCreateTransform**](/windows/win32/api/icm/nf-icm-cmcreatetransform) | 已取代。 沒有取代的 API，因為不再使用此 API。 不需要替代的 CMM 模組開發人員來執行它。 |
| [**CMCreateTransformExt**](/windows/win32/api/icm/nf-icm-cmcreatetransformext) | 建立從輸入 [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) 對應至選擇性目標空間的色彩轉換，然後使用一組旗標來定義應如何建立轉換，以將其對應至輸出裝置。 |
| [**CMCreateTransformExtW**](/windows/win32/api/icm/nf-icm-cmcreatetransformextw) | 建立從輸入 [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) 對應至選擇性目標空間的色彩轉換，然後使用一組旗標來定義應如何建立轉換，以將其對應至輸出裝置。 |
| [**CMCreateTransformW**](/windows/win32/api/icm/nf-icm-cmcreatetransformw) | 已取代。 沒有取代的 API，因為不再使用此 API。 不需要替代的 CMM 模組開發人員來執行它。 |
| [**CMDeleteTransform**](/windows/win32/api/icm/nf-icm-cmdeletetransform) | 刪除指定的色彩轉換，並釋出任何與其相關聯的記憶體。 |
| [**CMGetInfo**](/windows/win32/api/icm/nf-icm-cmgetinfo) | 抓取 (CMM) 的色彩管理模組的各種相關資訊。 |
| [**CMGetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-cmgetnamedprofileinfo) | 抓取指定之命名色彩設定檔的相關資訊。 |
| [**CMGetPS2ColorRenderingDictionary**](/windows/desktop/api/Wingdi/) | 取得 PostScript 色彩轉譯字典。                                             |
| [**CMGetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-cmgetps2colorrenderingintent) | 從設定檔抓取 PostScript 層級2色彩轉譯 [意圖](rendering-intents.md) 。 |
| [**CMGetPS2ColorSpaceArray**](/windows/desktop/api/Wingdi/)                   | 取得 PostScript 色彩空間陣列。                                                      |
| [**CMIsProfileValid**](/windows/win32/api/icm/nf-icm-cmisprofilevalid) | 報告指定的設定檔是否為可用於色彩管理的有效 ICC 設定檔。 |
| [**CMTranslateColors**](/windows/win32/api/icm/nf-icm-cmtranslatecolors) | 使用色彩轉換，將色彩的陣列從來源 [色彩空間](rendering-intents.md) 轉譯為目的色彩空間。 |
| [**CMTranslateRGB**](/windows/win32/api/icm/nf-icm-cmtranslatergb) | 將應用程式提供的 RGBQuad 轉譯成裝置 [色彩空間](color-spaces.md)。 |
| [**CMTranslateRGBs**](/windows/win32/api/icm/nf-icm-cmtranslatergbs) | 使用色彩轉換，將點陣圖從某個 [色彩空間](color-spaces.md) 轉譯成另一個。 |
| [**CMTranslateRGBsExt**](/windows/win32/api/icm/nf-icm-cmtranslatergbsext) | 將點陣圖從一個已定義的格式轉譯為不同的定義格式，並定期呼叫回呼函式（如果有指定），以報告進度並允許呼叫應用程式終止翻譯。 |



 

 

 