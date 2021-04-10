---
title: 取得連結識別碼
description: 從 Windows Server 2003 開始，不再需要向 Microsoft 要求 linkID;自動產生 linkID 的流程。
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- 取得連結識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6893baab780d7fb481de0af77a607e988c3f87a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092631"
---
# <a name="obtaining-a-link-id"></a>取得連結識別碼

從 Windows Server 2003 開始，不再需要向 Microsoft 要求 [**linkID**](/windows/desktop/ADSchema/a-linkid) ;自動產生 **linkID** 的流程。 當屬性的 **linkID** 屬性設定為1.2.840.113556.1.2.50 時，系統會自動為新的連結屬性產生連結識別碼。 將 **linkID** 設定為轉寄連結的 [**attributeID**](/windows/desktop/ADSchema/a-attributeid) 或 [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) ，即可建立此轉寄連結的上一頁連結。 在建立轉寄連結之後，以及建立後置連結之前，必須重載架構快取。 否則，就不會在建立後置連結時找到轉寄連結的 **attributeId** 或 **ldapDisplayName** 。 架構快取是在進行架構變更後的幾分鐘內，或是在重新開機 DC 時，視需要重載。 建立所有轉寄連結、重載架構快取，然後建立所有的上一頁連結。

例如，當您建立新的屬性 **myForwardLinkAttr** 和 **myBackLinkAttr**，並想要將它們連結：

> [!Note]  
> 此範例中的 Oid 是假設。 如需取得新屬性之 Oid 的指示，請參閱 [從 Microsoft 取得物件識別碼](obtaining-an-object-identifier-from-microsoft.md) 。

 

1.  在要作為轉寄連結的屬性上，設定這些屬性：
    ```C++
    ldapDisplayName: myForwardLinkAttr
    OID: 1.2.840.113556.6.1234
    LinkID: 1.2.840.113556.1.2.50
    ```

    

2.  重載架構。
3.  在要做為後置連結的屬性上，設定這些屬性：
    ```C++
    ldapDisplayName: myBackLinkAttr
    OID: 1.2.840.113556.6.1235
    LinkID: 1.2.840.113556.6.1234 or myForwardLinkAttr
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[連結屬性](linked-attributes.md)
</dt> <dt>

[如何延伸架構](how-to-extend-the-schema.md)
</dt> </dl>

 

 