---
description: 本節說明與 MXDC ESCAPE 函式搭配使用的結構 \_ ，以及 MICROSOFT XPS 檔轉換器 (MXDC) 。
ms.assetid: 102dc056-7f65-47d4-8bcd-3b11608bdb9c
title: MXDC Escape 程式碼結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b87ef962be9f8fffa1ae0b2d126cecfda4cc157118f4defd21360b030dc9d30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948388"
---
# <a name="mxdc-escape-code-structures"></a>MXDC Escape 程式碼結構

本節說明與 [**MXDC \_ ESCAPE**](mxdc-escape.md) 函式搭配使用的結構，以及 Microsoft XPS 檔轉換器 (MXDC) 。

## <a name="in-this-section"></a>本節內容



| 結構                                                                              | 描述                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md)<br/>                         | [**MXDC \_ escape \_ HEADER \_ T**](/windows/desktop/printdocs/mxdcescapeheader)結構會保存使用 [**MXDC \_ ESCAPE**](mxdc-escape.md)作為 *nEscape* 參數之 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)呼叫的作業程式碼。 它也會提供輸入和輸出緩衝區的大小。<br/>  |
| [**MXDC \_ 取得 \_ 檔案名 \_ 資料 \_ T**](mxdcgetfilenamedata.md)<br/>                 | [**MXDC \_ 取得 \_ 檔案名 \_ 資料 \_ T**](/windows/desktop/printdocs/mxdcgetfilenamedata)結構會保存 Microsoft XPS 檔轉換器的完整路徑和檔案名， (MXDC) 輸出檔。<br/>                                                                                                     |
| [**MXDC \_ PRINTTICKET \_ ESCAPE \_ T**](mxdcprintticketescape.md)<br/>               | [**MXDC 的 \_ printticket \_ escape \_ t**](mxdcprintticketescape.md)結構是與 [**MXDC 的 \_ printticket \_ 資料 \_ t**](mxdcprintticketpassthrough.md)結構串連的 [**MXDC \_ ESCAPE \_ HEADER \_ t**](mxdcescapeheader.md)結構。<br/>                            |
| [**MXDC 的 \_ PRINTTICKET \_ 資料 \_ T**](mxdcprintticketpassthrough.md)<br/>            | [**MXDC 的 \_ PRINTTICKET \_ 資料 \_ T**](/windows/desktop/printdocs/mxdcprintticketpassthrough)結構會保存 XPS 檔列印票證，其中包含的印表機和列印工作設定，可傳遞給 MICROSOFT XPS 檔轉換器 (MXDC) 輸出檔，而不需要任何處理。<br/>              |
| [**MXDC \_ S0PAGE \_ 資料 \_ T**](mxdcs0pagedata.md)<br/>                             | [**MXDC \_ S0PAGE \_ DATA \_ T**](/windows/desktop/printdocs/mxdcs0pagedata)結構會保存 XPS 檔頁面，以傳遞至 MICROSOFT xps 檔轉換器 (MXDC) 輸出檔，而不需要任何處理。<br/>                                                                                  |
| [**MXDC \_ S0PAGE \_ 傳遞 \_ ESCAPE \_ T**](mxdcs0pagepassthroughescape.md)<br/> | [**MXDC \_ S0PAGE \_ 傳遞 \_ escape \_ t**](/windows/desktop/printdocs/mxdcs0pagepassthroughescape)結構是與 [**MXDC \_ S0PAGE \_ 資料 \_ T**](mxdcs0pagedata.md)結構串連的 [**MXDC \_ ESCAPE \_ HEADER \_ t**](mxdcescapeheader.md)結構。<br/>                             |
| [**MXDC \_ S0PAGE \_ 資源 \_ ESCAPE \_ T**](mxdcs0pageresourceescape.md)<br/>       | [**MXDC \_ S0PAGE \_ 資源 \_ ESCAPE \_ t**](/windows/desktop/printdocs/mxdcs0pageresourceescape)結構是與 [**MXDC \_ XPS \_ S0PAGE \_ 資源 \_ t**](mxdcxpss0pageresource.md)結構串連的 [**MXDC \_ ESCAPE \_ HEADER \_ t**](mxdcescapeheader.md)結構。<br/>                   |
| [**MXDC \_ XPS \_ S0PAGE \_ 資源 \_ T**](mxdcxpss0pageresource.md)<br/>             | [**MXDC \_ XPS \_ S0PAGE \_ 資源 \_ T**](/windows/desktop/printdocs/mxdcxpss0pageresource)結構會保存與 XPS 檔頁面相關聯的資源（例如影像或字型）相關資訊，並將其傳遞至 Microsoft xps 檔轉換器 (MXDC) 輸出檔。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**MXDC \_ ESCAPE**](mxdc-escape.md)
</dt> </dl>

 

