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
ms.openlocfilehash: 81911b6afb00d61713f966ba9e1981b979e51008
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462569"
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

 

 




