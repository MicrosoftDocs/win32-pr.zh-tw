---
description: 下圖說明與 TAPI 3 會議 blob 控制項相關的主要物件。 顯示的介面會以超連結的形式出現在相關的參考頁面中。
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: 會議 Blob 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1361951fcb830676e36acb4ec397832629dc5745983c654317a457a0d66ac336
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867988"
---
# <a name="conference-blob-controls"></a>會議 Blob 控制項

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

下圖說明與 TAPI 3 會議 blob 控制項相關的主要物件。 顯示的介面會以超連結的形式出現在相關的參考頁面中。

![會議 blob 控制項和介面](images/rendblob.png)

會議 blob 包含會議物件的提供者特定資訊。 [**ITConferenceBlob**](itconferenceblob.md)介面 blob 的指標是藉由在 [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)上執行 QueryInterface 來取得的。 **ITConferenceBlob** 介面提供一般會議 blob 基本操作的方法。 使用非 SDP 會議 blob 的應用程式必須針對詳細操作來執行自己的方法。

會合提供用來操作 SDP 會議 blob 的 [**ITSdp**](itsdp.md) 介面。 SDP 是一種通訊協定，用來描述多媒體會話及其相關的排程資訊。 如需 SDP 通訊協定的詳細資訊，請找出網際網路工程任務推動小組 (IETF) RFC 2327，其標題為「SDP： Session Description Protocol」。 如果指定的會議 blob 有 **ITSDP** 介面，您可以在 [**ITConferenceBlob**](itconferenceblob.md)上執行 **QueryInterface** 來取得它的指標。

針對 SDP 會議 blob， [**ITTimeCollection**](ittimecollection.md)、 [**ITTime**](ittime.md)、 [**ITMediaCollection**](itmediacollection.md)和 [**ITMedia**](itmedia.md) 介面可讓您更詳細地控制 sdp 會議時間和媒體特性。

 

 



