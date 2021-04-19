---
title: 'glDeleteLists 函式 (Gl) '
description: GlDeleteLists 函式會刪除連續的顯示清單群組。
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- glDeleteLists 函式 OpenGL
topic_type:
- apiref
api_name:
- glDeleteLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11ae41273cba5bd050a62ea330cef9da0647769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106998014"
---
# <a name="gldeletelists-function"></a>glDeleteLists 函式

**GlDeleteLists** 函式會刪除連續的顯示清單群組。

## <a name="syntax"></a>語法


```C++
void WINAPI glDeleteLists(
   GLuint  list,
   GLsizei range
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*list* 
</dt> <dd>

要刪除的第一個顯示清單的整數名稱。

</dd> <dt>

*range* 
</dt> <dd>

要刪除的顯示清單數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *範圍* 為負數。<br/>                                                                                                      |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlDeleteLists** 函式會刪除連續的顯示清單群組。 *清單* 參數是要刪除之第一個顯示清單的名稱，而 *範圍* 是要刪除的顯示清單數目。 系統會刪除 *清單*  =  *d*  =  *清單*  +  *範圍*-1 的所有顯示清單 d。

配置給指定之顯示清單的所有儲存位置會釋出，且名稱可供稍後重複使用。 系統會忽略範圍內沒有相關聯顯示清單的名稱。 如果 *範圍* 為零，則不會發生任何事。

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





