---
description: 請務必務必將用來儲存整數的位元組順序和個別傳輸通訊協定在網路上使用的位元組順序之間的任何差異列入考慮。
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: 位元組順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554b9f00b67fcd602daee0ed33443e228e4e3976f334506d949e3af79fef7e8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560178"
---
# <a name="byte-ordering"></a>位元組順序

請務必務必將用來儲存整數的位元組順序和個別傳輸通訊協定在網路上使用的位元組順序之間的任何差異列入考慮。 傳遞至 Windows 通訊端常式或從中傳遞的位址或埠號碼的任何參考，都必須以網路順序 (可供使用之通訊協定的位元組由大到小) 。 在 IP 的案例中，這包括 [**sockaddr**](sockaddr-2.md) 結構的 ip 位址和埠參數 (但不是) 的 *sin \_ 系列* 參數。

許多 UNIX 系統會在 cpu 上運作，而這些 cpu 代表以網路位元組順序表示的整數 (位元組由大到小的) 。 因此，將整數從主機位元組順序轉換成網路位元組順序的需要略過，而不會造成問題，即使不建議對可攜性也是如此。

相反地，大部分 Intel® Cpu 用來表示整數的位元組順序是以位元組為單位。 因此，從主機位元組順序轉換成網路位元組順序之前，必須先將整數轉換成網路位元組順序，然後才能在 Winsock 通訊端函數和結構中使用。

假設應用程式通常會在與時間服務對應的 TCP 通訊埠上連線到伺服器，但提供了一種機制讓使用者指定替代埠。 [**Getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)所傳回的埠號碼已是網路順序，這是用來建立位址以進行不需要轉譯的格式。 不過，如果使用者想要使用不同的埠（輸入為整數），則應用程式必須在使用 [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) 或) [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) 函式之前，將它從主機轉換成 tcp/ip 網路順序 (，才能用來建立位址。 相反地，如果應用程式要在 [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) 所傳回的位址 (（例如) ）中顯示埠號碼，則必須先使用 [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) 或 [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) 函式) 將埠號碼從網路轉換成主機順序 (，才能顯示該埠號碼。

由於 Intel 和網際網路位元組的順序不同，因此上述的轉換是不可避免的。 應用程式寫入器的匯，應該使用 Winsock 提供的標準轉換函式，而不是撰寫自己的轉換程式碼，因為未來的 Winsock 執行可能會在主機順序與網路位元組順序相同的系統上執行。 只有在主機和網路位元組順序之間使用標準轉換函式的應用程式，才有可能是可移植的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)
</dt> <dt>

[**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[**htons**](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[將通訊端應用程式移植到 Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**sockaddr**](sockaddr-2.md)
</dt> <dt>

[Winsock 程式設計考慮](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtohl**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> </dl>

 

 



