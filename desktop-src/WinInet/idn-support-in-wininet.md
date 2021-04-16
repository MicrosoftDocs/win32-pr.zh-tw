---
title: WinINet 中的 IDN 支援
description: 從 Windows Server 2008 和 Windows Vista 開始，Unicode URL 的主機部分會轉換成國際化功能變數名稱 (IDN) 。
ms.assetid: 7c56908e-f6d0-48dc-9ac1-73f888fb7b6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510b1bc8d2ab77534d7f5dac587f287d5e7095af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382590"
---
# <a name="idn-support-in-wininet"></a>WinINet 中的 IDN 支援

從 Windows Server 2008 和 Windows Vista 開始，Unicode URL 的主機部分會轉換成國際化功能變數名稱 (IDN) 。 個別的 Unicode URL 編碼部分也可以由應用程式設定的設定修改。 ANSI 版本的 WinINet API 會繼續透過網路傳送 URL，如同應用程式所輸入的一樣，不過，WinINet Unicode 版本的 API 現在符合 IDN 標準 (RFC3490) 進行 URL 編碼。

根據預設，當輸入 URL 作為 Unicode 參數時，會將 proxy 和直接連接的主機部分轉換成 IDN 格式。 應用程式可透過設定 **網際網路 \_ 選項 \_ IDN** 選項，選擇停用 IDN 主機格式。 您可以使用 **網際網路 \_ 旗標 \_ Idn \_ direct** 或 **網際網路 \_ 旗標 \_ idn \_ proxy** 旗標搭配 **網際網路 \_ 選項 \_ idn**，僅在直接或 proxy 連接上啟用 idn 主機轉換。

下列程式碼範例示範如何停用 proxy 和直接連接的 IDN 主機轉換。

``` syntax
DWORD IDN = 0; 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_IDN,
                   &IDN, 
                   sizeof(DWORD) ); 
```

如果已停用 IDN 主機格式，則應用程式可以選擇使用 **網際網路 \_ 選項 \_ 字碼頁** 來指定所需的字碼頁。

下列程式碼範例顯示如何指定日文字碼頁。

``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS, 
                   Sizeof(DWORD) ); 
```

URL 的路徑部分預設為 UTF8 編碼，而 URL 的其餘區段（查詢或片段）會轉換成預設的系統字碼頁 (CP \_ ACP) 。

下列範例示範如何指定 URL 路徑部分的韓文語言字碼頁。

``` syntax
DWORD CP_KOREAN = 949;   // ANSI/OEM Korean 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE_PATH,
                   &CP_KOREAN, 
                   sizeof(DWORD) );
```

下表定義支援 IDN 的選項。 如需詳細資訊，請參閱 [選項旗標](option-flags.md) 主題。



| 選項                            | Description                                                                                                                                                                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 網際網路 \_ 選項 \_ 字碼頁        | 此選項設定于要求或連接控制碼上，以指定 URL 之主機部分的字碼頁編碼配置。 如果已啟用 IDN，則會忽略此選項。                                                      |
| 網際網路 \_ 選項 \_ 字碼頁 \_ 路徑  | 此選項會在要求上設定，或連接控制碼會對 URL 的路徑部分啟用指定的編碼配置。 根據預設，URL 的路徑部分為 UTF8 編碼。                                         |
| 網際網路 \_ 選項 \_ 字碼頁 \_ 額外 | 在要求上設定此選項，或連接控制碼，可針對 URL 的額外部分啟用指定的編碼配置。 根據預設，會在預設的系統字碼頁中，將 URL 的額外部分編碼 (CP \_ ACP) 。 |
| 網際網路 \_ 選項 \_ IDN             | 此選項可用於要求或連接控制碼，以啟用或停用 IDN 主機轉換。 當 IDN 停用時，WinINet 會使用預設的系統字碼頁來編碼 URL 的主機或授權單位部分。       |



 

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 