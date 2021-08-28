---
description: MTP 擴充事件
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: MTP 擴充事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a95999557e67ee8929fddc56dd7fd8eb43e6831af9f81f884303a2089bbe3fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806708"
---
# <a name="mtp-extension-events"></a>MTP 擴充事件

事件會通知應用程式變更已發生在裝置上。 例如，應用程式可以註冊，以接收已移除裝置的通知。

## <a name="vendor-extended-event-codes"></a>廠商-擴充的事件代碼

當裝置製造商支援廠商擴充的事件時，其驅動程式會將廠商的事件程式碼 (UINT16) 與 **WPD \_ 事件 \_ MTP \_ 廠商 \_ 擴充 \_ 事件** GUID 的最高16位結合。

例如，如果廠商擴充的程式碼是0xC001，則產生的 GUID 會如下列範例所示：


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a>廠商擴充的事件參數

廠商擴充事件的參數是由 **WPD \_ 事件 \_ 參數 \_ 事件 \_ 識別碼** GUID 和 **WPD \_ 屬性 \_ MTP \_ EXT \_ 事件 \_** 參數（ **PROPVARIANTS** 的集合）所報告。 這些 **PROPVARIANTS** 會對應到事件參數。 如果沒有參數，此集合會是空的。


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[支援 MTP 擴充功能](supporting-mtp-extensions.md)
</dt> </dl>

 

 



