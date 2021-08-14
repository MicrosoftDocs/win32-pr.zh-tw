---
description: MTP 延伸格式
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: MTP 延伸格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a490c29c98b454b7d563e8af46131b040f123b9de2ef689ea5ede1a2ac100ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193954"
---
# <a name="mtp-extension-formats"></a>MTP 延伸格式

裝置上的檔案格式可由 GUID 值描述。 這個值是由 [WPD \_ 物件格式] 屬性所指定 \_ 。

## <a name="vendor-extended-formats"></a>廠商延伸格式

當裝置製造商支援廠商延伸格式時，其驅動程式會將廠商的格式代碼 (UINT16) 與 **WPD \_ 物件 \_ 格式 \_ 未指定** GUID 的最高16位結合在一起。

例如，如果廠商擴充的程式碼是0xB001，則產生的 GUID 會如下列範例所示：


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[支援 MTP 擴充功能](supporting-mtp-extensions.md)
</dt> </dl>

 

 



