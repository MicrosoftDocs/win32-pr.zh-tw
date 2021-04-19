---
title: 'IADsMembers 屬性方法 (Iads .h) '
description: IADsMembers 介面的方法會讀取及寫入本主題中所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: ed4e98e5-053c-4d3b-bcd0-3add96bbe120
ms.tgt_platform: multiple
keywords:
- IADsMembers 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsMembers Property Methods
- IADsMembers.Count
- IADsMembers.get_Count
- IADsMembers.Filter
- IADsMembers.get_Filter
- IADsMembers.put_Filter
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af047d6fe52fdd7d808b1d7e5dbfb35303d3ff59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969607"
---
# <a name="iadsmembers-property-methods"></a>IADsMembers 屬性方法

[**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)介面的方法會讀取及寫入本主題中所述的屬性。 如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**Count**
</dt> <dd> <dl>

指出容器中的專案數目。 如果設定篩選準則，則 count 只會傳回符合篩選描述的專案數目。

<dt>

存取類型：唯讀
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCountr
);
```


</dt> </dl> </dd> <dt>

**Filter**
</dt> <dd> <dl>

表示篩選。 篩選陣列中專案的語法與 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 介面上所使用的篩選器相同。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>備註

ADSI 系統提供者不支援 **IADsMembers：： get \_ Count** 屬性方法。

## <a name="examples"></a>範例

下列程式碼範例示範如何使用這個介面的屬性方法。


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://myComputer/someGroup")
grp.members.filter = Array("user")
For Each usr In grp.Members
    MsgBox usr.Name & "," & usr.Class & "," & usr.AdsPath
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



下列程式碼範例使用 **IADsMembers：:p ui \_ 篩選** 方法來準備群組成員集合的列舉。


```C++
IADsGroup *pGroup;
HRESULT hr = S_OK;

LPWSTR grpPath = L"WinNT://myComputer/someGroup";
hr = ADsGetObject(grpPath,IID_IADsGroup,(void**)&pGroup);
if(FAILED(hr)){goto Cleanup;}

IADsMembers *pMembers;
hr = pGroup->Members(&pMembers);
if(FAILED(hr)){goto Cleanup;}

hr = pGroup->Release();

SAFEARRAY *sa = CreateSafeArray(L"user");
hr = pMembers->put_Filter(sa);
if(FAILED(hr)){goto Cleanup;}

hr = EnumMembers(pMembers);    // For more information, and a 
                               // code example, see 
                               // IADsMembers::get__NewEnum.
if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pGroup) pGroup->Release();
    if(pMembers) pMembers->Release();
    return hr;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsMembers 定義為451A0030-72EC-11CF-B03B-00AA006E0975<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[**IADsMembers：： get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum)
</dt> <dt>

[**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)
</dt> <dt>

[介面屬性方法](interface-property-methods.md)
</dt> </dl>

 

 





