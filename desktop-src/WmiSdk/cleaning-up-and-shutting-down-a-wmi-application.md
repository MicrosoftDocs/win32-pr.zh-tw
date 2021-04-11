---
description: 設定 IWbemServices 指標的安全性層級之後，您就可以存取 WMI 的各種功能。 使用 WMI 完成後，您必須關閉應用程式。
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: 清除和關閉 WMI 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7758cbdba81e018ff3362cec86aa5096838dc9e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944719"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a>清除和關閉 WMI 應用程式

設定 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 指標的安全性層級之後，您就可以存取 WMI 的各種功能。 使用 WMI 完成後，您必須關閉應用程式。

下列程式說明如何清除和關閉 WMI 應用程式。

**清除和關閉 WMI 應用程式**

1.  釋放任何開啟的 COM 介面。

    您必須記得發行的兩個主要介面是 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 和 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)。

2.  呼叫 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)。

    和所有 COM 應用程式一樣，您必須在應用程式結束時呼叫 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 。

3.  結束您的應用程式。

    下列程式碼範例顯示如何結束 WMI 用戶端應用程式。

    ```C++
        // The following #include and #define statements need
        // to be used with this code:
        // #define _WIN32_DCOM
        // #include <wbemidl.h>  
        // #pragma comment(lib, "wbemuuid.lib")
        
        // pSvc was declared as IWbemServices *pSvc;
        // pLoc was declared as IWbemLocator *pLoc;

        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 0;   // Program successfully completed.
    ```

    

    > [!Note]  
    > `pSvc`變數的類型是 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* ，qps-ploc 變數的類型為 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \* 。

     

您現在已成功初始化 COM、存取 WMI，並結束您的應用程式。 如需詳細資訊，請參閱 [範例：建立 WMI 應用程式](example-creating-a-wmi-application.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 c + + 建立 WMI 應用程式](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
