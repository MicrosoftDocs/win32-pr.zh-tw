---
title: 使用 Windows 標頭
description: 使用 Windows 標頭檔來建立使用 Windows API 的應用程式。
ms.assetid: a4def563-8ddc-4630-ae8a-86c07cf98374
keywords:
- WindowsAPI，標頭檔
- C2065
- WINVER
- _WIN32_WINDOWS
- _WIN32_WINNT
- _WIN32_IE
- WIN32_LEAN_AND_MEAN
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: 886c5601683cc03fb2486f8be3b69f31c4619b721276babbc2c3e31e28c0a022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643588"
---
# <a name="using-the-windows-headers"></a>使用 Windows 標頭

Windows API 的標頭檔可讓您建立32和64位應用程式。 它們包含 Unicode 和 ANSI API 版本的宣告。 如需詳細資訊，請參閱[Windows API 中的 Unicode](/windows/desktop/Intl/unicode-in-the-windows-api)。 它們使用的 [資料類型](windows-data-types.md) 可讓您從單一原始程式碼基底建立32和64位版本的應用程式。 如需詳細資訊，請參閱[準備開始64位 Windows](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows)。 其他功能包括 [標頭注釋](header-annotations.md) 和 [嚴格的類型檢查](strict-type-checking.md)。

-   [Visual C++ 和 Windows 標頭檔](#visual-c-and-the-windows-header-files)
-   [條件式宣告的宏](#macros-for-conditional-declarations)
-   [設定 WINVER 或 \_ WIN32 \_ WINNT](#setting-winver-or-_win32_winnt)
-   [控制結構封裝](#controlling-structure-packing)
-   [更快速的組建，包含較小的標頭檔](#faster-builds-with-smaller-header-files)
-   [相關主題](#related-topics)

## <a name="visual-c-and-the-windows-header-files"></a>Visual C++ 和 Windows 標頭檔

Microsoft Visual C++ 包含 Visual C++ 發行時目前的 Windows 標頭檔的複本。 因此，如果您從 SDK 安裝更新的標頭檔，您的電腦上可能會有多個版本的 Windows 標頭檔。 如果您不確定您使用的是最新版的 SDK 標頭檔，當您在編譯使用 Visual C++ 發行之後引進之功能的程式碼時，將會收到下列錯誤碼：錯誤 C2065：未宣告的識別碼。

## <a name="macros-for-conditional-declarations"></a>條件式宣告的宏

某些相依于特定 Windows 版本的函式是使用條件式程式碼宣告的。 這可讓您使用編譯器來偵測應用程式是否使用其目標版本 (s) Windows 不支援的函數。 若要編譯使用這些函數的應用程式，您必須定義適當的宏。 否則，您會收到 C2065 錯誤訊息。

Windows 標頭檔會使用宏來指出哪些版本的 Windows 支援許多程式設計項目。 因此，您必須定義這些宏，以使用每個主要作業系統版本引進的新功能。  (個別的標頭檔可能會使用不同的宏;因此，如果發生編譯問題，請檢查包含條件式定義定義的標頭檔。 ) 如需詳細資訊，請參閱 Sdkddkver.h。

下表說明 Windows 標頭檔中使用的慣用宏。 如果您定義 NTDDI \_ 版本，您也必須定義 \_ WIN32 \_ WINNT。



| 需要的最低系統                       | NTDDI 版本的值 \_            |
|-----------------------------------------------|-------------------------------------|
| Windows 10 1903 "19H1"                        | **NTDDI \_WIN10 \_ 19H1** (0x0A000007)  |
| Windows 10 1809 "Redstone 5"                  | **NTDDI \_WIN10 \_ RS5** (0x0A000006)   |
| Windows 10 1803 "Redstone 4"                  | **NTDDI \_WIN10 \_ RS4** (0x0A000005)   |
| Windows 10 1709 "Redstone 3"                  | **NTDDI \_WIN10 \_ RS3** (0x0A000004)   |
| Windows 10 1703 "Redstone 2"                  | **NTDDI \_WIN10 \_ RS2** (0x0A000003)   |
| Windows 10 1607 "Redstone 1"                  | **NTDDI \_WIN10 \_ RS1** (0x0A000002)   |
| Windows 10 1511 "閾值 2"                 | **NTDDI \_WIN10 \_ TH2** (0x0A000001)   |
| Windows 10 1507 「閾值」                   | **NTDDI \_WIN10** (0x0A000000)        |
| Windows 8.1                                   | **NTDDI \_WINBLUE** (0x06030000)      |
| Windows 8                                     | **NTDDI \_WIN8** (0x06020000)         |
| Windows 7                                     | **NTDDI \_WIN7** (0x06010000)         |
| Windows Server 2008                           | **NTDDI \_WS08** (0x06000100)         |
| Windows Vista 包含 Service Pack 1 (SP1)       | **NTDDI \_VISTASP1** (0x06000100)     |
| Windows Vista                                 | **NTDDI \_VISTA** (0x06000000)        |
| Windows Server 2003 Service Pack 2 (SP2) | **NTDDI \_WS03SP2** (0x05020200)      |
| Windows Server 2003 含 Service Pack 1 (SP1) | **NTDDI \_WS03SP1** (0x05020100)      |
| Windows Server 2003                           | **NTDDI \_WS03** (0x05020000)         |
| Windows XP (含 Service Pack 3，SP3)          | **NTDDI \_WINXPSP3** (0x05010300)     |
| Windows XP with Service Pack 2 (SP2)          | **NTDDI \_WINXPSP2** (0x05010200)     |
| WindowsXP Service Pack 1 (SP1)           | **NTDDI \_WINXPSP1** (0x05010100)     |
| Windows XP                                    | **NTDDI \_>TEST-WINXP** (0x05010000)        |



 

下表說明 Windows 標頭檔中使用的其他宏。



| 需要的最低系統                           | \_WIN32 \_ WINNT 和 WINVER 的最小值 |
|---------------------------------------------------|---------------------------------------------|
| Windows 10                                        | **\_ WIN32 \_ WINNT \_ WIN10** (0x0A00)           |
| Windows 8.1                                       | **\_ WIN32 \_ WINNT \_ WINBLUE** (0x0603)         |
| Windows 8                                         | **\_ WIN32 \_ WINNT \_ WIN8** (0x0602)            |
| Windows 7                                         | **\_ WIN32 \_ WINNT \_ WIN7** (0x0601)            |
| Windows Server 2008                               | **\_ WIN32 \_ WINNT \_ WS08** (0x0600)            |
| Windows Vista                                     | **\_ WIN32 \_ WINNT \_ VISTA** (0x0600)           |
| WindowsServer 2003 SP1、Windows XP SP2 | **\_ WIN32 \_ WINNT \_ WS03** (0x0502)            |
| WindowsServer 2003、Windows XP                   | **\_ WIN32 \_ WINNT \_ >test-winxp** (0x0501)           |



 



| 需要的最低版本          | \_WIN32 IE 的最小值 \_      |
|-----------------------------------|-----------------------------------|
| Internet Explorer 11。0            | **\_ WIN32 \_ IE \_ IE110** (0x0A00)    |
| Internet Explorer 10。0            | **\_ WIN32 \_ IE \_ IE100** (0x0A00)    |
| Internet Explorer 9.0             | **\_ WIN32 \_ IE \_ IE90** (0x0900)     |
| Internet Explorer 8.0             | **\_ WIN32 \_ IE \_ IE80** (0x0800)     |
| Internet Explorer 7.0             | **\_ WIN32 \_ IE \_ IE70** (0x0700)     |
| Internet Explorer 6.0 SP2         | **\_ WIN32 \_ IE \_ IE60SP2** (0x0603)  |
| Internet Explorer 6.0 SP1         | **\_ WIN32 \_ IE \_ IE60SP1** (0x0601)  |
| Internet Explorer 6.0             | **\_ WIN32 \_ IE \_ IE60** (0x0600)     |
| Internet Explorer 5.5             | **\_ WIN32 \_ IE \_ IE55** (0x0550)     |
| Internet Explorer 5.01            | **\_ WIN32 \_ IE \_ IE501** (0x0501)    |
| Internet Explorer 5.0、5.0 a、5.0 b | **\_ WIN32 \_ IE \_ IE50** (0x0500)     |



 

## <a name="setting-winver-or-_win32_winnt"></a>設定 WINVER 或 \_ WIN32 \_ WINNT

您可以使用每個原始程式檔中的 define 語句來定義這些符號 \# ，或是指定 Visual C++ 所支援的/d 編譯器選項來定義這些符號。

例如，若要在原始程式檔中設定 WINVER，請使用下列語句：

`#define WINVER 0x0502`

若要 \_ \_ 在原始程式檔中設定 WIN32 WINNT，請使用下列語句：

`#define _WIN32_WINNT 0x0502`

若要 \_ \_ 使用/d 編譯器選項設定 WIN32 WINNT，請使用下列命令：

**cl-c/d \_WIN32 \_ WINNT = 0x0502** _source_**.cpp**

如需使用/D 編譯器選項的詳細資訊，請參閱 [/d (預處理器定義) ](/cpp/build/reference/d-preprocessor-definitions)。

請注意，最新版本的 Windows 引進的某些功能可能會新增至舊版 Windows 的 service pack 中。 因此，若要以 service pack 為目標，您可能需要 \_ \_ 使用下一個主要作業系統版本的值來定義 WIN32 WINNT。 例如， [**GetDllDirectory**](/windows/desktop/api/winbase/nf-winbase-getdlldirectorya)函式是在 Windows Server 2003 中引進，如果 \_ WIN32 \_ WINNT 0x0502 或更大，則會有條件地定義。 此函式也已加入至 Windows XP SP1。 因此，如果您要將 \_ WIN32 \_ WINNT 定義為 Windows xp 的目標0x0501，您會錯過 Windows XP SP1 中定義的功能。

## <a name="controlling-structure-packing"></a>控制結構封裝

專案應該編譯為使用預設結構封裝（目前為8個位元組，因為最大整數類型是8個位元組）。 這麼做可確保標頭檔中的所有結構類型都會編譯到應用程式中，且 Windows API 所預期的對齊方式相同。 它也可確保具有8位元組值的結構正確對齊，且不會在強制執行資料對齊的處理器上造成對齊錯誤。

如需詳細資訊，請參閱 [/Zp (結構成員對齊) ](/cpp/build/reference/zp-struct-member-alignment) 或 [套件](/cpp/preprocessor/pack)。

## <a name="faster-builds-with-smaller-header-files"></a>更快速的組建，包含較小的標頭檔

您可以排除一些較不常用的 API 宣告，以減少 Windows 標頭檔的大小，如下所示：

-   定義 WIN32 的 \_ 精簡 \_ 和 MEAN， \_ 以排除 api，例如加密、DDE、RPC、Shell 和 Windows 通訊端。

    `#define WIN32_LEAN_AND_MEAN`

-   定義一個或多個不包含 api 的 *api* 符號。 例如，NOCOMM 會排除序列通訊 API。 如需不支援 *api* 符號的清單，請參閱 Windows .h。

    `#define NOCOMM`

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WindowsSDK 下載網站](https://msdn.microsoft.com/windowsserver/bb980924.aspx)
</dt> </dl>

 

 