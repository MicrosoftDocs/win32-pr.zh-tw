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
# <a name="commdatamodem"></a><span data-ttu-id="df866-103">通訊/datamodem</span><span class="sxs-lookup"><span data-stu-id="df866-103">comm/datamodem</span></span>

<span data-ttu-id="df866-104">Comm/datamodem 裝置類別包含 datamodem 裝置。</span><span class="sxs-lookup"><span data-stu-id="df866-104">The comm/datamodem device class consists of datamodem devices.</span></span> <span data-ttu-id="df866-105">您可以使用[檔案和](/windows/desktop/FileIO/file-management-functions)[通訊功能](/windows/desktop/DevIO/communications-functions)來存取這些裝置。</span><span class="sxs-lookup"><span data-stu-id="df866-105">You access these devices by using the [file](/windows/desktop/FileIO/file-management-functions) and [communications functions](/windows/desktop/DevIO/communications-functions).</span></span> <span data-ttu-id="df866-106">此類別中的裝置會與支援 LINEMEDIAMODE DATAMODEM 媒體類型的線路裝置相關聯 \_ ，該媒體類型是線上路裝置之 [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)結構的 **dwMediaModes** 成員中指定的。</span><span class="sxs-lookup"><span data-stu-id="df866-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_DATAMODEM media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="df866-107">[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構、將 **dwStringFormat** 設定為 STRINGFORMAT \_ 二進位值，並附加這些額外的成員：</span><span class="sxs-lookup"><span data-stu-id="df866-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to the STRINGFORMAT\_BINARY value and appending these additional members:</span></span>

``` syntax
HANDLE hComm;            // file handle to data modem
CHAR   szDeviceName[1];  // name of data modem
```

<span data-ttu-id="df866-108">**HComm** 成員是開啟通訊埠的控制碼。</span><span class="sxs-lookup"><span data-stu-id="df866-108">The **hComm** member is the handle of the open communications port.</span></span> <span data-ttu-id="df866-109">如果埠尚未開啟，或 [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)的 *dwSelect* 參數不是 LINECALLSELECT 呼叫值，則這個成員是 **Null** \_ 。</span><span class="sxs-lookup"><span data-stu-id="df866-109">This member is **NULL** if the port is not yet open or if the *dwSelect* parameter of [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) is not the LINECALLSELECT\_CALL value.</span></span> <span data-ttu-id="df866-110">如果是使用中的呼叫，服務提供者通常會開啟埠本身以直接控制通訊硬體，但只有線上路連接時才需要傳回有效的控制碼。</span><span class="sxs-lookup"><span data-stu-id="df866-110">If a call is active, the service provider typically opens the port itself to get direct control of the communications hardware, but is only required to return a valid handle if the line is connected.</span></span> <span data-ttu-id="df866-111">服務提供者會使用檔案旗標重迭值來開啟埠 \_ \_ ，然後使用 [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) 函式所指定的設定來設定埠。</span><span class="sxs-lookup"><span data-stu-id="df866-111">The service provider opens the port using the FILE\_FLAG\_OVERLAPPED value and then configures the port using the settings specified by the [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) function.</span></span> <span data-ttu-id="df866-112">您可以使用通訊功能搭配傳回的控制碼，來設定裝置的其他設定選項。</span><span class="sxs-lookup"><span data-stu-id="df866-112">You can set additional configuration options for the device by using communications functions with the returned handle.</span></span>

<span data-ttu-id="df866-113">**SzDeviceName** 成員是以 **null** 終止的字串，它會指定與線路、位址或呼叫相關聯的通訊埠名稱。</span><span class="sxs-lookup"><span data-stu-id="df866-113">The **szDeviceName** member is a **null**-terminated string that specifies the name of the communications port associated with the line, address, or call.</span></span>

<span data-ttu-id="df866-114">如果 **hComm** 是有效的控制碼，您可以在後續的檔案函數呼叫（例如 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 和 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)）中使用它來傳送和接收呼叫的資料。</span><span class="sxs-lookup"><span data-stu-id="df866-114">If **hComm** is a valid handle, you can use it in subsequent calls to file functions, such as [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) and [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), to send and receive data on the call.</span></span> <span data-ttu-id="df866-115">當您完成使用通訊埠，且最好在使用 [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) 函式來解除配置呼叫之前，您必須使用 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式來關閉埠。</span><span class="sxs-lookup"><span data-stu-id="df866-115">When you are finished using the communications port and preferably before you use the [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) function to deallocate the call, you must close the port by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="df866-116">使用 [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) 和 [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) 函式時，某些服務提供者需要此裝置類別的設定資料具有下列格式：</span><span class="sxs-lookup"><span data-stu-id="df866-116">When using the [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) and [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) functions, some service providers require that the configuration data for this device class have the following format:</span></span>

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

<span data-ttu-id="df866-117">以下是可搭配 [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) 和 [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) 功能使用的裝置設定資訊。</span><span class="sxs-lookup"><span data-stu-id="df866-117">The following is device configuration information for use with the [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) and [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) functions.</span></span>

<dl> <dt>

<span data-ttu-id="df866-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="df866-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="df866-119">**DEVCFGHDR** 結構的大小總和和 [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig)結構的實際大小。</span><span class="sxs-lookup"><span data-stu-id="df866-119">Sum of the size of the **DEVCFGHDR** structure and the actual size of the [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) structure.</span></span>

</dd> <dt>

<span data-ttu-id="df866-120"><span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="df866-120"><span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="df866-121">Unimodem **DevConfig** 結構的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="df866-121">Version number of the Unimodem **DevConfig** structure.</span></span> <span data-ttu-id="df866-122">這個成員可以是 MDMCFG \_ 版本 (0x00010003) 。</span><span class="sxs-lookup"><span data-stu-id="df866-122">This member can be MDMCFG\_VERSION (0x00010003).</span></span>

</dd> <dt>

<span data-ttu-id="df866-123"><span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**</span><span class="sxs-lookup"><span data-stu-id="df866-123"><span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**</span></span>
</dt> <dd>

<span data-ttu-id="df866-124">出現在 [Unimodem 選項] 頁面上的選項旗標。</span><span class="sxs-lookup"><span data-stu-id="df866-124">Option flags that appear on the Unimodem Option page.</span></span> <span data-ttu-id="df866-125">這個成員可以是下列值的組合：</span><span class="sxs-lookup"><span data-stu-id="df866-125">This member can be a combination of these values:</span></span>

<dl> <dt>

<span data-ttu-id="df866-126"><span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>終端機 \_ 前 (1) </span><span class="sxs-lookup"><span data-stu-id="df866-126"><span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>TERMINAL\_PRE (1)</span></span>
</dt> <dd>

<span data-ttu-id="df866-127">顯示前端子畫面。</span><span class="sxs-lookup"><span data-stu-id="df866-127">Displays the pre-terminal screen.</span></span>

</dd> <dt>

<span data-ttu-id="df866-128"><span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>終端機 \_ POST (2) </span><span class="sxs-lookup"><span data-stu-id="df866-128"><span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>TERMINAL\_POST (2)</span></span>
</dt> <dd>

<span data-ttu-id="df866-129">顯示終端機後畫面。</span><span class="sxs-lookup"><span data-stu-id="df866-129">Displays the post-terminal screen.</span></span>

</dd> <dt>

<span data-ttu-id="df866-130"><span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>手動 \_ 撥號 (4) </span><span class="sxs-lookup"><span data-stu-id="df866-130"><span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>MANUAL\_DIAL (4)</span></span>
</dt> <dd>

<span data-ttu-id="df866-131">如果能夠這麼做，請手動撥打電話。</span><span class="sxs-lookup"><span data-stu-id="df866-131">Dials the phone manually, if capable of doing so.</span></span>

</dd> <dt>

<span data-ttu-id="df866-132"><span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>啟動 \_ 燈光 (8) </span><span class="sxs-lookup"><span data-stu-id="df866-132"><span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>LAUNCH\_LIGHTS (8)</span></span>
</dt> <dd>

<span data-ttu-id="df866-133">在工作列的 [狀態] 區域中顯示數據機圖示。</span><span class="sxs-lookup"><span data-stu-id="df866-133">Displays the modem icon in the status area of the taskbar.</span></span>

<span data-ttu-id="df866-134">\_預設只會設定啟動燈值</span><span class="sxs-lookup"><span data-stu-id="df866-134">Only the LAUNCH\_LIGHTS value is set by default</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="df866-135"><span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**</span><span class="sxs-lookup"><span data-stu-id="df866-135"><span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**</span></span>
</dt> <dd>

<span data-ttu-id="df866-136">以兩秒的資料細微性 (的秒數) 來取代點數色調 ($) 。</span><span class="sxs-lookup"><span data-stu-id="df866-136">Number of seconds (in two seconds granularity) to replace the wait for credit tone ($).</span></span>

</dd> <dt>

<span data-ttu-id="df866-137"><span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**</span><span class="sxs-lookup"><span data-stu-id="df866-137"><span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**</span></span>
</dt> <dd>

<span data-ttu-id="df866-138">可搭配通訊和數據機設定功能使用的 [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig)結構。</span><span class="sxs-lookup"><span data-stu-id="df866-138">[**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) structure that can be used with the communications and modem configuration functions.</span></span>

</dd> </dl>

 

 
