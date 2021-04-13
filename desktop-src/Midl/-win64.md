---
title: /win64 參數
description: /Win64 參數會指示 MIDL 編譯器產生64位環境的存根檔或類型程式庫檔案。請注意，此參數已淘汰。
ms.assetid: 6f4780d3-6415-42af-a8ee-3884a8cebe26
keywords:
- /win64 參數 MIDL
topic_type:
- apiref
api_name:
- /win64
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61906126607c0a8d4b81ef76805bb4b7e0d4145
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312297"
---
# <a name="win64-switch"></a>/win64 參數

**/Win64** 參數會指示 MIDL 編譯器產生64位環境的存根檔或類型程式庫檔案。

> [!Note]  
> 此參數已淘汰。 請改用 [**/ia64**](-ia64.md) 或 [**/amd64**](-amd64.md) 參數。 **/Win64** 參數相當於 **/ia64** 參數。

 

``` syntax
midl /win64
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

**/Win64** 參數相當於將 [**/env**](-env.md)參數設定為 win64。

> [!Note]  
> 您無法使用 MIDL.exe 在 Windows 2000 上產生64位 tlb。

 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/env**](-env.md)
</dt> <dt>

[**/ia64**](-ia64.md)
</dt> <dt>

[**/amd64**](-amd64.md)
</dt> </dl>

 

 




