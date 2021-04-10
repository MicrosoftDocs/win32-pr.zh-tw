---
description: VARIANT 類型變數有一個類型標記欄位 vt，表示資料的資料類型。
ms.assetid: 3436faf6-2e66-46a1-b1e8-84f513282c16
title: 設定類型標記欄位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e443fae33b14bd4270e63188ff96a042a91c8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191115"
---
# <a name="setting-the-type-tag-field"></a>設定類型標記欄位

**VARIANT** 類型變數有一個類型標記欄位 **vt** ，表示資料的資料類型。 **VARIANT** 型別傳回值是由將 type tag 欄位設定為傳回值資料類型的方法所傳回。 方法呼叫中的 **VARIANT** 類型輸入參數必須將應用程式所設定的類型標記欄位設定為其中一個支援的值。 參數類型與資料類型的對應如下所示。



| 參數類型              | 資料類型                                      |
|-----------------------------|------------------------------------------------|
| PROPTYPE \_ LONG<br/>   | VT \_ I2 或 vt \_ I4<br/>                    |
| PROPTYPE \_ 日期<br/>   | VT \_ 日期<br/>                            |
| PROPTYPE \_ 二進位檔<br/> | VT \_ bstr 或 (vt \_ bstr \| VT \_ BYREF) <br/> |
| PROPTYPE \_ 字串<br/> | VT \_ bstr 或 (vt \_ bstr \| VT \_ BYREF) <br/> |



 

下列範例示範如何初始化上述的 variant 資料類型。


```C++
HRESULT hr;
VARIANT vEMail;
VARIANT vNotBefore;
VARIANT vCount;
VARIANT vByRef;
BSTR bstr = NULL;
SYSTEMTIME st;

//Set the BSTR variant data type.
VariantInit(&vEMail);
vEMail.vt = VT_BSTR;   
vEMail.bstrVal = SysAllocString(L"someone@example.com");
if (NULL == vEMail.bstrVal)
{
    hr = E_OUTOFMEMORY;
    //Handle error.   
}
//Use the variant.
VariantClear(&vEMail);  //when done


//Set the BSTR|BYREF variant data type.
VariantInit(&vByRef);
vByRef.vt = VT_BSTR | VT_BYREF;   
vByRef.pbstrVal = &bstr;
//Use the variant.
VariantClear(&vByRef);  //when done
SysFreeString(bstr);


//Set the DATE variant data type.
memset(&st, 0, sizeof(SYSTEMTIME));
st.wYear = 2000;
st.wMonth = 1;
st.wDay = 1;
st.wHour = 12;

VariantInit(&vNotBefore);
vNotBefore.vt = VT_DATE;
if (!SystemTimeToVariantTime(&st, &vNotBefore.date))
{
    hr = E_FAIL;
    //Handle error.
}
//Use the variant.
VariantClear(&vNotBefore);  //when done


//Set the LONG variant data type.
VariantInit(&vCount);
vCount.vt = VT_I4;
vCount.long = 123456;
//Use the variant.
VariantClear(&vCount);  //when done
```



 

 




