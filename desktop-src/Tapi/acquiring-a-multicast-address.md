---
description: 下列程式碼片段說明如何要求及設定會議的多播位址。
ms.assetid: faff57a9-88b3-45ce-bf9e-3f7087dfd1fd
title: 取得多播位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb451bb403002a4b2dc347abf51e587d8ea02a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112613"
---
# <a name="acquiring-a-multicast-address"></a>取得多播位址

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

下列程式碼片段說明如何要求及設定會議的多播位址。

為了簡單起見，此片段顯示將一個多播位址指派給一個媒體專案。 在實際情況下，會針對參與會議的每個媒體專案，執行選取範圍、多播位址要求和指派。

此片段假設已經執行 [連接到 ILS 伺服器](connecting-to-an-ils-server.md) 。 此處所示的作業會在 [建立會議公告](creating-a-conference-announcement.md)的「必要時修改設定」一節中執行。


```C++
// If ( hr != S_OK ) process the error here.
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[多播 COM 介面](multicast-com-interfaces.md)
</dt> <dt>

[**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)
</dt> <dt>

[**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)
</dt> <dt>

[**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)
</dt> <dt>

[**IEnumMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)
</dt> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> <dt>

[**IEnumBstr**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr)
</dt> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

 



