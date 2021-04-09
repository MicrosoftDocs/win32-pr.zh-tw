---
title: 'glGetError 函式 (Gl) '
description: GlGetError 函數會傳回錯誤資訊。
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- glGetError 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetError
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c0abf6ec03ca0c29ede3b7d396db375fd06ac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934931"
---
# <a name="glgeterror-function"></a>glGetError 函式

**GlGetError** 函數會傳回錯誤資訊。

## <a name="syntax"></a>語法


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

**GlGetError** 函數會傳回下列其中一個錯誤碼。



| 傳回碼                                                                                           | Description                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | 針對列舉引數指定了無法接受的值。 若未設定錯誤旗標，則會忽略有問題的函式，而不會有任何副作用。<br/>         |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | 數值引數超出範圍。 若未設定錯誤旗標，則會忽略有問題的函式，而不會有任何副作用。<br/>                                    |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 目前的狀態不允許指定的作業。 若未設定錯誤旗標，則會忽略有問題的函式，而不會有任何副作用。<br/>           |
| <dl> <dt>**GL \_ 沒有 \_ 錯誤**</dt> </dl>          | 未記錄任何錯誤。 此符號常數的值保證為零。<br/>                                                                         |
| <dl> <dt>**GL \_ 堆疊 \_ 溢位**</dt> </dl>    | 此函數會導致堆疊溢位。 若未設定錯誤旗標，則會忽略有問題的函式，而不會有任何副作用。<br/>                            |
| <dl> <dt>**GL \_ 堆疊 \_ 下溢**</dt> </dl>   | 此函數會導致堆疊下溢。 若未設定錯誤旗標，則會忽略有問題的函式，而不會有任何副作用。<br/>                           |
| <dl> <dt>**GL \_ \_ 記憶體不足 \_**</dt> </dl>    | 沒有足夠的記憶體可執行函式。 在記錄此錯誤之後，不會定義 OpenGL 的狀態，除了錯誤旗標的狀態。<br/> |



 

請注意 ， \_ \_ 如果呼叫 [**GlBegin**](glbegin.md)和其對應的 [**glEnd**](glend.md)呼叫之間呼叫 glGetError，則會傳回 GL 不正確作業。

## <a name="remarks"></a>備註

每個可偵測的錯誤都會被指派一個數位代碼和符號名稱。 發生錯誤時，錯誤旗標會設定為適當的錯誤碼值。 在呼叫 **glGetError** 之前，不會記錄其他錯誤，會傳回錯誤碼，並將旗標重設為 GL \_ 無 \_ 錯誤。 如果呼叫 **glGetError** 時 \_ 未 \_ 發生錯誤，則在上一次呼叫 **GlGetError** 之後，或由於 OpenGL 已初始化，即沒有可偵測的錯誤。

若要允許分散式執行，可能會有數個錯誤旗標。 如果有任何單一錯誤旗標已記錄錯誤，則會傳回該旗標的值，並在呼叫 GlGetError 時，將旗標重設為 GL \_ 無 \_ 錯誤。  如果有一個以上的旗標已記錄錯誤， **glGetError** 會傳回並清除任意錯誤旗標值。 如果要重設所有錯誤旗標，您應該一律在迴圈中呼叫 **glGetError** ，直到它傳回 GL \_ 沒有錯誤為止 \_ 。

一開始，所有錯誤旗標都會設定為 GL \_ 無 \_ 錯誤。

設定錯誤旗標時，只有當 GL 記憶體不足時，才會定義 OpenGL 作業的結果 \_ \_ \_ 。 在所有其他情況下，會忽略產生錯誤的函式，且不會影響 OpenGL 狀態或畫面格緩衝區內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Gl</dt> </dl>         |
| 程式庫<br/>                  | <dl> <dt>Opengl32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





