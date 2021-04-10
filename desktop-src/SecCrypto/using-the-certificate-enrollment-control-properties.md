---
description: 每個憑證註冊控制項屬性都是讀取/寫入，而且具有初始化的預設值以及一組可接受的值。
ms.assetid: e31dd6df-bc2a-401f-9343-a7dbb0f374bb
title: 使用憑證註冊控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192ad4efd3d2438f800d4a3872a8cf1057ca9920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691395"
---
# <a name="using-the-certificate-enrollment-control-properties"></a>使用憑證註冊控制項屬性

每個憑證註冊控制項屬性都是讀取/寫入，而且具有初始化的預設值以及一組可接受的值。 您可以將屬性設定為此集合中的任何值，以修改使用屬性之方法的行為。 若要取得所需的行為，請先設定屬性，然後再呼叫使用該屬性值的方法。

不過請注意，在呼叫下列方法之後

-   [**acceptPKCS7**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptpkcs7)
-   [**acceptFilePKCS7**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptfilepkcs7)
-   [**createPKCS10**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createpkcs10)
-   [**createFilePKCS10**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createfilepkcs10)

下列屬性已封鎖而無法重設

-   [**ProviderType**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providertype)
-   [**KeySpec**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_keyspec)
-   [**ProviderFlags**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providerflags)
-   [**容器**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_containername)
-   [**ProviderName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providername)

除非呼叫 [**ICEnroll4：： Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) 方法。

如需個別屬性和方法的詳細資訊，請參閱 [密碼編譯參考](cryptography-reference.md)中這些屬性和方法的參考主題。

下列各節包含設定和取得憑證註冊控制項屬性的特定語言資訊：

-   [C + + 中的憑證註冊控制項屬性](certificate-enrollment-control-properties-in-c-.md)

 

 
