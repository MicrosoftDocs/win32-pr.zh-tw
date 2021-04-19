---
description: Comm/datamodem 裝置類別包含 datamodem 裝置。
ms.assetid: 6bc314c6-30ec-4318-856a-3ab2fa6aadfb
title: 通訊/datamodem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89210bcf14931e3905f71cdbb8678f5519cc4c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996610"
---
# <a name="commdatamodem"></a>通訊/datamodem

Comm/datamodem 裝置類別包含 datamodem 裝置。 您可以使用[檔案和](/windows/desktop/FileIO/file-management-functions)[通訊功能](/windows/desktop/DevIO/communications-functions)來存取這些裝置。 此類別中的裝置會與支援 LINEMEDIAMODE DATAMODEM 媒體類型的線路裝置相關聯 \_ ，該媒體類型是線上路裝置之 [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)結構的 **dwMediaModes** 成員中指定的。

[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構、將 **dwStringFormat** 設定為 STRINGFORMAT \_ 二進位值，並附加這些額外的成員：

``` syntax
HANDLE hComm;            // file handle to data modem
CHAR   szDeviceName[1];  // name of data modem
```

**HComm** 成員是開啟通訊埠的控制碼。 如果埠尚未開啟，或 [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)的 *dwSelect* 參數不是 LINECALLSELECT 呼叫值，則這個成員是 **Null** \_ 。 如果是使用中的呼叫，服務提供者通常會開啟埠本身以直接控制通訊硬體，但只有線上路連接時才需要傳回有效的控制碼。 服務提供者會使用檔案旗標重迭值來開啟埠 \_ \_ ，然後使用 [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) 函式所指定的設定來設定埠。 您可以使用通訊功能搭配傳回的控制碼，來設定裝置的其他設定選項。

**SzDeviceName** 成員是以 **null** 終止的字串，它會指定與線路、位址或呼叫相關聯的通訊埠名稱。

如果 **hComm** 是有效的控制碼，您可以在後續的檔案函數呼叫（例如 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 和 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)）中使用它來傳送和接收呼叫的資料。 當您完成使用通訊埠，且最好在使用 [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) 函式來解除配置呼叫之前，您必須使用 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式來關閉埠。

使用 [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) 和 [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) 函式時，某些服務提供者需要此裝置類別的設定資料具有下列格式：

``` syntax
typedef struct  tagDEVCFG  {
  DEVCFGHDR   dfgHdr;
  COMMCONFIG  commconfig;
} DEVCFG, *PDEVCFG, FAR* LPDEVCFG;

// Device setting information
typedef struct  tagDEVCFGDR  {
  DWORD       dwSize;
  DWORD       dwVersion;
  WORD        fwOptions;
  WORD        wWaitBong;
} DEVCFGHDR;
```

以下是可搭配 [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) 和 [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) 功能使用的裝置設定資訊。

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

**DEVCFGHDR** 結構的大小總和和 [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig)結構的實際大小。

</dd> <dt>

<span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**
</dt> <dd>

Unimodem **DevConfig** 結構的版本號碼。 這個成員可以是 MDMCFG \_ 版本 (0x00010003) 。

</dd> <dt>

<span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**
</dt> <dd>

出現在 [Unimodem 選項] 頁面上的選項旗標。 這個成員可以是下列值的組合：

<dl> <dt>

<span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>終端機 \_ 前 (1) 
</dt> <dd>

顯示前端子畫面。

</dd> <dt>

<span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>終端機 \_ POST (2) 
</dt> <dd>

顯示終端機後畫面。

</dd> <dt>

<span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>手動 \_ 撥號 (4) 
</dt> <dd>

如果能夠這麼做，請手動撥打電話。

</dd> <dt>

<span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>啟動 \_ 燈光 (8) 
</dt> <dd>

在工作列的 [狀態] 區域中顯示數據機圖示。

\_預設只會設定啟動燈值

</dd> </dl> </dd> <dt>

<span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**
</dt> <dd>

以兩秒的資料細微性 (的秒數) 來取代點數色調 ($) 。

</dd> <dt>

<span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**
</dt> <dd>

可搭配通訊和數據機設定功能使用的 [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig)結構。

</dd> </dl>

 

 
