---
title: 'IADsPathname 屬性方法 (Iads .h) '
description: 取得或設定 EscapedMode 屬性。
ms.assetid: 007ec617-cff2-492a-a62c-50d65fefcd3b
ms.tgt_platform: multiple
keywords:
- IADsPathname 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsPathname Property Methods
- IADsPathname.EscapedMode
- IADsPathname.get_EscapedMode
- IADsPathname.get_EscapedMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11d3321d58065d890d864ed967a4e6a66dad22cde2cc234b5907afab74986898
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023426"
---
# <a name="iadspathname-property-methods"></a>IADsPathname 屬性方法

[**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname)介面的屬性方法會取得或設定 **EscapedMode** 屬性。 如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**EscapedMode**
</dt> <dd> <dl>

檢查或指定在路徑名稱中處理逸出字元的方式。 如需詳細資訊和定義的選項，請參閱 [**ADS \_ ESCAPE \_ 模式 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)。

<dt>

存取類型：讀取/寫入
</dt> <dt>

編寫資料類型的腳本： **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EscapedMode(
  [out] long* retval
);
HRESULT get_EscapedMode(
  [in] long* lnEscapedMode
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>備註

**EscapedMode** 代表狀態。 您可以開啟或關閉它，方法是將它設定為 \_ ESCAPEDMODE \_ ON 或 ads \_ ESCAPEDMODE \_ off/ADS \_ ESCAPEDMODE \_ off/ads \_ 的廣告。 開啟或關閉時，所有後續的檢索都會產生轉義或非轉義的路徑字串。

在 ADSI 中，只有 [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) 能夠未逸出路徑。 所有其他 ADSI 介面一律會傳回已轉義的路徑。 **EscapedMode** 的預設狀態是 ads \_ EscapedMode \_ 預設值，如 [**ads \_ ESCAPE \_ 模式 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)中所定義。

## <a name="examples"></a>範例

下列程式碼範例示範如何使用 **EscapedMode** 屬性，將下列三個特殊字元的轉換開啟/關閉： "="、"、" 和 "/"。


```VB
Dim path As New Pathname
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All escaped, producing:
                                          ' "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' Only "/" is unescaped:
                                          ' "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
```



下列程式碼範例示範如何使用 **EscapedMode** 屬性，將下列三個特殊字元的轉換開啟/關閉： "="、"、" 和 "/"。


```VB
<%
Dim path
const ADS_SETTYPE_FULL = 1
const ADS_SETTYPE_DN   = 4
const ADS_FORMAT_WINDOWS = 1
const ADS_ESCAPEDMODE_ON = 2
const ADS_ESCAPEDMODE_OFF = 3
const ADS_ESCAPEDMODE_OFF_EX = 4
 
Set path = CreateObject("Pathname")
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' All escaped, producing:  "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' Only "/" is unescaped: "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
%>
```



下列程式碼範例顯示如何使用 **EscapedMode** 屬性。 忽略錯誤檢查。


```C++
IADsPathname *pPathname=NULL;
HRESULT hr;
 
hr = CoCreateInstance(CLSID_Pathname,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsPathname,
                      (void**)&pPathname);
 
if(FAILED(hr)) 
{
    if(pPathname) pPathname->Release();
    return NULL;
}
 
pPathname->AddRef();
hr = pPathname->Set(CComBSTR("LDAP://CN=joy/ful\/*"), 
                    ADS_SETTYPE_FULL); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy/ful\/*"

SysFreeString(bstr);
 
// Set the path using ADS_SETTYPE_DN
 
hr = pPathname->Set(CComBSTR("CN=joy/ful\/*"), ADS_SETTYPE_DN); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy\/ful\/*"

SysFreeString(bstr);
 
hr = pPathname->Release();
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsPathname 定義為 D592AED4-F420-11D0-A36E-00C04FB950DC<br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname)
</dt> <dt>

[**ADS \_ ESCAPE \_ 模式 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)
</dt> </dl>

 

 





