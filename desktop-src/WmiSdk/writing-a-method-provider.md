---
description: 方法提供者允許 WMI 存取類別的方法。 例如，代表應用程式的類別可能會有一個終止應用程式的方法。
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: 撰寫方法提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8626e2e16fe5424a0b05df81e2444a72ecb8841f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975029"
---
# <a name="writing-a-method-provider"></a>撰寫方法提供者

方法提供者允許 WMI 存取類別的方法。 例如，代表應用程式的類別可能會有一個終止應用程式的方法。

在更新現有的方法提供者時，變更方法輸入和輸出參數的順序，可能會導致呼叫方法的應用程式失敗。 輸入或輸出參數的順序，是由每個參數上的 [**識別碼**](standard-wmi-qualifiers.md) 辨識符號值所建立。 第一個參數的 **識別碼** 值為零。 在現有參數的結尾加入新的輸入參數，而不是將它們插入已建立的序列中。

下列程式描述如何執行方法提供者。

**若要執行方法提供者**

1.  使用 WMI 設計和註冊您的類別提供者。

    類別提供者會藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)實例和 [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md)類別，向 WMI 註冊。 如需詳細資訊，請參閱 [註冊方法提供者](registering-a-method-provider.md)。

2.  為您的提供者執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面。

    > [!Note]  
    > 強烈建議您使用方法提供者來使用多執行緒模型「兩者」。

     

3.  為您的提供者執行 [**IWbemServices：： ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) 方法。

    [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面是方法提供者的主要介面。 如需詳細資訊，請參閱 [執行方法提供者的主要介面](implementing-the-primary-interface-for-a-method-provider.md)。

4.  加入提供者所需的任何其他程式碼。

    設計您的提供者時，您很可能需要呼叫 WMI 介面。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md) 和 [維護提供者中的安全性層級](impersonating-a-client.md)。

    取得用戶端的資訊時，您可能需要存取該用戶端的安全性層級。 如需詳細資訊，請參閱模擬 [用戶端](impersonating-a-client.md)。

5.  以您的新程式碼取代預先存在的提供者。

    如果您沒有預先存在的提供者可進行複製，則不需要執行此步驟。 如需詳細資訊，請參閱 [更新提供者](updating-a-provider.md)。

 

 



