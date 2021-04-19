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
# <a name="passthrough-mode"></a>傳遞模式

當呼叫在 **LINEBEARERMODE \_ 傳遞** 中為作用中時，服務提供者可讓應用程式直接存取附加的硬體來控制。 應用程式可以使用此模式，透過 [通訊功能](/windows/desktop/DevIO/communications-functions)存取非同步數據機，以設定或使用服務提供者不支援的特殊功能，例如 (類別1、2等) 的傳真。 通用數據機驅動程式 (UNIMODEM) 服務提供者支援此持有人模式。

支援 **LINEBEARERMODE \_ 傳遞** 的服務提供者會在 [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)結構的 **dwBearerModes** 成員中指出該服務提供者。 指出 **LINEBEARERMODE \_ 傳遞** 時，Unimodem 服務提供者也會包含在 **LINEDEVCAPS** 結構的 **DevSpecific** 區域中，此登錄機碼會用來存取與線路裝置相關聯之數據機的資料，格式如下：

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

例如：

``` syntax
    00000001 00000008 74737953 435c6d65  ........System\C
    65727275 6f43746e 6f72746e 7465536c  urrentControlSet
    7265535c 65636976 6c435c73 5c737361  urrentControlSet
    65646f4d 30305c6d xx003030 xxxxxxxx  Modem\0000.
```

然後可以使用 [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) 函式來開啟此登錄機碼。

使用 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)函數最常叫用傳遞模式，方法是在 *lpCallParams* 參數所指向之 [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)結構的 **dwBearerMode** 成員中設定 **LINEBEARERMODE \_ 傳遞** 位。 當此動作完成時，服務提供者會開啟數據機的序列埠，並立即將呼叫放入 **\_ 連接的 LINECALLSTATE**。 然後，應用程式可以使用 [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) 函式搭配裝置類別 "comm/datamodem" 來取得開啟的檔案控制代碼，以讀取和寫入至通訊埠。

也可以叫用傳遞模式，以回應傳入的呼叫。 一般而言，應用程式會在呼叫于 LINECALLSTATE 供應專案中 **叫 \_** 用傳遞模式，然後才會呼叫接聽。 應用程式不會呼叫 [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)，而是會呼叫 [**LineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams)，將 **LINEBEARERMODE \_** 傳遞當作 *dwBearerMode* 參數傳遞。 完成這項操作時，如同 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)，呼叫會立即置於服務提供者所 **\_ 連接的 LINECALLSTATE** 中，應用程式可以使用 [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)取得開啟埠的控制碼。 當呼叫位於 LINECALLSTATE 供應專案、 **LINECALLSTATE \_ 接受** 或 **LINECALLSTATE \_ 連線** 時，可以呼叫 **lineSetCallParams** 函數。 **\_**

一般來說，如果呼叫是傳入的呼叫，就會在從 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)取得的呼叫控制碼上呼叫 [**LineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)或第 [**一行 \_ CALLSTATE**](line-callstate.md)訊息來終止傳遞模式。 服務提供者將會關閉埠，並將數據機還原為其預設狀態。 應用程式必須在從 [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)收到的控制碼上呼叫 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 。

藉由呼叫 [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) ，並將 *dwBearerMode* 參數設定為 **LINEBEARERMODE \_ VOICE**，也可以終止傳遞模式。 [**LineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)所設定的媒體類型 (模式) 會假設為作用中。 如果 **LINEMEDIAMODE \_ DATAMODEM** 為作用中，服務提供者將會接管呼叫，就好像它是已在進行中的資料數據機呼叫一樣; 如果接下來會呼叫 [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) ，服務提供者將發出適當的數據機命令或介面狀態變更，以捨棄資料呼叫。

> [!Note]  
> 如果在呼叫進行時終止傳遞模式，則線路的 TAPI 服務提供者 (TSP) 可能會將數據機設定還原為其預設狀態。 Unimodem 是在終止傳遞模式時一律會還原數據機設定的 TSP 範例。 基於這個理由，無法使用傳遞模式作為設定裝置的方法。 傳遞模式應僅用於可在傳遞終止時視為已完成的相異活動。 可使用通過模式的活動範例包括透過專屬的數據機通訊協定傳送傳真或播放 wave/音訊資料。

 

 

 
