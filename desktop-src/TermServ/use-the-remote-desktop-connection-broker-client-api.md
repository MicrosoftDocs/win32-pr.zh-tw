---
title: 如何使用遠端桌面連線代理人用戶端 API
description: 遠端桌面連線代理人用戶端 API 可讓協力廠商通訊協定廠商利用連線代理人，以加速處理使用其通訊協定的連線，以連接到伺服器陣列中的虛擬機器或遠端桌面伺服器。
ms.assetid: 05C2D6CA-C9C5-4783-B196-6A02918046EF
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c931245870cfb72aed54e5aaff24e12d03ddf9e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316186"
---
# <a name="how-to-use-the-remote-desktop-connection-broker-client-api"></a>如何使用遠端桌面連線代理人用戶端 API

遠端桌面連線代理人用戶端 API 可讓協力廠商通訊協定廠商利用連線代理人，以加速處理使用其通訊協定的連線，以連接到伺服器陣列中的虛擬機器或遠端桌面伺服器。

## <a name="instructions"></a>指示

### <a name="step-1-obtain-the-iconnectionbrokerclient-interface"></a>步驟1：取得 IConnectionBrokerClient 介面

當您的應用程式或通訊協定提供者初始化時，請執行下列步驟。

1.  呼叫 [**CBCreateClientInstance**](cbcreateclientinstance.md) 函數，以取得 [**IConnectionBrokerClient**](iconnectionbrokerclient.md) 介面。
2.  只要您需要，請保留 [**IConnectionBrokerClient**](iconnectionbrokerclient.md) 介面。
3.  當不再需要 [**IConnectionBrokerClient**](iconnectionbrokerclient.md) 介面時，請呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 方法。

### <a name="step-2-request-the-target-information"></a>步驟2：要求目標資訊

當您的通訊協定提供者收到連入連線要求時，請執行下列步驟來呼叫 [**IConnectionBrokerClient：： GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) 方法。 這個方法會從連接代理程式取得要將連接重新導向至的適當伺服器。

1.  建立可使用 [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)或類似函式來發出信號，以用於 *hStatusEvent* 參數的事件。
2.  配置 *pTargetInfo* 和 *pResult* 參數的記憶體。 這些記憶體區塊必須保持在原處，直到整個順序完成為止。
3.  填寫 [**CB \_ 連接 \_ 資訊**](cb-connection-info.md) 結構，其中包含連入連線的所有資訊。
4.  呼叫 [**GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) 方法，並傳遞所有必要的參數。 這是會傳回 [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) 介面實例的非同步方法。
5.  等候 *hStatusEvent* 事件變成已設定。
6.  每當設定 *hStatusEvent* 事件時，請呼叫 [**IConnectionBrokerRequest：： CheckStatus**](iconnectionbrokerrequest-checkstatus.md) 方法來判斷要求的狀態。
7.  當 [**CheckStatus**](iconnectionbrokerrequest-checkstatus.md) 傳回 **CB \_ 狀態 \_ 要求 \_ 已完成** 時， *pTargetInfo* 和 *pResult* 參數會包含其資訊。 您可以中斷等候迴圈，因為 *hStatusEvent* 參數將不再使用。
8.  使用 *pTargetInfo* 參數所代表的 [**CB \_ 目標 \_ 資訊**](cb-target-info.md)結構中的資訊，來決定要將傳入連接重新導向至何處。
9.  釋放 [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) 介面。
10. 關閉 *hStatusEvent* 事件控制碼，或將它重複用於後續的連接要求。

 

 