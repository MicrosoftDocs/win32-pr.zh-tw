---
description: WSDAPI 記錄包含可用於尋找 WSDAPI 應用程式失敗根本原因的偵錯工具資訊。
ms.assetid: 28b4c032-1c9a-4b3a-9a6a-2948456572b2
title: 啟用 WSDAPI 追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8f765249f4888a1dcfd2c6a44a81d3e2652a75bb983e85a881093d3c266b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049696"
---
# <a name="enabling-wsdapi-tracing"></a>啟用 WSDAPI 追蹤

WSDAPI 記錄包含可用於尋找 WSDAPI 應用程式失敗根本原因的偵錯工具資訊。 啟用追蹤時，記錄資訊會儲存在使用者指定位置的 .etl 檔案中。 您可以將此 etl 檔案傳送給 Microsoft 開發人員支援，以進行根本原因分析。 如需聯絡支援的相關資訊，請移至 [https://support.microsoft.com](https://support.microsoft.com) 。

此程式必須完成兩次：在用戶端上執行一次，並在主機上進行一次。

**啟用 WSDAPI 追蹤**

1.  使用記事本或其他文字編輯器，建立具有下列文字的文字檔：

    ``` syntax
    "{480217a9-f824-4bd4-bbe8-f371caaf9a0d}" 0xFF 0xFF
    "{649e3596-2620-4d58-a01f-17aefe8185db}" 0xFF 0xFF
    "{96ab095a-9519-4f5c-81ee-c510b0a45463}" 0xFF 0xFF
    "{f9be9c98-10db-4318-bb61-cb0ddea08bf7}" 0xFF 0xFF
    "{db1d0418-105a-4c77-9a25-8f96a19716a4}" 0xFF 0xFF
    "{7e2dbfc7-41e8-4987-bca7-76cadfad765f}" 0xFF 0xFF
    "{8b20d3e4-581f-4a27-8109-df01643a7a93}" 0xFF 0xFF
    "{6d04bf88-60a5-4d02-bc5c-94a20ba490ec}" 0xFF 0xFF
    "{75454210-b231-4fea-b2b4-2cc66d7ae8aa}" 0xFF 0xFF
    "{e176aa66-5cc8-4321-9624-f9c1d2b7bf06}" 0xFF 0xFF
    "{836767a6-af31-4938-b4c0-ef86749a9aef}" 0xFF 0xFF
    ```

2.  將文字檔儲存為 `C:\temp\traceguids.txt` ，然後關閉檔案。
3.  開啟提升權限的命令提示字元視窗。
4.  執行下列命令： **logman.exe create trace wsdlog-o c： \\ temp \\ wsd**
5.  執行下列命令： **logman.exe update wsdlog-pf c： \\ temp \\traceguids.txt**
6.  執行下列命令： **logman.exe 開始 wsdlog**
7.  啟動主機和用戶端，或在網路總管中按 F5，以重現失敗。

**停用 WSDAPI 追蹤**

1.  開啟提升權限的命令提示字元視窗。
2.  執行下列命令： **logman.exe 停止 wsdlog**

一旦已捕捉到應用程式失敗， \* 就可以將 etl 檔案傳送給 Microsoft 支援服務。 這些檔案位於 `C:\temp\wsd_*.etl` 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WSDAPI 診斷程式](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[https://support.microsoft.com](https://support.microsoft.com)
</dt> </dl>

 

 



