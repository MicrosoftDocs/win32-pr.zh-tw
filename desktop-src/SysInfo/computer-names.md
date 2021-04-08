---
description: DNS 名稱包含一或多個以句點分隔的元件 (例如，msdn.microsoft.com) 。
ms.assetid: 7e083cb5-cf0a-4284-8b54-dac856910c44
title: 電腦名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf076f42e3353aa03db951e9dec428766cf4895
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853111"
---
# <a name="computer-names"></a>電腦名稱

DNS 名稱包含一或多個以句點分隔的元件 (例如，msdn.microsoft.com) 。 每個元件最多可達63個位元組。 每個名稱最多可以有255個位元組的總計。 DNS 名稱會以 UTF-8 字元集或 Unicode 表示。 名稱不區分大小寫。 如需詳細資訊，請參閱 [**DnsValidateName**](/windows/desktop/api/windns/nf-windns-dnsvalidatename)。

電腦是以其完整的 DNS 名稱來唯一識別，其包含其 DNS 主機名稱，以及指派給它的 DNS 網域的名稱。 若要取出電腦的完整 DNS 名稱、DNS 主機名稱或 DNS 功能變數名稱，請呼叫 [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) 函數。 若要設定電腦的 DNS 主機名稱或 DNS 功能變數名稱，請呼叫 [**SetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) 函數。 在使用者重新開機電腦之前，名稱變更不會生效。

NetBIOS 名稱包含最多15個位元組的 OEM 字元，包括字母、數位、連字號和句點。 某些字元特定于字元集。 NetBIOS 名稱通常是以 OEM 字元集表示。 OEM 字元集取決於地區設定。 某些 OEM 字元集將某些字元表示為兩個位元組。 依慣例，NetBIOS 名稱會以大寫表示，其中小寫到大寫的轉譯演算法是與 OEM 字元集相依。

[**SetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa)和 [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa)函式也可以設定和取出電腦的 NetBIOS 名稱。 依照慣例，NetBIOS 名稱和 DNS 主機名稱是相互依存的。 當您修改 DNS 名稱時，也會更新 NetBIOS 名稱。 NetBIOS 名稱是 DNS 主機名稱的 OEM 表示，最多可達 COMPUTERNAME 長度的最大 \_ \_ 字元數。 如果設定的 DNS 主機名稱超過最大 \_ COMPUTERNAME \_ 長度字元，則 NetBIOS 名稱會設定為已截斷的 dns 主機名稱版本。 否則，會將整個 DNS 主機名稱轉譯成 OEM NetBIOS 名稱。 警告：如果您修改 NetBIOS 名稱，使其不是 DNS 名稱的截斷對應，您將會中斷使用依賴此慣例之函式（例如 [**DnsHostnameToComputerName**](/windows/desktop/api/Winbase/nf-winbase-dnshostnametocomputernamea) ）的應用程式。

 

 
