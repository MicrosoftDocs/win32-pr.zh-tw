---
description: 這些資料類型可以用來指定登錄值的型別。
title: '登錄資料類型 (Winnt. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4185e7af-e1f0-40af-91c7-0ff7e27896ae
api_name:
- REG_BINARY
- REG_DWORD
- REG_QWORD
- REG_DWORD_LITTLE_ENDIAN
- REG_QWORD_LITTLE_ENDIAN
- REG_DWORD_BIG_ENDIAN
- REG_EXPAND_SZ
- REG_LINK
- REG_MULTI_SZ
- REG_NONE
- REG_RESOURCE_LIST
- REG_SZ
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4de4595b55716d58df04a598dd6ba298f22829d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104992519"
---
# <a name="registry-data-types"></a>登錄資料類型

這些資料類型可以用來指定登錄值的型別。



| 常數                                                                                                                                                                                      | 描述                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_BINARY"></span><span id="reg_binary"></span><dl> <dt>**REG \_ 二進位檔**</dt> </dl>                                          | 任何形式的二進位資料，<br/>                                                                                                                                                                                                                                                                                          |
| <span id="REG_DWORD"></span><span id="reg_dword"></span><dl> <dt>**REG \_ DWORD**</dt> </dl>                                             | 32位數位。<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_QWORD"></span><span id="reg_qword"></span><dl> <dt>**REG \_ QWORD**</dt> </dl>                                             | 64位數位。<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_DWORD_LITTLE_ENDIAN"></span><span id="reg_dword_little_endian"></span><dl> <dt>**REG DWORD 位元組由大到 \_ \_ 小 \_**</dt> </dl> | 以位元組由大到小的格式的32位數位。 這相當於 **REG \_ DWORD**。<br/> 以位元組由小到大的格式來說，多位元組值會儲存在最低位元組的記憶體中， (「小端」 ) 到最高的位元組。 例如，值0x12345678 會儲存為 (0x78 0x56 0x34 0x12) 以位元組由小到大格式表示。<br/> |
| <span id="REG_QWORD_LITTLE_ENDIAN"></span><span id="reg_qword_little_endian"></span><dl> <dt>**REG \_ QWORD 位元組由大到 \_ 小 \_**</dt> </dl> | 以位元組由大到小的格式的64位數位。 這相當於 **REG \_ QWORD**。 <br/>                                                                                                                                                                                                                                   |
| <span id="REG_DWORD_BIG_ENDIAN"></span><span id="reg_dword_big_endian"></span><dl> <dt>**REG \_ DWORD \_ BIG \_ ENDIAN**</dt> </dl>          | 以位元組由大到小的格式的32位數位。<br/> 以位元組由大到小的格式，會將多位元組值儲存在記憶體中，從最大的位元組 (「大端」 ) 至最低位元組。 例如，值0x12345678 會以位元組由大到小的格式儲存為 (0x12 0x34 0x56 0x78) 。<br/>                                                   |
| <span id="REG_EXPAND_SZ"></span><span id="reg_expand_sz"></span><dl> <dt>**REG \_ EXPAND \_ SZ**</dt> </dl>                                | 以 Null 終止的字串，其中包含環境變數未展開的參考 (例如 "% PATH%" ) 。 它將會是 Unicode 或 ANSI 字串，取決於您使用的是 Unicode 或 ANSI 函數。<br/>                                                                                                     |
| <span id="REG_LINK"></span><span id="reg_link"></span><dl> <dt>**REG \_ 連結**</dt> </dl>                                                | Unicode 符號連結。<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dl> <dt>**REG \_ 多重 \_ SZ**</dt> </dl>                                   | 以 null 結束的字串陣列，由兩個 null 字元終止。<br/>                                                                                                                                                                                                                                      |
| <span id="REG_NONE"></span><span id="reg_none"></span><dl> <dt>**REG \_ 無**</dt> </dl>                                                | 沒有定義的實值型別。<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_RESOURCE_LIST"></span><span id="reg_resource_list"></span><dl> <dt>**REG \_ 資源 \_ 清單**</dt> </dl>                    | 裝置驅動程式資源清單。<br/>                                                                                                                                                                                                                                                                                      |
| <span id="REG_SZ"></span><span id="reg_sz"></span><dl> <dt>**REG \_ SZ**</dt> </dl>                                                      | 以 Null 結束的字串。 它將會是 Unicode 或 ANSI 字串，取決於您使用的是 Unicode 或 ANSI 函數。<br/>                                                                                                                                                                                          |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Winnt。h</dt> </dl> |



 

 




