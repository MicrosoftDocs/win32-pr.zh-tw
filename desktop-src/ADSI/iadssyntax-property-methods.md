---
title: 'IADsSyntax 屬性方法 (Iads .h) '
description: IADsSyntax 介面的屬性方法會取得或設定下表所列的屬性。 如需屬性方法的詳細資訊，請參閱介面屬性方法。
ms.assetid: a216a55d-63eb-4fdf-a67f-8d4b5eb74262
ms.tgt_platform: multiple
keywords:
- IADsSyntax 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsSyntax Property Methods
- IADsSyntax.OleAutoDataType
- IADsSyntax.get_OleAutoDataType
- IADsSyntax.put_OleAutoDataType
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c193bba78bfe215d37bdfdedf5d45bd73f1a85606b3dab6e5a3c233cece8db18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961897"
---
# <a name="iadssyntax-property-methods"></a>IADsSyntax 屬性方法

[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)介面的屬性方法會取得或設定下表所列的屬性。 如需屬性方法的詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**OleAutoDataType**
</dt> <dd> <dl>

抓取並設定 **LONG** ，其包含表示此語法之 Automation 資料類型的 **VT \_ xxx** 常數值。

Active Directory 針對表示此語法的 Automation 資料類型支援下列 **VT \_ xxx** 常數：

-   **VT \_BOOL** BOOL
-   **VT \_BSTR** BSTR
-   **VT \_BSTRT** BSTRT
-   **VT \_CY** 貨幣
-   **VT \_日期** 日期
-   **VT \_空白** **Null**
-   **VT \_錯誤** 無效
-   **VT \_I2** 簡短
-   **VT \_I4** long
-   **VT \_R4** real
-   **VT \_R8** double
-   **VT \_UI1** 位元組

<dt>

存取類型：讀取/寫入
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OleAutoDataType(
  [out] LONG* plAutoDataType
);
HRESULT put_OleAutoDataType(
  [in] LONG lAutoDataType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>備註

不帶正負號的位元組陣列， **vt \_ UI1** \| **vt \_ array** 可能表示提供者已對應無法對應至 Automation 虛擬類型的語法。

## <a name="examples"></a>範例

下列程式碼範例會透過 WinNT 提供者，檢查網路上電腦的 **OperatingSystemVersion** 屬性語法。 結果語法為字串。


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sy As IADsSyntax
Dim sc As IADsContainer
On Error GoTo Cleanup

Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystemVersion")
Set sy = GetObject(sc.ADsPath & "/" & pr.Syntax)
 
MsgBox "Automation data types: " & sy.OleAutoDataType

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sy = Nothing
    Set sc = Nothing
```



下列程式碼範例會透過 WinNT 提供者，檢查網路上電腦的 **OperatingSystemVersion** 屬性語法。 結果語法為字串。 為了簡潔起見，會忽略錯誤檢查。


```C++
#include <stdio.h>
#include <activeds.h>
#include <atlbase.h>
 
IADs *pObj = NULL;
IADsClass *pCls = NULL;
IADsProperty *pProp = NULL;
IADsSyntax *pSyn = NULL;
IADsContainer *pCont = NULL;
 
HRESULT hr = ADsGetObject(L"WinNT://myMachine,computer",
                          IID_IADs,
                          (void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
VARIANT var;
VariantInit(&var);
CComBSTR sbstr;
 
pObj->get_Schema(&sbstr);
printf("Object schema: %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsClass,(void**)&pCls);
if(FAILED(hr)){goto Cleanup;}

pCls->get_Parent(&sbstr);
printf("Object class's container:  %S\n", sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr)){goto Cleanup;}
pCont->QueryInterface(IID_IADs,(void**)&pObj);
pObj->get_ADsPath(&sbstr);
printf("Container's AdsPath:  %S\n",sbstr);
 
IDispatch *pDisp;
hr = pCont->GetObject(CComBSTR("Property"),
                      CComBSTR("OperatingSystemVersion"),
                      (IDispatch**)&pDisp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pDisp->QueryInterface(IID_IADsProperty, (void**)&pProp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pProp->get_Syntax(&sbstr);
if(FAILED(hr)){goto Cleanup;}
printf("Property Syntax:  %S\n",sbstr);
 
printf("ADsPath of the syntax object %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsSyntax, (void**)&pSyn);
if(FAILED(hr)){goto Cleanup;}

long lType;
pSyn->get_OleAutoDataType(&lType);
printf("Property syntax's OleAutoDataType: %d\n", lType);

Cleanup:
    if(pObj)
        pObj->Release();

    if(pProp)
        pProp->Release();

    if(pCls)
        pCls->Release();

    if(pSyn)
        pSyn->Release();

    if(pCont)
        pCont->Release();
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsSyntax 定義為 C8F93DD2-4AE0-11CF-9E73-00AA004A5691<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





