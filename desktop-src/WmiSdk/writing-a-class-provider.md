---
description: 類別提供者會管理 WMI 的類別或一系列的類別。
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: 撰寫類別提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45815c795b6f43f3e7ec99b9ce9535c4d14b2bc8426ea5ca6b44f736415bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311937"
---
# <a name="writing-a-class-provider"></a>撰寫類別提供者

類別提供者會管理 WMI 的類別或一系列的類別。 類別提供者可以是 push 或 pull;也就是說，它可以儲存本身的資料，或允許 WMI 將其資料儲存在 Windows 管理服務中。 雖然類別提供者是安裝在特定的電腦上，但它可以變更整個企業的類別定義。 因此，大部分的開發人員通常不會建立類別提供者。

在建立類別提供者之前，請確認支援的類別確實必須動態產生。 在大多數情況下，類別的清單會變得緩慢且有限。 如果是這種情況，您就不需要建立類別提供者。 相反地，您可以使用 WMI API 或 MOF 檔案，將您的類別定義放在 WMI 存放庫中。

下列程式描述如何執行類別提供者。

**若要執行類別提供者**

1.  判斷您的提供者是否為 push 或 pull 提供者。

    提取提供者會動態提供資料以回應應用程式要求，而推送提供者則會在 WMI 儲存機制中儲存一次資料。 如需詳細資訊，請參閱 [判斷推播或提取狀態](determining-push-or-pull-status.md)。

2.  使用 WMI 設計和註冊您的類別提供者。

    類別提供者會藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)實例和 [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md)實例，向 WMI 註冊。 如需詳細資訊，請參閱 [註冊類別提供者](registering-a-class-provider.md)。

3.  為您的提供者執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面。

    WMI 使用 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 來載入和初始化提供者。 如果您要設計推播提供者， **IWbemProviderInit** 是您將會執行的唯一介面。 如需詳細資訊，請參閱 [初始化提供者](initializing-a-provider.md)。

    > [!Note]  
    > 強烈建議您使用類別提供者來使用多執行緒模型「兩者」。

     

4.  加入提供者所需的任何其他程式碼。

    設計您的提供者時，您很可能需要呼叫 WMI 介面。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md) 和 [維護提供者中的安全性層級](impersonating-a-client.md)。

    取得用戶端的資訊時，您可能需要存取該用戶端的安全性層級。 如需詳細資訊，請參閱模擬 [用戶端](impersonating-a-client.md)。

5.  為您的提供者執行 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 介面。

    [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面是提取類別提供者的主要介面。 如需詳細資訊，請參閱 [執行類別提供者的主要介面](implementing-the-primary-interface-for-a-class-provider.md)。

6.  以您的新程式碼取代預先存在的提供者。

    如果您沒有預先存在的提供者可進行複製，則不需要執行此步驟。 如需詳細資訊，請參閱 [更新提供者](updating-a-provider.md)。

 

 



