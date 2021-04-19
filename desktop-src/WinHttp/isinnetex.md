---
description: 判斷 IP 位址是否在特定子網中。
ms.assetid: 2fbfad9c-86b1-44c3-860b-a5c98ac6c2e9
title: isInNetEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isInNetEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: d738fbf5788fbe56d8c801b6c5256e96e8d4a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979320"
---
# <a name="isinnetex-function"></a>isInNetEx 函式

判斷 IP 位址是否在特定子網中。

## <a name="parameters"></a>參數

<dl> <dt>

*址* 
</dt> <dd>

包含 IPv6/IPv4 位址的字串。

</dd> <dt>

*IPprefix* 
</dt> <dd>

字串，其中包含以冒號分隔的 IP 前置詞，並在位欄位中指定前 n 個位 (亦即3ffe：8311： ffff：：/48 或 123.112.0.0/16) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果主機位於相同的子網中，則為 TRUE;否則為 FALSE。

如果前置詞的格式不正確，或在比較 (（例如 IPv4 首碼和 IPv6 位址) ）中使用不同類型的位址和前置詞，也會傳回 FALSE。

## <a name="examples"></a>範例

``` syntax
isInNetEx(host, "198.95.249.79/32");
    true if the IP address of host matches exactly 198.95.249.79
```

``` syntax
isInNetEx(host, "198.95.0.0/16");
    true if the IP address of the host matches 198.95.*.*
```

``` syntax
isInNetEx(host, "3ffe:8311:ffff::/48");
    true if the IP address of the host matches 3ffe:8311:fff:*:*:*:*:*
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[IPv6 感知 Proxy Helper API 定義](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[瀏覽器自動設定檔案格式的 IPv6 擴充功能](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



