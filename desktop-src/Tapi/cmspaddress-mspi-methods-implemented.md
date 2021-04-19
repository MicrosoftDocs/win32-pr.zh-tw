---
description: 以下是所有 Msp 都必須執行的標準 MSPI 方法。 這些方法的主要檔集存在於媒體服務提供者介面 (MSPI) 參考區段中。
ms.assetid: 22d4828e-f439-44ca-aa6c-f7f18c5fd64f
title: CMSPAddress MSPI 方法實作為
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed19bbacc13990d052c35bda68f97db80ff68ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988404"
---
# <a name="cmspaddress-mspi-methods-implemented"></a>CMSPAddress MSPI 方法實作為

以下是所有 Msp 都必須執行的標準 MSPI 方法。 這些方法的主要檔集存在於 [媒體服務提供者介面 (MSPI) 參考](media-service-provider-interface-mspi-reference.md) 區段中。



| CMSPAddress 方法                                                                          | Description                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**初始化**](/windows/desktop/api/msp/nf-msp-itmspaddress-initialize)                                                | 第一次建立此 MSP 時，由 TAPI3 呼叫 (Interface [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) 。                                                                                                                                                                                                                                                                                                   |
| [**關閉**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdown)                                                    | 當此位址未在使用中時，由 TAPI3 呼叫 (介面 [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) 。                                                                                                                                                                                                                                                                                         |
| [**ReceiveTSPData**](/windows/desktop/api/msp/nf-msp-itmspaddress-receivetspdata)                                        | 當 TSP 將資料傳送至此 MSP 位址物件時，由 TAPI3 呼叫 (Interface [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) 。                                                                                                                                                                                                                                                                               |
| [**GetEvent**](/windows/desktop/api/msp/nf-msp-itmspaddress-getevent)                                                    |  (介面 [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) 由 TAPI3 呼叫，以取得有關事件的詳細資訊。                                                                                                                                                                                                                                                                                       |
| [**取得 \_ StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals)                        | ITTerminalSupport helper 函式 [**GetStaticTerminals**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals)的 (介面 [](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) OLE Automation 包裝函式。                                                                                                                                                                                                                            |
| [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals)               |  (介面 [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) Helper 函數 [**GetStaticTerminals**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals)的) 列舉包裝函式。                                                                                                                                                                                                                               |
| [**取得 \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses)          | ITTerminalSupport helper 函式 [**GetDynamicTerminalClasses**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses)的 (介面 [](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) OLE Automation 包裝函式。                                                                                                                                                                                                              |
| [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) |  (介面 [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) Helper 函數 [**GetDynamicTerminalClasses**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses)的) 列舉包裝函式。                                                                                                                                                                                                                 |
| [**CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)                                   |  (介面 [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) 這個方法是由應用程式呼叫，以建立動態終端。 它會在 MSP 的背景工作執行緒上排程工作專案，然後在執行時，要求終端機管理員建立動態終端。 衍生類別可以覆寫這個方法，以建立動態終端機的方式。                                |
| [**GetDefaultStaticTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-getdefaultstaticterminal)               |  (介面 [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) 這個方法是由應用程式呼叫，以取得指定類型和方向的預設靜態終端機。 它會視需要更新預設的終端機清單 (，) 並傳回介面指標。 衍生的類別可以覆寫這個方法，以有自己的方式來決定預設的終端機。 鎖定終端機清單。 |



 

 

 
