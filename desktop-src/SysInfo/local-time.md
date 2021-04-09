---
description: 當系統在內部使用以 UTC 為基礎的時間時，您的應用程式通常會顯示當地時間，也就是時區的日期和時間。
ms.assetid: a6570ec5-ac77-427a-86d9-32cbecc62e37
title: 當地時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c60eb9ca53245a12eba1bc0096b522eae97de75a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848229"
---
# <a name="local-time"></a>當地時間

當系統在內部使用以 UTC 為基礎的時間時，您的應用程式通常會顯示 **當地時間**，也就是時區的日期和時間。 因此，若要確保正確的結果，您必須知道函式是否預期接收 UTC 時間或本地時間，以及函式是否傳回以 UTC 為基礎的時間或本地時間。

目前的時區設定會控制系統在 UTC 和本地時間之間的轉換方式。 您可以使用 [**GetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation) 函式來取出目前的時區設定。 函式會將結果複製到 [**時區 \_ \_ 資訊**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) 結構，並傳回值，指出當地時間目前是否為標準時間或日光節約時間 (DST) 。 您可以使用 [**SetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation) 函數來設定時區設定。 若要支援從 year 變更為 year 的日光節約時間範圍，請使用 [**GetTimeZoneInformationForYear**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear)、 [**GetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation) 和 [**SetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation) 函數。

若要取出本地時間，請使用 [**GetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime) 函數。 **GetLocalTime** 會根據目前的時區設定，將系統時間轉換為當地時間，並將結果複製到 [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) 結構。 您可以使用 [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime) 函數來設定系統時間。 **SetLocalTime** 會假設您已指定本地時間，並會在設定系統時間之前轉換為 UTC。

當您呼叫 [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime)時，系統會使用目前的時區資訊（包括日光節約時間設定）來執行轉換。 請注意，系統會使用目前時間的日光節約時間設定，而不是您所設定的新時間。 因此，若要確保正確的結果，請呼叫 **SetLocalTime** 第二次，現在第一個呼叫已更新日光節約時間設定。

若要將 UTC 時間轉換為當地時間，請使用 [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) 函數。 若要將當地時間轉換為 UTC 時間，請使用 [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime) 函數。

 

 
