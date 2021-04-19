---
description: TAPI 3 秒會合 IP 電話語音會議中說明了使用以 IP 為基礎的網路的 Advanced 會議。 下列是基本會議的相關內容。
ms.assetid: f685097b-1b54-412b-999f-d9bdb3120ab9
title: 會議
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace4cb45bf74335298a3d4d262d064eb85c547f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000081"
---
# <a name="conference"></a>會議

使用以 IP 為基礎的網路的 Advanced 會議，說明于 TAPI 3 的會合 [IP 電話語音會議](rendezvous-ip-telephony-conferencing.md)中。 下列是基本會議的相關內容。

會議研討會是同時包含兩方以上的會話。 您可以使用以外部伺服器為基礎的橋接器或以交換器為基礎的會議橋接器來設定它們。

在以伺服器為基礎的會議會話中，所有參與的合作物件都會撥入伺服器，該伺服器會將媒體串流混合在一起，並將混合的每個參與者傳送出去。 只有在應用程式和橋接器伺服器之間進行單一呼叫的情況下，才會有個別合作物件的概念。 對 TAPI 而言，這種類型的會議呼叫似乎是正常的一對一連線。

以交換器為基礎的會議會進行階段，其中有些可能會在服務提供者支援時結合：

1.  起始一般通訊會話。
2.  建立會議會話，其中第一個成員是起始會議的合作物件。
3.  在目前連接的另一端，與合作物件建立會議諮詢會話。
4.  將諮詢會話新增至會議。

當會話成為會議的成員之後，該成員的狀態就會還原為 conferenced。 會議會話的狀態通常會變成 [ *已連線*]。 會議的會話識別碼和所有加入的合作物件都會保持有效。 您可以接收所有呼叫的狀態事件。 例如，如果其中一個成員因為掛斷而中斷連線，則適當的狀態訊息會通知應用程式這項事實。

**TAPI 2.x：** 應用程式可以使用 LINECALLPARAMFLAGS NOHOLDCONFERENCE 選項來使用 Pbx 的「無保留會議」功能 \_ ; 這項功能可讓另一部裝置（例如監督員或錄製裝置）以無訊息模式附加至該行。

當您取消會議協力廠商的諮詢會話或在先前建立的會議中移除協力廠商時，服務提供者可能會釋出會議，並將會話還原為一般的兩方連線。 如果是這種情況，會議會話將會轉換為 *閒置* 狀態，而唯一剩餘的參與會話將會從 conferenced 轉換為 *連線* 狀態。

並非所有服務提供者都支援會議。

**TAPI 2.x：**[**LineSetupConference**](/windows/win32/api/tapi/nf-tapi-linesetupconference)函式會接受原始的兩方呼叫做為輸入、配置會議通話、將原始呼叫連接到會議，以及配置將控制碼傳回給應用程式的諮詢通話。

如果應用程式要將另一個成員新增至會議，可以在諮詢電話上執行撥號操作。 接著會在 [**lineAddToConference**](/windows/win32/api/tapi/nf-tapi-lineaddtoconference) 函式中使用會議通話控制碼和諮詢通話連接。 如果服務提供者支援，也可以使用 [**linePrepareAddToConference**](/windows/win32/api/tapi/nf-tapi-lineprepareaddtoconference) 函數來新增會議成員。

如果服務提供者支援，則會使用 [**lineRemoveFromConference**](/windows/win32/api/tapi/nf-tapi-lineremovefromconference) 函式移除會議成員。

或者，您也可以使用 [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer) 函式來建立會議，此函式會傳回諮詢通話控制碼，而 [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer) 函式會使用會議選項 (而非 [傳送](transfer-ovr.md) 選項) 。

**TAPI 3.x：**[**ITBasicCallControl：：**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-conference) session 方法會將現有的會話作為輸入，並建立 [CallHub 物件](callhub-object.md)（如果尚未存在的話）。 [**ITBasicCallControl：： Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish)方法會將諮詢呼叫加入至 CallHub。 您可以使用 [**ITAddress：： CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)建立其他諮詢會話，並使用「 **會議** 」和「 **完成** 」方法新增。

> [!Note]  
> 定址線路裝置的功能可限制在單一呼叫中 conferenced 的合作物件數目，以及會議是否以一般的兩方電話開始。

 

 

 
