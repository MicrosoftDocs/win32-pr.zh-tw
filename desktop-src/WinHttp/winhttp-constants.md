---
description: 本主題將識別 WinHTTP 使用的常數。
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: WinHTTP 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7c277b4235e23254000766fdef53d25f19ddbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469080"
---
# <a name="winhttp-constants"></a>WinHTTP 常數

WinHTTP 使用下列常數：

<dl> <dt>

[**錯誤訊息**](error-messages.md)
</dt> <dd>

WinHTTP 函數特定的錯誤訊息。 這些函數也會在適當的情況下傳回 Windows 錯誤訊息。 對應至每個常數的值是應用程式開發介面的常數值， (API) 函式和 [**WinHttpRequest**](winhttprequest.md) 物件錯誤號碼的較低16位。

</dd> <dt>

[**HTTP 狀態碼**](http-status-codes.md)
</dt> <dd>

常數和對應的值，指出網際網路上的伺服器所傳回的 HTTP 狀態碼。

</dd> <dt>

[**選項旗標**](option-flags.md)
</dt> <dd>

[**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)和 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)支援的選項旗標。 所有有效的選項旗標值都大於或等於 WINHTTP \_ FIRST \_ 選項，且小於或等於 winHTTP \_ LAST \_ 選項。

</dd> <dt>

[**網際網路 \_ 埠**](internet-port.md)
</dt> <dd>

指出埠的文字值。

</dd> <dt>

[**網際網路 \_ 配置**](internet-scheme.md)
</dt> <dd>

WinHTTP 支援的網際網路架構。

</dd> <dt>

[**查詢資訊旗標**](query-info-flags.md)
</dt> <dd>

[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)所使用的屬性和修飾詞。

</dd> </dl>

 

 



