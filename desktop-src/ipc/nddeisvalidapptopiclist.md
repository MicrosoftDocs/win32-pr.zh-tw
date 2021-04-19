---
description: 判斷應用程式和主題字串是否 (&\# 0034;AppName \| TopicName&\# 0034; ) 使用適當的語法。
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: 'NDdeIsValidAppTopicList 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidAppTopicList
- NDdeIsValidAppTopicListA
- NDdeIsValidAppTopicListW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: fb990830583f6684502438f132c1c98f5741a0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996931"
---
# <a name="nddeisvalidapptopiclist-function"></a>NDdeIsValidAppTopicList 函式

\[不再支援網路 DDE。 Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]

判斷應用程式和主題字串 ( "*AppName* \| *TopicName*" ) 是否使用適當的語法。

## <a name="syntax"></a>語法


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*targetTopic* \[在\]
</dt> <dd>

要驗證之應用程式和主題字串的指標。 此參數不可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 *targetTopic* 參數的語法有效，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

[**NDdeShareAdd**](nddeshareadd.md)在建立 DDE 共用時，也會呼叫這個函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                      |
| 標頭<br/>                   | <dl> <dt>Nddeapi。h</dt> </dl>      |
| 程式庫<br/>                  | <dl> <dt>Nddeapi .lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl>    |
| Unicode 與 ANSI 名稱<br/>   | **NDdeIsValidAppTopicListW** (Unicode) 和 **NDdeIsValidAppTopicListA** (ANSI) <br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網路動態資料交換總覽](network-dynamic-data-exchange.md)
</dt> <dt>

[網路 DDE 函數](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




