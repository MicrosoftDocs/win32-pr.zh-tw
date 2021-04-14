---
title: 使用 NDF 功能
description: Microsoft 透過公用 API 提供對 NDF 功能的存取。 發生問題時，應用程式可以使用此 API，在特定應用程式的內容內利用這項功能。
ms.assetid: db06b9a9-a64a-43ff-9b77-95230208cfd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca74a8a80f7babca75182625ec71dc1ec47cbc7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/10/2020
ms.locfileid: "104374921"
---
# <a name="using-ndf-functionality"></a>使用 NDF 功能

Microsoft 透過公用 API 提供對 NDF 功能的存取。 發生問題時，應用程式可以使用此 API，在特定應用程式的內容內利用這項功能。

使用 NDF 執行診斷的階段有三個：建立事件、執行診斷和修復，以及關閉事件。 本總覽指出哪些 NDF 功能可能與特定案例相關。 您可以在 [ [NDF 參考](ndf-reference.md) ] 區段中找到每個函式的詳細資訊。

## <a name="creating-an-incident"></a>建立事件

NDF 診斷會話需要特定的事件來進行診斷。 有幾個函數可用來建立事件。 選擇最符合應用程式嘗試在失敗發生時執行的功能。

-   [**NdfCreateConnectivityIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateconnectivityincident)：不需要額外資訊的一般網際網路連線問題。
-   [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) /[**NdfCreateWebIncidentEx**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincidentex)：連接至 HTTP 或 HTTPS URL。
-   [**NdfCreateSharingIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatesharingincident)：存取 UNC 路徑或檔案共用。
-   [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident)：解析 DNS 主機名稱。
-   [**NdfCreatePnrpIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatepnrpincident)：解析 PNRP 對等名稱。
-   [**NdfCreateGroupingIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreategroupingincident)：加入對等群組。
-   [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident)：使用通訊端連接到目的地， (沒有任何其他函式特別適用) 。
-   [**NdfCreateIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateincident)：當沒有其他適用的案例，以及要叫用的特定 NDF 協助程式類別已知 (以及需要) 的引數時，就會使用。 主要是供已撰寫自己的 helper 類別的應用程式開發人員用來進行測試。

## <a name="running-diagnosis-and-repairs"></a>正在執行診斷和修復

有兩種方式可以啟動診斷和修復功能。

-   使用 Windows 消費者介面 (建議的) 

    在標準 Windows 使用者介面中執行時，您可以直接呼叫 [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) 函數。 NDF Wizard 將會啟動並協助使用者找出 (（如果可能的話），並解決) 問題。 此函式會在此程式完成後傳回。 使用者介面可選擇性地對您的應用程式進行強制回應。

-   使用自訂消費者介面 (Windows 7 及更新版本僅) 

    不同的功能可用於未顯示任何使用者介面的案例中，或未使用標準 Windows 體驗 (例如 Media Center、內嵌應用程式和命令提示字元) 。 此選項會略過 NDF Wizard 中提供的使用者體驗功能，包括將結果限制為完全支援的根本原因，以及啟發學習法，以建議的順序向使用者顯示修復。 使用這些函式時，您必須自行提供任何這類功能。 您也必須確定釋放診斷結果所使用的記憶體。

    若要開始診斷，請呼叫 [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) 函數。 任何發現的問題都會以 [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) 結構集合的形式傳回給應用程式，以描述識別的根本原因和可能的修復。

    選取修復 (或要求使用者選取修復) 之後，應呼叫 [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) 以嘗試修復，並判斷問題是否已解決。

    在某些情況下，修復可能會成功執行，但不會解決問題。 在這種情況下，建議您關閉現有的事件，然後再開啟新的事件。 這可確保會識別初始修復未遮罩的任何新問題。 例如，假設沒有看到任何無線網路。 重設介面卡之後，就可以看見無線網路，但它們都不在慣用的清單中。 這是新的問題，需要新的診斷來識別。 如果這類的第二個診斷嘗試找不到其他問題，則可以嘗試進行不同的修復來解決原始問題，或是通知使用者無法解決問題。

    [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) 和 [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) 是同步 api。 如果您想要取消這些函數所起始的活動，請從另一個執行緒呼叫 [**NdfCancelIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcancelincident) 。 函式將會在診斷或修復程式中的下一個可用停止點傳回。

    在任何時間點，您都可以選擇性地呼叫 [**NdfGetTraceFile**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfgettracefile) ，以取得目前診斷會話的 NDF 記錄檔複本，並將它包含在您的應用程式記錄檔中。 一旦抓取記錄檔，就會清除記錄檔，而且後續的呼叫只會抓取最後一次呼叫此函式之後發生的事件。

## <a name="closing-an-incident"></a>關閉事件

當您完成診斷事件時，請呼叫 [**NdfCloseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident) 來釋放與針對該事件執行診斷相關聯的系統資源。  (請注意，這不會釋放 [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident)所建立的物件。
