---
description: 屬性提供者會針對儲存在 WMI 儲存機制中之指定類別的實例，抓取和修改個別的屬性值。
ms.assetid: fe150157-cf9d-47da-8f94-b18eb0502bd8
ms.tgt_platform: multiple
title: 撰寫屬性提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8442225ee763a222b4bbdc87bb38477dbb69726183bb0546271039969b7f18bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118106864"
---
# <a name="writing-a-property-provider"></a>撰寫屬性提供者

屬性提供者會針對儲存在 WMI 儲存機制中之指定類別的實例，抓取和修改個別的屬性值。

下列程式描述如何建立屬性提供者。

**若要建立屬性提供者**

1.  使用 WMI 設計和註冊您的提供者。

    執行個體提供者會藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)實例和 [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md)類別，向 WMI 註冊。 如需詳細資訊，請參閱 [註冊屬性提供者](registering-a-property-provider.md)。

2.  為您的提供者執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面。

    WMI 使用 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 來載入和初始化提供者。 這是所有提供者通用的工作。 如需詳細資訊，請參閱 [初始化提供者](initializing-a-provider.md)。

    > [!Note]  
    > 強烈建議您使用多執行緒模型「兩者」的屬性提供者。

     

3.  為您的提供者執行 [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) 介面。

    [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider)介面是屬性提供者的主要介面。 這兩種主要方法是 [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) 和 [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty)。 如需詳細資訊，請參閱 [執行屬性提供者的主要介面](implementing-the-primary-interface-for-a-property-provider.md)。

4.  加入提供者所需的任何其他程式碼。

    設計您的提供者時，您很可能需要呼叫 WMI 介面。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md) 和 [維護提供者中的安全性層級](impersonating-a-client.md)。

    取得用戶端的資訊時，您可能需要存取該用戶端的安全性層級。 如需詳細資訊，請參閱模擬 [用戶端](impersonating-a-client.md)。

5.  以您的新程式碼取代預先存在的提供者。

    如果您沒有預先存在的提供者可進行複製，則不需要執行此步驟。 如需詳細資訊，請參閱 [更新提供者](updating-a-provider.md)。

 

 



