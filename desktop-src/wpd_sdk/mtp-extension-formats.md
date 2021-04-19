---
description: MTP 延伸格式
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: MTP 延伸格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff86265e47071fce9fe523cfbb64f2e355ed541e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985666"
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

 

 



