---
description: 您可以藉由將 WQL 查詢指派給 PostJoinFilter 限定詞，來篩選聯結視圖類別的實例。
ms.assetid: 926a7262-ea6b-4a5a-8aa7-6ec0ae389031
ms.tgt_platform: multiple
title: PostJoinFilter 辨識符號
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostJoinFilter
api_type:
- NA
api_location: ''
ms.openlocfilehash: be491c0bfefe77c2bf016789786212047d5ca8d00570c84057b8e8e346fb382e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317022"
---
# <a name="postjoinfilter-qualifier"></a>PostJoinFilter 辨識符號

您可以藉由將 WQL 查詢指派給 **PostJoinFilter** 限定詞，來篩選聯結視圖類別的實例。 WQL 查詢的值會套用到聯結視圖類別的實例。 您可以使用這個辨識符號，將 view 類別的實例限制為符合特定條件的實例。 下列 WQL 查詢會篩選依據 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)實例所呼叫之聯結類別的實例。


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



使用此辨識符號有數項限制：

-   **PostJoinFilter** 僅適用于聯結視圖類別。
-   查詢中指定的類別名稱和屬性名稱會參考 view 類別的屬性，而非來源類別的屬性。
-   不允許排除屬性;只 `SELECT *` 允許型別查詢。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**視圖提供者專用的限定詞**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

