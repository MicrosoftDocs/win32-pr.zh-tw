---
title: DVD-ROM
description: 網域屬性會抓取 DVD 的目前網域。
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD-ROM Windows Media Player
topic_type:
- apiref
api_name:
- DVD.domain
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0db8e6e212fec11de5f3619c2c1f97a90f579b34515983b0384d0d08ab0ff60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651168"
---
# <a name="dvddomain"></a>DVD-ROM

**網域** 屬性會抓取 DVD 的目前網域。

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串** ，其中包含下列其中一個值。



| String            | 描述                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| firstPlay         | 執行 DVD 光碟的預設初始化。                                                                                      |
| videoManagerMenu  | 顯示整個光碟的功能表。也稱為 Windows Media Player 的 topMenu。 通常稱為標題功能表或頂端功能表。 |
| videoTitleSetMenu | 顯示目前標題集的功能表。 也稱為 Windows Media Player 的 titleMenu。 通常稱為根功能表。              |
| title             | 通常會顯示目前的標題。                                                                                                 |
| stop              | DVD 導覽器位於 DVD 停止網域中。                                                                                          |
| 未定義         | 播放程式不在任何 DVD 網域中。                                                                                                      |



 

## <a name="remarks"></a>備註

每個 DVD 的撰寫方式不同。 某些 Dvd 不包含 firstPlay、videoManagerMenu 或 videoTitleSetMenu 網域。

**Windows Media Player 10** 行動裝置版：此屬性一律會傳回空字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 版本<br/>                  | Windows XP 或更新版本的 Windows Media Player<br/>                            |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DVD 物件**](dvd-object.md)
</dt> </dl>

 

 





