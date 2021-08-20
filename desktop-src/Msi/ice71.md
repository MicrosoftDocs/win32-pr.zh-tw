---
description: ICE71 會確認媒體資料表是否包含 DiskId 等於1的專案。
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1090eb8b1a36ed361ef763bfda3875a8fde052ed8643dceeb660c88ae954a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142512"
---
# <a name="ice71"></a>ICE71

ICE71 會確認 [媒體資料表](media-table.md) 是否包含 DiskId 等於1的專案。  (Windows Installer 會假設 .msi 的封裝位於磁片1上。 ) 

## <a name="result"></a>結果

如果媒體資料表未包含 DiskId 等於1的專案，ICE71 會傳回錯誤。

## <a name="example"></a>範例

ICE71 會針對所顯示的範例報告下列錯誤。

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

T0 修正這個錯誤，請變更將封裝儲存至1之專案的 DiskId。

[媒體資料表](media-table.md) (部分) 



| DiskId |
|--------|
| 2      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



