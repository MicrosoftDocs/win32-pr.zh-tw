---
title: '得到 iadsclass 屬性方法 (Iads .h) '
description: 得到 iadsclass 介面的屬性方法會取得或設定下列屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 191f6873-c4bd-4e71-9d23-478454b7cec2
ms.tgt_platform: multiple
keywords:
- 得到 iadsclass 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsClass Property Methods
- IADsClass.Abstract
- IADsClass.get_Abstract
- IADsClass.put_Abstract
- IADsClass.AuxDerivedFrom
- IADsClass.get_AuxDerivedFrom
- IADsClass.put_AuxDerivedFrom
- IADsClass.Auxiliary
- IADsClass.get_Auxiliary
- IADsClass.put_Auxiliary
- IADsClass.CLSID
- IADsClass.get_CLSID
- IADsClass.put_CLSID
- IADsClass.Container
- IADsClass.get_Container
- IADsClass.put_Container
- IADsClass.Containment
- IADsClass.get_Containment
- IADsClass.put_Containment
- IADsClass.DerivedFrom
- IADsClass.get_DerivedFrom
- IADsClass.put_DerivedFrom
- IADsClass.HelpFileContext
- IADsClass.get_HelpFileContext
- IADsClass.put_HelpFileContext
- IADsClass.HelpFileName
- IADsClass.get_HelpFileName
- IADsClass.put_HelpFileName
- IADsClass.MandatoryProperties
- IADsClass.get_MandatoryProperties
- IADsClass.put_MandatoryProperties
- IADsClass.NamingProperties
- IADsClass.get_NamingProperties
- IADsClass.put_NamingProperties
- IADsClass.OID
- IADsClass.get_OID
- IADsClass.put_OID
- IADsClass.OptionalProperties
- IADsClass.get_OptionalProperties
- IADsClass.put_OptionalProperties
- IADsClass.PossibleSuperiors
- IADsClass.get_PossibleSuperiors
- IADsClass.put_PossibleSuperiors
- IADsClass.PrimaryInterface
- IADsClass.get_PrimaryInterface
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358bc33347f035af92303a4ce9879105cd247a3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105155"
---
# <a name="iadsclass-property-methods"></a>得到 iadsclass 屬性方法

[**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)介面的屬性方法會取得或設定下列屬性。 如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**摘要**
</dt> <dd> <dl>

指出此類別為抽象或非抽象的布林值。 當 **為 TRUE** 時，這個類別是抽象類別，無法在目錄服務中直接具現化。 抽象類別只能用來做為超級類別。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **布林值**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Abstract(
  [out] BOOLEAN* pbAbstract
);
HRESULT put_Abstract(
  [in] BOOLEAN bAbstract
);
```


</dt> </dl> </dd> <dt>

**AuxDerivedFrom**
</dt> <dd> <dl>

ADsPath 字串的陣列，表示此類別衍生自的超級輔助類別。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AuxDerivedFrom(
  [out] VARIANT* pvAuxDerivedFrom
);
HRESULT put_AuxDerivedFrom(
  [in] VARIANT vAuxDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**輔助**
</dt> <dd> <dl>

指出此類別是否為輔助的布林值。 當 **為 TRUE** 時，這個類別是輔助類別，無法在目錄服務中直接具現化。 輔助類別只能用來做為其他輔助類別的超級類別，或是結構類別上其他屬性的來源。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **布林值**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Auxiliary(
  [out] BOOLEAN* pbAuxiliary
);
HRESULT put_Auxiliary(
  [in] BOOLEAN bAuxiliary
);
```


</dt> </dl> </dd> <dt>

**Clsid**
</dt> <dd> <dl>

選擇性的提供者特定 CLSID，識別可執行此類別的 COM 物件。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CLSID(
  [out] BSTR* pbstrCLSID
);
HRESULT put_CLSID(
  [in] BSTR bstrCLSID
);
```


</dt> </dl> </dd> <dt>

**容器**
</dt> <dd> <dl>

指出此類別是否可以是其他物件類別之容器的布林值。 如果這個值為 **TRUE**，您可以呼叫 **get \_ 容器** 方法，以取得這個類別可包含的物件類別陣列。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **布林值**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Container(
  [out] BOOLEAN* pbContainer
);
HRESULT put_Container(
  [in] BOOLEAN bContainer
);
```


</dt> </dl> </dd> <dt>

**遏制**
</dt> <dd> <dl>

**BSTR** 陣列，其中每個元素都是這個類別可包含的物件類別名稱。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Containment(
  [out] VARIANT* pvContainment
);
HRESULT put_Containment(
  [in] VARIANT vContainment
);
```


</dt> </dl> </dd> <dt>

**DerivedFrom**
</dt> <dd> <dl>

ADsPath 字串的陣列，表示此類別衍生自哪些類別。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DerivedFrom(
  [out] VARIANT* pvDerivedFrom
);
HRESULT put_DerivedFrom(
  [in] VARIANT vDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**HelpFileCoNtext**
</dt> <dd> <dl>

**HelpFileName** 內的內容識別碼，可以找到這個類別的特定資訊。

<dt>

存取類型：讀取/寫入
</dt> <dt>

編寫資料類型的腳本： **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileContext(
  [out] long* plHelpContext
);
HRESULT put_HelpFileContext(
  [in] long lHelpContext
);
```


</dt> </dl> </dd> <dt>

**HelpFileName**
</dt> <dd> <dl>

包含此類別物件之詳細資訊的說明檔名稱。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileName(
  [out] BSTR* pbstrHelpFileName
);
HRESULT put_HelpFileName(
  [in] BSTR bstrHelpFileName
);
```


</dt> </dl> </dd> <dt>

**MandatoryProperties**
</dt> <dd> <dl>

**VARIANT** 的 **SAFEARRAY** ，其中列出必須設定才能將此類別寫入至儲存體的屬性。 如果類別只包含一個屬性，則 **get \_ MandatoryProperties** 會傳回 **BSTR**。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MandatoryProperties(
  [out] VARIANT* pvarMandatoryProperties
);
HRESULT put_MandatoryProperties(
  [in] VARIANT varMandatoryProperties
);
```


</dt> </dl> </dd> <dt>

**NamingProperties**
</dt> <dd> <dl>

**BSTR** 的 **SAFEARRAY** ，列出用來命名這個架構類別之屬性的屬性。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamingProperties(
  [out] VARIANT* pvarNamingProperties
);
HRESULT put_NamingProperties(
  [in] VARIANT varNamingProperties
);
```


</dt> </dl> </dd> <dt>

**老**
</dt> <dd> <dl>

定義此類別的提供者特定物件識別碼。 這是為了在需要類別的提供者特定 Oid 的目錄服務中，使用 Active Directory 來允許架構延伸。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* pbstrOID
);
HRESULT put_OID(
  [in] BSTR bstrOID
);
```


</dt> </dl> </dd> <dt>

**OptionalProperties**
</dt> <dd> <dl>

**VARIANT** 的 **SAFEARRAY** ，列出此架構類別的選擇性屬性。 如果類別只包含一個屬性，則 **get \_ OptionalProperties** 會傳回 **BSTR**。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OptionalProperties(
  [out] VARIANT* pvarOptionalProperties
);
HRESULT put_OptionalProperties(
  [in] VARIANT varOptionalProperties
);
```


</dt> </dl> </dd> <dt>

**PossibleSuperiors**
</dt> <dd> <dl>

ADsPath 字串的陣列，表示可以包含這個類別之實例的架構類別。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PossibleSuperiors(
  [out] VARIANT* pvSuperiors
);
HRESULT put_PossibleSuperiors(
  [in] VARIANT vSuperiors
);
```


</dt> </dl> </dd> <dt>

**PrimaryInterface**
</dt> <dd> <dl>

選擇性的提供者特定識別碼 GUID，可將介面與此架構類別的物件產生關聯。 例如，支援 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) 和 **PrimaryInterface** 的 "User" 類別是由 **IID \_ IADsUser** 所識別。 這必須是由 COM 定義的 GUID 標準字串格式。 此 GUID 是在這個類別的實例中，出現在 [**IADs：： get \_ GUID**](/windows/desktop/api/Iads/nn-iads-iads) 屬性中的值，可供執行這個屬性的提供者。 依類別程式碼主要介面的 IID 來識別架構類別，可讓您在執行時間使用 **QueryInterface** 來判斷物件是否為所需的類別。

<dt>

存取類型：唯讀
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryInterface(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>範例

下列程式碼範例示範如何使用 [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) 介面判斷物件是否可以是容器，如果是，則會列出任何包含物件的名稱。


```VB
Dim ads As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(ads.Schema)
if cls.Container = True Then
    MsgBox "This object contains the following children:"
    For Each o In cls.Containment
        MsgBox o
    Next
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
```



下列程式碼範例示範如何使用 [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) 介面判斷物件是否可以是容器，如果是，則會列出任何包含物件的名稱。


```C++
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs = NULL;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) {goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) {goto Cleanup;}
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) {goto Cleanup;}
 
VariantInit(&var);
VARIANT_BOOL bCont;
pCls->get_Container(&bCont);
if(bCont != false) {
    VariantClear(&var);
    pCls->get_Containment(&var);
    hr = printVarArray(var);
}

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    SysFreeString(bstrSchema);
    CoUninitialize();
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ 得到 iadsclass 定義為 C8F93DD0-4AE0-11CF-9E73-00AA004A5691<br/>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**得到 iadsclass：：限定詞**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers)
</dt> </dl>

 

 





