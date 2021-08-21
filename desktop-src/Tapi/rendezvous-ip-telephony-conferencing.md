---
description: TAPI 3 會合控制項可讓程式設計人員建立可建立及探索多媒體多播 IP 會議的應用程式。
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: 彙集 IP 電話語音會議
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c1486f2ca730f1efb0391fdea5a3ad22bec65385a31bce9bf233f0f230b7ee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773568"
---
# <a name="rendezvous-ip-telephony-conferencing"></a>彙集 IP 電話語音會議

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

TAPI 3 會合控制項可讓程式設計人員建立可建立及探索多媒體多播 IP 會議的應用程式。

彙集的主要元件：

[目錄控制項](directory-controls.md) 是 ILS 或 NTDS 伺服器上的會議清單摘要。

[會議 Blob 控制項](conference-blob-controls.md) 代表會議特定的資訊，例如開始和停止時間。 提供適用于 SDP 通訊協定 blob 的特殊介面。 如需詳細資訊，請參閱 RFC 2327，其標題為「SDP： Session Description Protocol」。 您可以使用網際網路搜尋引擎來找出此 RFC 的目前複本。

[多播 COM 介面](multicast-com-interfaces.md) 是 MADCAP 函式的 COM 包裝函式，先前稱為 MDHCP。 這些介面可讓應用程式從多播位址佈建服務器取得多播位址。

下列內容提供 IP 電話語音和會議的會合控制項一般總覽和一些使用範例。

 

 



