---
title: 'IADsLargeInteger 屬性方法 (Iads .h) '
description: IADsLargeInteger 介面的屬性方法會取得並設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 73e0c7fe-e468-4f92-9c9e-721bf00dd4bb
ms.tgt_platform: multiple
keywords:
- IADsLargeInteger 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsLargeInteger Property Methods
- IADsLargeInteger.HighPart
- IADsLargeInteger.get_HighPart
- IADsLargeInteger.put_HighPart
- IADsLargeInteger.LowPart
- IADsLargeInteger.get_LowPart
- IADsLargeInteger.put_LowPart
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b46a992accea468b6f3c8a70c7fcfcbe63cf72667c4394c27df273767a387b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023476"
---
# <a name="iadslargeinteger-property-methods"></a>IADsLargeInteger 屬性方法

[**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)介面的屬性方法會取得並設定下表所述的屬性。 如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**HighPart**
</dt> <dd> <dl>

整數的高部分。

<dt>

存取類型：讀取/寫入
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HighPart(
  [out] LONG* retval
);
HRESULT put_HighPart(
  [in] LONG lnHighPart
);
```


</dt> </dl> </dd> <dt>

**LowPart**
</dt> <dd> <dl>

整數的低部分。

<dt>

存取類型：讀取/寫入
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LowPart(
  [out] LONG* retval
);
HRESULT put_LowPart(
  [in] LONG lnLowPart
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>備註

如果 largeInt 是 **LargeInteger** 類型，則會根據下列公式，為 **HighPart** 和 **LowPart** 的值指定其值。


```VB
largeInt = HighPart * 2^32 + LowPart
```



## <a name="examples"></a>範例

下列 Visual Basic 程式碼範例會將大型整數設定為43937327281。


```VB
Dim LI As New LargeInteger
LI.HighPart = 10
LI.LowPart = 987654321
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsLargeInteger 定義為9068270B-0939-11D1-8BE1-00C04FD8D503<br/>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)
</dt> </dl>

 

 





