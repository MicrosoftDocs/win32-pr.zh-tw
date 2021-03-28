---
description: 當遇到錯誤時，字型內嵌函式會傳回下列 LONG 值。 當函式成功時， \_ 會傳回值 E NONE。
ms.assetid: 71effafe-55a9-40ed-81c7-07278eba32d3
title: Font-Embedding 函數錯誤訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a4bf348d73e6b452ba9afe819e3fa515ebd04c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191943"
---
# <a name="font-embedding-function-error-messages"></a>Font-Embedding 函數錯誤訊息

當遇到錯誤時，字型內嵌函式會傳回下列 LONG 值。 當函式成功時， \_ 會傳回值 E NONE。



| 傳回值                  | 描述                                                                                                                                                                                                                                                                              |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 電子 \_ 無                       | 沒有錯誤。                                                                                                                                                                                                                                                                                |
| E \_ ADDFONTFAILED              | 當 load 函式嘗試使用 [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)新增新字型時發生錯誤。                                                                                                                                                                    |
| E \_ CHARCODECOUNTINVALID       | 在 [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont) 中指定的子集字元計數無效。                                                                                                                                                                                            |
| E \_ CHARCODESETINVALID         | [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont)中指定的字元集無效。                                                                                                                                                                                                            |
| E \_ COULDNTCREATETEMPFILE      | 載入函數無法在中建立所需的暫存檔案，以安裝新的字型或資源檔。                                                                                                                                                                                   |
| E \_ DEVICETRUETYPEFONT         | 指定的 TrueType®字型不是系統字型。 字型可能會以裝置字型的形式存在於印表機中。                                                                                                                                                                                     |
| E \_ ERRORACCESSINGEXCLUDELIST  | 嘗試存取字樣排除清單時發生錯誤。                                                                                                                                                                                                                |
| E \_ ERRORACCESSINGFACENAME     | 嘗試配置 [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) 結構時，發生非 DC 相關的錯誤。                                                                                                                                                             |
| E \_ ERRORACCESSINGFONTDATA     | 嘗試使用 [**GetFontData**](/windows/desktop/api/Wingdi/nf-wingdi-getfontdata)時發現錯誤。                                                                                                                                                                                                     |
| E \_ ERRORCOMPRESSINGFONTDATA   | [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont)嘗試壓縮字型資料時發生錯誤。                                                                                                                                                                                          |
| E \_ ERRORCONVERTINGCHARS       | 發生錯誤，無法將單一位元組字元字串轉換成 Unicode 字元。 如果 *pucCharCodes* 或 *pusShortCodes* 為非 null 值，或在使用 MultiByteToWideChar 時轉換失敗， [**TTCharToUnicode**](/windows/desktop/api/T2embapi/nf-t2embapi-ttchartounicode)可能會發生這種情況。 |
| E \_ ERRORCREATINGFONTFILE      | 嘗試建立字型檔案時發生錯誤。                                                                                                                                                                                                                              |
| E \_ ERRORDECOMPRESSINGFONTDATA | 嘗試解壓縮字型檔中的資料時發生錯誤。                                                                                                                                                                                                                        |
| E \_ ERROREXPANDINGFONTDATA     | 載入函式嘗試擴充內嵌的壓縮字型資料時發生錯誤。                                                                                                                                                                                           |
| E \_ ERRORGETTINGDC             | 嘗試配置 DC 時發生錯誤，正在停止處理。                                                                                                                                                                                                                     |
| E \_ ERRORREADINGFONTDATA       | 嘗試讀取字型資料時發生錯誤。                                                                                                                                                                                                                                    |
| E \_ ERRORUNICODECONVERSION     | 配置記憶體以將名稱字串轉換成 Unicode 時發生錯誤。                                                                                                                                                                                                           |
| E \_ ERRORUSINGTEMPFILE         | 載入函式使用暫存檔案來安裝新的字型檔案或資源檔時發生錯誤。                                                                                                                                                                      |
| E \_ 例外狀況                  | 未知的原因擲回例外狀況。                                                                                                                                                                                                                                             |
| E \_ FACENAMEINVALID            | 已將 null *szFaceName* 參數傳遞給函數。                                                                                                                                                                                                                                |
| E \_ FLAGSINVALID               | 目前函數中的 *ulFlags* 參數無效。                                                                                                                                                                                                                              |
| E \_ FONTALREADYEXISTS          | 內嵌字型的名稱和總和檢查碼與系統上已安裝的字型相同。                                                                                                                                                                                              |
| E \_ FONTDATAINVALID            | 從磁片讀取的字型資料不是有效的內嵌字型結構。                                                                                                                                                                                                                         |
| E \_ FONTFILECREATEFAILED       | 載入函數無法 ( 建立字型檔案)                                                                                                                                                                                                                                  |
| E \_ FONTFILENOTFOUND           | 指定之檔案名的字型檔案不存在。                                                                                                                                                                                                                                 |
| E \_ FONTINSTALLFAILED          | 嘗試在系統中安裝內嵌的字型失敗。                                                                                                                                                                                                                            |
| E \_ FONTNAMEALREADYEXISTS      | 內嵌字型具有相同的名稱，但已安裝的字型具有不同的總和檢查碼。                                                                                                                                                                                                |
| E \_ FONTNOTEMBEDDABLE          | 由於字型製造商的限制，無法內嵌指定的字型。 在檔中嵌入此字型違反著作權法。                                                                                                                                         |
| E \_ FONTREFERENCEINVALID       | 已將 null *phFontReference* 傳遞給函數。                                                                                                                                                                                                                                     |
| E \_ HDCINVALID                 | 為 [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont) 函數指定的裝置內容無效。                                                                                                                                                                                             |
| E \_ NAMECHANGEFAILED           | [**TTLoadEmbeddedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttloadembeddedfont) 無法變更所載入字型的名稱。                                                                                                                                                                                 |
| E \_ NOFREEMEMORY               | 嘗試配置記憶體時發生內部操作失敗。                                                                                                                                                                                                                        |
| E \_ NOOS2                      | 在字型中找不到 OS/2 資料表。                                                                                                                                                                                                                                                 |
| E \_ NOTATRUETYPEFONT           | 指定的字型不是 TrueType 字型。                                                                                                                                                                                                                                               |
| E \_ PBENABLEDINVALID           | 已將 null *pbEnabled* 參數傳遞給函數。                                                                                                                                                                                                                                 |
| E \_ PERMISSIONSINVALID         | 已將 null *pulPermissions* 參數傳遞給函數。                                                                                                                                                                                                                            |
| E \_ PRIVSINVALID               | 載入函數中指定的 *ulPrivs* 參數無效。                                                                                                                                                                                                                      |
| E \_ PRIVSTATUSINVALID          | 已將 null *pulPrivStatus* 參數傳遞給函數。                                                                                                                                                                                                                             |
| E \_ READFROMSTREAMFAILED       | 嘗試從資料流程讀取內嵌字型結構時發生錯誤。                                                                                                                                                                                                  |
| E \_ RESOURCEFILECREATEFAILED   | 載入函數無法 ( 受) 建立字型資源檔。                                                                                                                                                                                                                       |
| E \_ SAVETOSTREAMFAILED         | 嘗試將內嵌字型結構儲存至資料流程時發生錯誤。                                                                                                                                                                                                      |
| E \_ STATUSINVALID              | 已將 null *pulStatus* 參數傳遞給函數。                                                                                                                                                                                                                                 |
| E \_ STREAMINVALID              | [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont)或 load 函數中指定的資料流程無效。                                                                                                                                                                                             |
| E \_ SUBSETTINGFAILED           | 嘗試建立字型的子集時， [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont)失敗。                                                                                                                                                                                                 |
| E \_ T2NOFREEMEMORY             | 嘗試釋放記憶體時發生錯誤。 在免費操作期間，有問題的記憶體失敗。                                                                                                                                                                              |
| E \_ WINDOWSAPI                 | 其中一個稱為 Windows API 的函式（例如 [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) 或 [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa)）時發生內部錯誤。                                                                                                   |
| E \_ API \_ >NOTIMPL               | 此 API 函式不會在其執行所在的 Windows 版本中執行。                                                                                                                                                                                                   |



 

 

 



