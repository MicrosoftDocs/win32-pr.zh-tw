---
description: 指定在設定時間戳記時，解碼器是否可以使用 (DTS) 的解碼時間戳記。
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ad80b0b7b29677ed0bee2f86a2c12c56c08441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975554"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>MF \_ MT \_ FSSourceTypeDecoded 屬性

指定媒體類型為自動解碼。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**


## <a name="remarks"></a>備註
媒體類型標示為屬性，以指出這不存在於實體來源上，並且由管線合成。 值為 1 (TRUE) 表示媒體類型已合成。 值為 0 (FALSE) ，或不存在值，表示它不存在。

在目前的版本中，您應該使用下列 GUID 值（而不是 MD_MT_FSSourceTypeDecoded 常數）來指定這個屬性：

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




