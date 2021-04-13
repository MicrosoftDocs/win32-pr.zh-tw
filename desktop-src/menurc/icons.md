---
title: " (功能表和其他資源的圖示) "
description: 本節討論圖示，這些圖示是與遮罩結合的點陣圖影像，可在圖片中建立透明區域。
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\icons.htm
keywords:
- 資源，圖示
- 圖示，關於
- RT_ICON 資源
- RT_GROUP_ICON 資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c96e740c23bb61cfdaa6cfbcbf6d0ce7538586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383749"
---
# <a name="icons-menus-and-other-resources"></a> (功能表和其他資源的圖示) 

*圖示* 是由點陣圖影像所組成的圖片，可在圖片中建立透明區域。 字詞圖示可以參考下列其中一項：

-   單一圖示影像。 這是 **RT \_ 圖示** 類型的資源。
-   一組影像，系統或應用程式可以根據大小和色彩深度選擇最適當的圖示。 這是 **RT \_ 群組 \_ 圖示** 類型的資源。

### <a name="in-this-section"></a>本節內容



| Name                                 | 描述                                                 |
|--------------------------------------|-------------------------------------------------------------|
| [關於圖示](about-icons.md)       | 討論圖示。<br/>                                 |
| [使用圖示](using-icons.md)       | 討論如何執行與圖示相關的工作。<br/> |
| [圖示參考](icon-reference.md) | 包含 API 參考。<br/>                      |



 

### <a name="icon-functions"></a>圖示函式



| Name                                                               | 描述                                                                                                                                                                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CopyIcon**](/windows/desktop/api/Winuser/nf-winuser-copyicon)                                       | 將指定的圖示從另一個模組複製到目前的模組。 <br/>                                                                                                                                      |
| [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon)                                   | 建立具有指定大小、色彩和位模式的圖示。 <br/>                                                                                                                                    |
| [**CreateIconFromResource**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresource)           | 從描述圖示的資源位建立圖示或游標。<br/>                                                                                                                                          |
| [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex)       | 從描述圖示的資源位建立圖示或游標。 <br/>                                                                                                                                         |
| [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)                   | 從 [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) 結構建立圖示或游標。 <br/>                                                                                                                                 |
| [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)                                 | 終結圖示，並釋出圖示所佔用的任何記憶體。 <br/>                                                                                                                                                  |
| [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)                                       | 將圖示或游標繪製到指定的裝置內容中。<br/>                                                                                                                                                 |
| [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex)                                   | 將圖示或游標繪製到指定的裝置內容中、執行指定的點陣作業，並依指定的方式延展或壓縮圖示或游標。 <br/>                                     |
| [**DuplicateIcon**](/windows/desktop/api/Shellapi/nf-shellapi-duplicateicon)                             | 建立重複的指定圖示。<br/>                                                                                                                                                                   |
| [**ExtractAssociatedIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extractassociatedicona)             | 抓取在檔案中找到之索引圖示的控制碼，或在相關聯的可執行檔中找到的圖示。 <br/>                                                                                                  |
| [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona)                                 | 從指定的可執行檔、DLL 或圖示檔中，抓取圖示的控制碼。<br/>                                                                                                                        |
| [**ExtractIconEx**](/windows/desktop/api/Shellapi/nf-shellapi-extracticonexa)                             | 建立從指定的可執行檔、DLL 或圖示檔解壓縮之大型或小型圖示的控制碼陣列。 <br/>                                                                                      |
| [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo)                                 | 抓取指定之圖示或游標的相關資訊。 <br/>                                                                                                                                                 |
| [**GetIconInfoEx**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa)                             | 抓取指定之圖示或游標的相關資訊。 [**GetIconInfoEx**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa)會使用較新的 [**ICONINFOEX**](/windows/desktop/api/Winuser/ns-winuser-iconinfoexa)結構來擴充 [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) 。<br/> |
| [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona)                                       | 從與應用程式實例相關聯的可執行檔 ( .exe) 檔案載入指定的圖示資源。<br/>                                                                                                 |
| [**LookupIconIdFromDirectory**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectory)     | 搜尋圖示或游標資料，以取得最適合目前顯示裝置的圖示或游標。<br/>                                                                                                     |
| [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) | 搜尋圖示或游標資料，以取得最適合目前顯示裝置的圖示或游標。 <br/>                                                                                                    |
| [**PrivateExtractIcons**](/windows/desktop/api/Winuser/nf-winuser-privateextracticonsa)                 | 建立從指定檔案解壓縮之圖示的控制碼陣列。<br/>                                                                                                                             |



 

### <a name="icon-structures"></a>圖示結構



| Name                               | 描述                                                                                                                                                                                                                                     |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo)       | 包含圖示或游標的相關資訊。 <br/>                                                                                                                                                                                     |
| [**ICONINFOEX**](/windows/desktop/api/Winuser/ns-winuser-iconinfoexa)   | 包含圖示或游標的相關資訊。 擴充 [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo)。 由 [**GetIconInfoEx**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa)使用。<br/>                                                                                                |
| [**ICONMETRICS**](/windows/win32/api/winuser/ns-winuser-iconmetricsa) | 包含與圖示相關聯的可調整計量。 當指定 **SPI \_ GETICONMETRICS** 或 **spi \_ SETICONMETRICS** 動作時，此結構會與 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)函數搭配使用。<br/> |



 

 

