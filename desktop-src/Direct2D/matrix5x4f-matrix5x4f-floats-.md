---
title: 'Matrix5x4F Matrix5x4F (浮點數、浮點數、浮點數、浮點數、浮點數、浮點數、浮點數、浮點數、浮點數、浮點數、浮點數、浮點數、浮點數、浮點數、浮點數、浮點數、浮點數、浮點數、浮點數)  (D2d1 \_ helper. h) '
description: 具現化 Matrix5x4F 類別的新實例，這個實例會使用所有浮點數矩陣值進行初始化。
ms.assetid: 46C2741F-9E49-4ABD-9DA5-D4E6D3CA2B09
keywords:
- Matrix5x4F 函式 Direct2D
- Matrix5x4F 函式 Direct2D、Matrix5x4F 介面
- Matrix5x4F 介面 Direct2D、Matrix5x4F 函式
topic_type:
- apiref
api_name:
- Matrix5x4F.Matrix5x4F
api_location:
- D2d1.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2582e58f535ddf4f87d54e16dd2edaec2aa37e91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106979697"
---
# <a name="matrix5x4fmatrix5x4ffloat-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-constructor"></a>Matrix5x4F：： Matrix5x4F (FLOAT，float，float，float，FLOAT，FLOAT，FLOAT，FLOAT，float，float，float，float，float，float，float，float，FLOAT，float，float，FLOAT) 函數

具現化 [**Matrix5x4F**](matrix5x4f.md) 類別的新實例，這個實例會使用所有浮點數矩陣值進行初始化。

## <a name="syntax"></a>語法


```C++
inline Matrix5x4F(
   FLOAT m11,
   FLOAT m12,
   FLOAT m13,
   FLOAT m14,
   FLOAT m21,
   FLOAT m22,
   FLOAT m23,
   FLOAT m24,
   FLOAT m31,
   FLOAT m32,
   FLOAT m33,
   FLOAT m34,
   FLOAT m41,
   FLOAT m42,
   FLOAT m43,
   FLOAT m44,
   FLOAT m51,
   FLOAT m52,
   FLOAT m53,
   FLOAT m54
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*m11* 
</dt> <dd>

類型： **FLOAT**

矩陣第一個資料列和第一個資料行中的值。

</dd> <dt>

*m12* 
</dt> <dd>

類型： **FLOAT**

矩陣的第一個資料列和第二個數據行中的值。

</dd> <dt>

*m13* 
</dt> <dd>

類型： **FLOAT**

矩陣的第一個資料列和第三個數據行中的值。

</dd> <dt>

*m14* 
</dt> <dd>

類型： **FLOAT**

矩陣的第一個資料列和第四個數據行中的值。

</dd> <dt>

*m21* 
</dt> <dd>

類型： **FLOAT**

矩陣第二列和第一個資料行中的值。

</dd> <dt>

*m22* 
</dt> <dd>

類型： **FLOAT**

矩陣的第二個數據列和第二個數據行中的值。

</dd> <dt>

*m23* 
</dt> <dd>

類型： **FLOAT**

矩陣的第二個數據列和第三個數據行中的值。

</dd> <dt>

*m24* 
</dt> <dd>

類型： **FLOAT**

矩陣的第二個數據列和第四個數據行中的值。

</dd> <dt>

*m31* 
</dt> <dd>

類型： **FLOAT**

矩陣第三列第一個資料行中的值。

</dd> <dt>

*m32* 
</dt> <dd>

類型： **FLOAT**

矩陣第三列第二行的值。

</dd> <dt>

*m33* 
</dt> <dd>

類型： **FLOAT**

矩陣第三列和第三個數據行中的值。

</dd> <dt>

*m34* 
</dt> <dd>

類型： **FLOAT**

矩陣的第三列第四個數據行中的值。

</dd> <dt>

*m41* 
</dt> <dd>

類型： **FLOAT**

矩陣第四個數據列和第一個資料行中的值。

</dd> <dt>

*m42* 
</dt> <dd>

類型： **FLOAT**

矩陣的第四個數據列和第二個數據行中的值。

</dd> <dt>

*m43* 
</dt> <dd>

類型： **FLOAT**

矩陣的第四個數據列和第三個數據行中的值。

</dd> <dt>

*m44* 
</dt> <dd>

類型： **FLOAT**

矩陣的第四個數據列和第四個數據行中的值。

</dd> <dt>

*m51* 
</dt> <dd>

類型： **FLOAT**

矩陣第五個數據列和第一個資料行中的值。

</dd> <dt>

*m52* 
</dt> <dd>

類型： **FLOAT**

矩陣第五個數據列和第二個數據行中的值。

</dd> <dt>

*m53* 
</dt> <dd>

類型： **FLOAT**

矩陣第五個數據列和第三個數據行中的值。

</dd> <dt>

*m54* 
</dt> <dd>

類型： **FLOAT**

矩陣第五個數據列和第四個數據行中的值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7、windows Vista （含 SP2）和平臺更新（僅適用于 Windows Vista \[ desktop 應用程式）\]<br/>                          |
| 最低支援的伺服器<br/> | Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新（僅適用于 Windows Server 2008 \[ desktop 應用程式）\]<br/> |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/>                                           |
| 命名空間<br/>                | D2D1<br/>                                                                                                                   |
| 標頭<br/>                   | <dl> <dt>D2d1 \_ helper。h</dt> </dl>                                         |
| 程式庫<br/>                  | <dl> <dt>D2d1 .lib</dt> </dl>                                               |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Matrix5x4F**](matrix5x4f.md)
</dt> </dl>

 

 





