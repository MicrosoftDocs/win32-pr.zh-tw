---
description: 執行個體提供者會提供一個或多個指定類別的實例。
ms.assetid: d53c3399-cba8-4b5d-8da0-b5a23f94c0ae
ms.tgt_platform: multiple
title: 撰寫執行個體提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bddfaa867624bd84cc975d32a8e7b747064d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982487"
---
# <a name="writing-an-instance-provider"></a>撰寫執行個體提供者

執行個體提供者會提供一個或多個指定類別的實例。 例如，執行個體提供者可以提供 CPU 或其他硬體類型的相關資訊。 因為執行個體提供者所管理的物件通常會定期變更，所以所有執行個體提供者都會被視為提取提供者;亦即，每當 WMI 提出資訊要求時，就會動態抓取有關受管理物件的資訊的提供者。 此名稱來自于 WMI 「提取」來自提供者的資訊，代表用戶端要求。 使用提取技術時，執行個體提供者可以支援特定實例的抓取、列舉、修改、刪除和查詢處理。

高效能的提供者可以提高執行個體提供者的效率，或以程式設計方式存取系統監視器中顯示的資料。 如需詳細資訊，請參閱 [讓執行個體提供者成為 High-Performance 提供](making-an-instance-provider-into-a-high-performance-provider.md)者。

下列程式描述如何撰寫執行個體提供者。

**若要撰寫執行個體提供者**

1.  向[WMI 註冊您的提供者](registering-an-instance-provider.md)。

    執行個體提供者會藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)實例和 [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md)類別，向 WMI 註冊。

2.  [初始化您的提供者](initializing-a-provider.md)。

    WMI 使用 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 來載入和初始化提供者。 這是所有提供者通用的工作。

    > [!Note]  
    > 強烈建議您使用執行個體提供者來使用多執行緒模型「兩者」。

     

3.  [為您的提供者執行 IWbemServices 介面](implementing-the-primary-interface-for-an-instance-provider.md)。

    [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面是執行個體提供者的主要介面。

4.  加入提供者所需的任何其他程式碼。

    設計您的提供者時，您很可能需要呼叫 WMI 介面。 如需詳細資訊，請參閱 [進行 WMI 的呼叫](making-calls-to-wmi.md)。

    取得用戶端的資訊時，您可能需要存取該用戶端的安全性層級。 如需詳細資訊，請參閱模擬 [用戶端](impersonating-a-client.md)。

5.  如有必要，請 [執行高效能介面](improving-the-efficiency-of-an-instance-provider.md)。

    高效能介面可增加提供者回應 WMI 要求的速度。

6.  如有必要，請 [執行部分實例更新的支援](supporting-partial-instance-operations.md)。

    顧名思義，部分實例更新是用來只更新部分實例的技巧。 如需從用戶端呼叫部分實例的詳細資訊，請參閱 [更新部分的實例](updating-part-of-an-instance.md) 和 [取出 WMI 實例的一部分](retrieving-part-of-an-instance.md)。

7.  以您的新程式碼取代預先存在的提供者。

    如果您沒有預先存在的提供者可進行複製，則不需要執行此步驟。 如需詳細資訊，請參閱 [更新提供者](updating-a-provider.md)。

 

 



