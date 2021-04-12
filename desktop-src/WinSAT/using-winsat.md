---
title: 使用 WinSAT
description: 您可以使用 Windows 系統評定工具 (WinSAT) API 來起始電腦硬體設定的正式和臨機操作評量、取得電腦的基本分數和評量的每個子元件的分數，以及取得評量的詳細資料，例如評定的處理器詳細資料。
ms.assetid: b0860c4a-cec3-440c-b31a-7e7ad1b393d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a23ab35d989a736fa61833e678c0a4c79954e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372092"
---
# <a name="using-winsat"></a>使用 WinSAT

\[在 Windows 8.1 之後，可能會變更或無法使用 WinSAT。\]

您可以使用 Windows 系統評定工具 (WinSAT) API 來起始電腦硬體設定的 [正式和](#initiating-an-assessment) 臨機操作評量、 [取得電腦的基本分數](#retrieving-the-scores-of-the-assessment) 和評量的每個子元件的分數，以及 [取得評量的詳細資料](#retrieving-details-of-the-assessment)，例如評定的處理器詳細資料。

## <a name="initiating-an-assessment"></a>起始評量

Windows 8.1 之後，您就可以起始電腦的正式和臨機操作評量。 正式評量會評估電腦的下列子元件：

-   CPU
-   記憶體
-   主要磁碟
-   視訊卡

若要起始正式的評量，請呼叫 [**IInitiateWinSATAssessment：： InitiateFormalAssessment**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateformalassessment) 方法。 正式評量的結果會儲存在評量存放區中，並可于日後取回。

一般來說，您會使用臨機操作評量來評定電腦的一個子元件，例如 CPU 或記憶體。 不過，您可以使用 **正式** 的參數來評估所有子元件。 若要起始臨機操作評量，請呼叫 [**IInitiateWinSATAssessment：： InitiateAssessment**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateassessment) 方法。 請注意，特定評量的結果不會儲存在評量存放區中。

若要在進行進度或評定完成時取得通知，請執行 [**IWinSATInitiateEvents**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iwinsatinitiateevents) 介面。

您無法從遠端或在執行電池的電腦上執行正式評量。 您也無法在圖形子元件上從遠端執行臨機操作評量。

## <a name="retrieving-the-scores-of-the-assessment"></a>正在抓取評量的分數

您可以取得電腦的基本分數，以及評量每個子元件的分數。 您可以使用 API 來只取得正式評量的分數。 若要取得特定評量的分數，您必須在命令列中包含 **-xml** 引數，以將評量結果儲存至 xml 檔案，然後剖析元件分數的檔案。

基本分數是電腦硬體設定的一般度量。 較高的基本分數通常表示電腦的執行速度會比低基本分數的電腦更好且更快速，尤其是在執行更先進且耗用大量資源的工作時。

每個硬體元件都會得到個別的子分數。 您電腦的基本分數是由最低的子分數所決定。 例如，如果個別硬體元件的最低子分數是 2.6，基本分數就是 2.6。 基本分數不是所有子分數的平均。

使用者可以使用基本分數，安心地購買符合其電腦基本分數的程式與其他軟體。 例如，如果電腦的基本分數為3.3，則使用者可以安心地購買針對此 Windows 版本所設計的任何軟體，這些軟體需要基本分數為3或更低的電腦。

若要取得基本分數，請先呼叫 [**IQueryRecentWinSATAssessment：： get \_ Info**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) 方法來取得 [**IProvideWinSATResultsInfo**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) 介面。 然後，呼叫 [**IProvideWinSATResultsInfo：： get \_ SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) 方法以取得基本分數。

使用者可以使用子元件分數來判斷電腦的子元件是否可以支援特定類型的應用程式。 例如，花更多時間讀取或寫入檔的使用者可能需要比執行科學應用程式的使用者更高的分數，而執行科學應用程式的使用者可能需要較高的 CPU 子元件分數，而且可能不在意較低的磁片分數。

若要取得每個子元件的分數，請先呼叫 [**IQueryRecentWinSATAssessment：： get \_ Info**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) 方法來取得 [**IProvideWinSATResultsInfo**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) 介面。 然後呼叫 [**IProvideWinSATResultsInfo：： GetAssessmentInfo**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-getassessmentinfo) 方法，以取得 [**IProvideWinSATAssessmentInfo**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatassessmentinfo) 介面。 針對您想要取得其分數的每個子元件，呼叫 [**IProvideWinSATAssessmentInfo：： get \_ 分數**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) 方法。

## <a name="retrieving-details-of-the-assessment"></a>正在抓取評量的詳細資料

WinSAT API 會提供每個子元件的整體基本分數和分數。 若要取得評量的詳細資料 (例如，用來計算評估) 之處理器分數和詳細資料的計量，您必須從 XML 評估檔取得資料。 若要取得最新正式評量的詳細資料，請呼叫 [**IQueryRecentWinSATAssessment：： get \_ XML**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_xml) 方法。 若要取得 WinSAT 資料存放區中每個評量的詳細資料，請呼叫 [**IQueryAllWinSATAssessments：： get \_ AllXML**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryallwinsatassessments-get_allxml) 方法。

如需 XML 架構的詳細資訊，以及您可以取得的詳細資料，請參閱 [WinSAT 架構](winsat-schema.md)。

 

 




