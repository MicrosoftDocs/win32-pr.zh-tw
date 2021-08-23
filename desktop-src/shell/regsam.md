---
description: 用來指定登錄中安全性存取屬性的資料類型。
title: 'REGSAM (Winnt. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 003f6be9-e4ba-4d23-b486-a167063c630e
api_name:
- KEY_ALL_ACCESS
- KEY_CREATE_LINK
- KEY_CREATE_SUB_KEY
- KEY_ENUMERATE_SUB_KEYS
- KEY_EXECUTE
- KEY_NOTIFY
- KEY_QUERY_VALUE
- KEY_READ
- KEY_SET_VALUE
- KEY_WRITE
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e202e615561ce0c51f44fc39726d8ab864afc2b5e1bcbbe5612edbb74c476c29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820418"
---
# <a name="regsam"></a>REGSAM

用來指定登錄中安全性存取屬性的資料類型。



| 常數                                                                                                                                                                                   | 描述                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <dt>**金鑰 \_ 所有 \_ 存取權**</dt> </dl>                          | * * * * 索引鍵 \_ 查詢值 * * * *、* * * * 金鑰列舉子機碼 * * * *、* * * * 金鑰通知 * * * *、* * * * * * * * * * * * * * * * * * 金鑰建立連結 * * * * \_ \_ 和 * * * \_ \_ \_ \_ \_ \_ \_ \_ * 金鑰 \_ 集 \_ 值 * * * * 存取的組合。<br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <dt>**金鑰 \_ 建立 \_ 連結**</dt> </dl>                       | 建立符號連結的許可權。<br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <dt>**金鑰 \_ 建立 \_ 子機 \_ 碼**</dt> </dl>             | 建立子機碼的許可權。<br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <dt>**金鑰 \_ 列舉 \_ 子 \_ 機碼**</dt> </dl> | 列舉子機碼的許可權。<br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <dt>**金鑰 \_ 執行**</dt> </dl>                                    | 讀取權限的許可權。<br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <dt>**金鑰 \_ 通知**</dt> </dl>                                       | 變更通知的許可權。<br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <dt>**金鑰 \_ 查詢 \_ 值**</dt> </dl>                       | 查詢子機碼資料的許可權。<br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <dt>**金鑰 \_ 讀取**</dt> </dl>                                             | * * * * 索引鍵 \_ 查詢 \_ 值 * * * *、* * * * 金鑰 \_ 列舉子機碼 * * * * 和 * * * \_ \_ * 金鑰 \_ 通知 * * * * 存取的組合。<br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <dt>**索引鍵 \_ 集 \_ 值**</dt> </dl>                             | 設定子機碼資料的許可權。<br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <dt>**金鑰 \_ 寫入**</dt> </dl>                                          | * * * * KEY \_ SET \_ VALUE * * * * 和 * * * * * * * * * * * * * * * * * * * * * * * * * * * * \_ \_ \_<br/>                                                                                                                |



## <a name="remarks"></a>備註

**REGSAM** 值可以是一個或多個列出的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Winnt。h</dt> </dl> |



 

 




