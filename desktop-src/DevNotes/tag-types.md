---
description: 描述與標記相關聯之值的資料類型。
ms.assetid: 009ad522-35da-4053-a7f6-61d7d240b98c
title: 標記類型
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8308f0adb9195363825a95253f1118305a88b9adeb46e9e7ce9518a6e005d96e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666389"
---
# <a name="tag-types"></a>標記類型

描述與標記相關聯之值的資料類型。



| 常數/值                                                                                                                                                                                                                            | 描述                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span id="TAG_TYPE_NULL"></span><span id="tag_type_null"></span><dl> <dt>**標記 \_輸入 \_ Null**</dt> <dt>0x1000</dt> </dl>                | 沒有與標記相關聯的值。<br/> |
| <span id="TAG_TYPE_BYTE"></span><span id="tag_type_byte"></span><dl> <dt>**標記 \_類型 \_ 位元組**</dt> <dt>0x2000</dt> </dl>                | **位元組** 值。<br/>                          |
| <span id="TAG_TYPE_WORD"></span><span id="tag_type_word"></span><dl> <dt>**標記 \_輸入 \_ WORD**</dt> <dt>0x3000</dt> </dl>                | **文字** 值。<br/>                          |
| <span id="TAG_TYPE_DWORD"></span><span id="tag_type_dword"></span><dl> <dt>**標記 \_輸入 \_ DWORD**</dt> <dt>0x4000</dt> </dl>             | **DWORD** 值。<br/>                         |
| <span id="TAG_TYPE_QWORD"></span><span id="tag_type_qword"></span><dl> <dt>**標記 \_輸入 \_ QWORD**</dt> <dt>0x5000</dt> </dl>             | **ULONGLONG** 值。<br/>                     |
| <span id="TAG_TYPE_STRINGREF"></span><span id="tag_type_stringref"></span><dl> <dt>**標記 \_輸入 \_ STRINGREF**</dt> <dt>0x6000</dt> </dl> | Token 化的字串值。<br/>                  |
| <span id="TAG_TYPE_LIST"></span><span id="tag_type_list"></span><dl> <dt>**標記 \_類型 \_ 清單**</dt> <dt>0x7000</dt> </dl>                | 標記值的清單。<br/>                      |
| <span id="TAG_TYPE_STRING"></span><span id="tag_type_string"></span><dl> <dt>**標記 \_類型 \_ 字串**</dt> <dt>0x8000</dt> </dl>          | 字串值。<br/>                            |
| <span id="TAG_TYPE_BINARY"></span><span id="tag_type_binary"></span><dl> <dt>**標記 \_輸入 \_ BINARY**</dt> <dt>0x9000</dt> </dl>          | 二進位值。<br/>                            |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**標記**](tag.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




