---
title: 'glListBase 函式 (Gl) '
description: GlListBase 函數會設定 glCallLists 的顯示清單基底。
ms.assetid: df82f699-b2af-471a-83f3-5620857ba45d
keywords:
- glListBase 函式 OpenGL
topic_type:
- apiref
api_name:
- glListBase
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ba7cbe7b179184efa739ac3492f4e74b36f56abe0f02498a0e1a688b85183a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938515"
---
# <a name="gllistbase-function"></a>glListBase 函式

**GlListBase** 函數會設定 **glCallLists** 的顯示清單基底。

## <a name="syntax"></a>語法


```C++
void WINAPI glListBase(
   GLuint base
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*base* 
</dt> <dd>

將加入至 [**glCallLists**](glcalllists.md) 位移以產生顯示清單名稱的整數位移。 初始值為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlListBase** 函數會指定位移的陣列。 顯示清單名稱是藉由將 *基底* 加入至每個位移來產生。 執行參考有效顯示清單的名稱;其他則會被忽略。

下列函式會抓取 **glListBase** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 清單 \_ 基底的 glGet

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

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





