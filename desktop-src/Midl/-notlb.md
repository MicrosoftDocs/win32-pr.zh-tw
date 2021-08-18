---
title: /notlb 參數
description: /Notlb 參數會防止 MIDL 編譯器產生類型程式庫 (TLB) 檔。
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- /notlb 參數 MIDL
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e309ed753d1549c31c9e3dea0a5c7aa87b32217aa12e5ee04934a183927adf87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067518"
---
# <a name="notlb-switch"></a>/notlb 參數

**/Notlb** 參數會防止 MIDL 編譯器產生類型程式庫 (TLB) 檔。

``` syntax
midl /notlb
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

根據預設，MIDL 編譯器會在遇到連結 [**庫**](library.md) 語句時產生 TLB 檔案。 此參數會覆寫預設行為。

當指定 **/notlb** 選項時，會如往常般產生所有其他的存根、標頭等等。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/tlb**](-tlb.md)
</dt> </dl>

 

 




