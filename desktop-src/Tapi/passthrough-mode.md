---
description: 當呼叫在 LINEBEARERMODE 傳遞中為作用中時 \_ ，服務提供者可讓應用程式直接存取附加的硬體來控制。
ms.assetid: 75e31241-c782-4d50-9590-cf68c0505add
title: 傳遞模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 985e1caf666fcb3278bacf5c5cfe9d8a4e847dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991835"
---
# <a name="passthrough-mode"></a><span data-ttu-id="c9e8c-103">傳遞模式</span><span class="sxs-lookup"><span data-stu-id="c9e8c-103">Passthrough Mode</span></span>

<span data-ttu-id="c9e8c-104">當呼叫在 **LINEBEARERMODE \_ 傳遞** 中為作用中時，服務提供者可讓應用程式直接存取附加的硬體來控制。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-104">When a call is active in **LINEBEARERMODE\_PASSTHROUGH**, the service provider gives direct access to the attached hardware for control by the application.</span></span> <span data-ttu-id="c9e8c-105">應用程式可以使用此模式，透過 [通訊功能](/windows/desktop/DevIO/communications-functions)存取非同步數據機，以設定或使用服務提供者不支援的特殊功能，例如 (類別1、2等) 的傳真。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-105">Applications can use this mode for temporary direct control over asynchronous modems, accessed through the [communications functions](/windows/desktop/DevIO/communications-functions), for the purpose of configuring or using special features not otherwise supported by the service provider, such as facsimile (Class 1, 2, and so on).</span></span> <span data-ttu-id="c9e8c-106">通用數據機驅動程式 (UNIMODEM) 服務提供者支援此持有人模式。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-106">This bearer mode is supported by the Universal Modem Driver (UNIMODEM) service provider.</span></span>

<span data-ttu-id="c9e8c-107">支援 **LINEBEARERMODE \_ 傳遞** 的服務提供者會在 [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)結構的 **dwBearerModes** 成員中指出該服務提供者。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-107">Service providers that support **LINEBEARERMODE\_PASSTHROUGH** indicate it in the **dwBearerModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure.</span></span> <span data-ttu-id="c9e8c-108">指出 **LINEBEARERMODE \_ 傳遞** 時，Unimodem 服務提供者也會包含在 **LINEDEVCAPS** 結構的 **DevSpecific** 區域中，此登錄機碼會用來存取與線路裝置相關聯之數據機的資料，格式如下：</span><span class="sxs-lookup"><span data-stu-id="c9e8c-108">When **LINEBEARERMODE\_PASSTHROUGH** is indicated, the Unimodem service provider will also include in the **DevSpecific** area of the **LINEDEVCAPS** structure the registry key used to access data about the modem associated with the line device, in the following format:</span></span>

``` syntax
struct {
    DWORD dwContents;   // Set to 1 (indicates containing key).
    DWORD dwKeyOffset;  // Offset to key from start of this
                        // structure (not from start of
                        // LINEDEVCAPS structure).
                        // 8 in this case. 
    BYTE rgby[...];     // Place that contains null-terminated
                        // registry key. 
}
```

<span data-ttu-id="c9e8c-109">例如：</span><span class="sxs-lookup"><span data-stu-id="c9e8c-109">For example:</span></span>

``` syntax
    00000001 00000008 74737953 435c6d65  ........System\C
    65727275 6f43746e 6f72746e 7465536c  urrentControlSet
    7265535c 65636976 6c435c73 5c737361  urrentControlSet
    65646f4d 30305c6d xx003030 xxxxxxxx  Modem\0000.
```

<span data-ttu-id="c9e8c-110">然後可以使用 [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) 函式來開啟此登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-110">This registry key could then be opened using the [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) function.</span></span>

<span data-ttu-id="c9e8c-111">使用 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)函數最常叫用傳遞模式，方法是在 *lpCallParams* 參數所指向之 [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)結構的 **dwBearerMode** 成員中設定 **LINEBEARERMODE \_ 傳遞** 位。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-111">Passthrough mode is invoked most often using the [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) function, by setting the **LINEBEARERMODE\_PASSTHROUGH** bit in the **dwBearerMode** member of the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure pointed to by the *lpCallParams* parameter.</span></span> <span data-ttu-id="c9e8c-112">當此動作完成時，服務提供者會開啟數據機的序列埠，並立即將呼叫放入 **\_ 連接的 LINECALLSTATE**。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-112">When this is done, the service provider opens the serial port to the modem and immediately place the call into **LINECALLSTATE\_CONNECTED**.</span></span> <span data-ttu-id="c9e8c-113">然後，應用程式可以使用 [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) 函式搭配裝置類別 "comm/datamodem" 來取得開啟的檔案控制代碼，以讀取和寫入至通訊埠。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-113">The application can then use the [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function with the device class "comm/datamodem" to obtain an open file handle to read from and write to the comm port.</span></span>

<span data-ttu-id="c9e8c-114">也可以叫用傳遞模式，以回應傳入的呼叫。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-114">Passthrough mode can be invoked in response to an incoming call as well.</span></span> <span data-ttu-id="c9e8c-115">一般而言，應用程式會在呼叫于 LINECALLSTATE 供應專案中 **叫 \_** 用傳遞模式，然後才會呼叫接聽。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-115">Generally, applications will invoke passthrough mode while the call is in **LINECALLSTATE\_OFFERING**, before the call has been answered.</span></span> <span data-ttu-id="c9e8c-116">應用程式不會呼叫 [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)，而是會呼叫 [**LineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams)，將 **LINEBEARERMODE \_** 傳遞當作 *dwBearerMode* 參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-116">Instead of calling [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer), the application calls [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams), passing **LINEBEARERMODE\_PASSTHROUGH** as the *dwBearerMode* parameter.</span></span> <span data-ttu-id="c9e8c-117">完成這項操作時，如同 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)，呼叫會立即置於服務提供者所 **\_ 連接的 LINECALLSTATE** 中，應用程式可以使用 [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)取得開啟埠的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-117">When this is done, as with [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), the call is immediately placed into **LINECALLSTATE\_CONNECTED** by the service provider, and the application can obtain a handle to the open port using [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).</span></span> <span data-ttu-id="c9e8c-118">當呼叫位於 LINECALLSTATE 供應專案、 **LINECALLSTATE \_ 接受** 或 **LINECALLSTATE \_ 連線** 時，可以呼叫 **lineSetCallParams** 函數。 **\_**</span><span class="sxs-lookup"><span data-stu-id="c9e8c-118">The **lineSetCallParams** function can be called when the call is in **LINECALLSTATE\_OFFERING**, **LINECALLSTATE\_ACCEPTED**, or **LINECALLSTATE\_CONNECTED**.</span></span>

<span data-ttu-id="c9e8c-119">一般來說，如果呼叫是傳入的呼叫，就會在從 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)取得的呼叫控制碼上呼叫 [**LineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)或第 [**一行 \_ CALLSTATE**](line-callstate.md)訊息來終止傳遞模式。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-119">Passthrough mode is normally terminated by calling [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) on the call handle obtained from [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) or the first [**LINE\_CALLSTATE**](line-callstate.md) message, if the call was an incoming call.</span></span> <span data-ttu-id="c9e8c-120">服務提供者將會關閉埠，並將數據機還原為其預設狀態。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-120">The service provider will close the port, and restore the modem to its default state.</span></span> <span data-ttu-id="c9e8c-121">應用程式必須在從 [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)收到的控制碼上呼叫 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-121">The application must call [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) on the handle it received from [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).</span></span>

<span data-ttu-id="c9e8c-122">藉由呼叫 [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) ，並將 *dwBearerMode* 參數設定為 **LINEBEARERMODE \_ VOICE**，也可以終止傳遞模式。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-122">Passthrough mode can also be terminated by calling [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) with the *dwBearerMode* parameter set to **LINEBEARERMODE\_VOICE**.</span></span> <span data-ttu-id="c9e8c-123">[**LineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)所設定的媒體類型 (模式) 會假設為作用中。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-123">The media type (mode) set by [**lineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode) is presumed to be in effect.</span></span> <span data-ttu-id="c9e8c-124">如果 **LINEMEDIAMODE \_ DATAMODEM** 為作用中，服務提供者將會接管呼叫，就好像它是已在進行中的資料數據機呼叫一樣; 如果接下來會呼叫 [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) ，服務提供者將發出適當的數據機命令或介面狀態變更，以捨棄資料呼叫。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-124">If **LINEMEDIAMODE\_DATAMODEM** is active, the service provider will take over the call as though it was a data modem call already in progress; if [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) is subsequently called, the service provider will issue the appropriate modem commands or interface state changes to drop a data call.</span></span>

> [!Note]  
> <span data-ttu-id="c9e8c-125">如果在呼叫進行時終止傳遞模式，則線路的 TAPI 服務提供者 (TSP) 可能會將數據機設定還原為其預設狀態。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-125">If Passthrough mode is terminated while the call is in progress, the TAPI service provider (TSP) for the line may restore the modem settings to their default state.</span></span> <span data-ttu-id="c9e8c-126">Unimodem 是在終止傳遞模式時一律會還原數據機設定的 TSP 範例。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-126">Unimodem is an example of a TSP that always restores the modem settings when terminating passthrough mode.</span></span> <span data-ttu-id="c9e8c-127">基於這個理由，無法使用傳遞模式作為設定裝置的方法。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-127">For this reason, Passthrough mode cannot be used as a method to configure the device.</span></span> <span data-ttu-id="c9e8c-128">傳遞模式應僅用於可在傳遞終止時視為已完成的相異活動。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-128">Passthrough mode should only be used for distinct activities that can be considered complete when Passthrough is terminated.</span></span> <span data-ttu-id="c9e8c-129">可使用通過模式的活動範例包括透過專屬的數據機通訊協定傳送傳真或播放 wave/音訊資料。</span><span class="sxs-lookup"><span data-stu-id="c9e8c-129">Examples of activities that can use passthrough mode include sending a fax or playing wave/audio data through a proprietary modem protocol.</span></span>

 

 

 
