---
title: 裝置校正和特性函數
description: 下列函式適用于撰寫裝置校正，以及安裝和校準色彩顯示裝置（例如監視器和印表機）所需的特性工具。
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- Windows Color System (WCS) ，函數
- WCS (Windows 色彩系統) ，函數
- 影像色彩管理，函數
- 色彩管理，函數
- 色彩，函數
- WCS 參考，函數
- WCS、函數的參考
- Windows Color System (WCS) 、裝置校正
- WCS (Windows 色彩系統) ，裝置校正
- 影像色彩管理、裝置校正
- 色彩管理，裝置校正
- 色彩，裝置校正
- WCS 參考，裝置校正
- WCS、裝置校正的參考
- Windows Color System (WCS) ，特性
- WCS (Windows 色彩系統) ，特性
- 影像色彩管理，特性
- 色彩管理，特性
- 色彩，特性
- WCS 參考，特性
- WCS 的參考，特性
- 裝置校正
- 校準
- 表徵
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3367bbc6385cc21c8dbff3a88bed685616fb3f29
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "106974827"
---
# <a name="device-calibration-and-characterization-functions"></a>裝置校正和特性函數

下列函式適用于撰寫裝置校正，以及安裝和校準色彩顯示裝置（例如監視器和印表機）所需的特性工具。



| 函式 | 描述 |
|-|-|
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | 關閉開啟的設定檔控制碼。 |
| [**CreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | 使用指定的意圖，從一組色彩設定檔建立國際色彩協會 (ICC) *裝置連結設定檔* 。 |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | 從指定的色彩設定檔中指定的已標記設定檔元素，將資料複製到緩衝區。 |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | 在指定的國際色彩協會)  (的標記資料表中，抓取 *dwIndex* 所指定的標籤名稱，其中 *dwIndex* 是該資料表中以單一為基礎的索引。 |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| 針對開啟色彩設定檔的控制碼，抓取色彩設定檔內容。     |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | 從 ICC 色彩設定檔或 WCS XML 設定檔，抓取或衍生 ICC 標頭結構。 驅動程式和應用程式應該假設傳回 **TRUE** 只表示傳回的是正確結構化的標頭。 每個標記仍然需要使用舊版 ICM2 Api 或 XML 架構 Api 獨立進行驗證。 |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | 抓取指定色彩設定檔中的已標記元素數目。 |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | 從指定的 ICC 色彩設定檔抓取 PostScript 層級2色彩轉譯字典。 |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | 從 ICC 色彩設定檔抓取 PostScript 層級2色彩轉譯 [意圖](r.md) 。 |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | 從 ICC 色彩設定檔抓取 PostScript 層級 2 [色彩空間](c.md) 陣列。 |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | 報告指定的國際色彩協會 (ICC) 標記是否存在於指定的色彩設定檔中。 |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | 可讓您判斷指定的設定檔是否為有效的國際色彩協會 (ICC) 設定檔，或可用於色彩管理的有效 Windows 色彩系統 (WCS) 設定檔控制碼。 |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | 建立指定之色彩設定檔的控制碼。 然後，控制碼可用於其他設定檔管理功能。 |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | 設定 ICC 色彩設定檔中已標記之設定檔元素的元素資料。 |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | 在指定的 ICC 色彩設定檔中，建立參考與現有標記相同資料的新標記。 |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | 設定 ICC 色彩設定檔中標記專案的大小。 |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | 設定指定之 ICC 色彩設定檔中的標頭資料。 |
| [**WcsGetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | 決定是否啟用顯示校正狀態的系統管理。 |
| [**WcsSetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | 決定是否啟用顯示校正狀態的系統管理。 |



 

 

 




