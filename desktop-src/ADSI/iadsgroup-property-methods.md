---
title: 'IADsGroup 屬性方法 (Iads .h) '
description: IADsGroup 介面的屬性方法。
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- IADsGroup 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsGroup Property Methods
- IADsGroup.Description
- IADsGroup.get_Description
- IADsGroup.put_Description
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 665cb91a55298012e4e906c2972da5371e3960be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965508"
---
# <a name="iadsgroup-property-methods"></a>IADsGroup 屬性方法

[**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)介面的屬性方法會讀取並寫入下列屬性。 如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**說明**
</dt> <dd> <dl>

指出群組成員資格的文字描述。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>備註

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a>使用 IADsGroup 來取出內建組的描述

下列範例示範如何依名稱抓取 Windows 群組物件的相關資訊。 在多國語言環境中，內建組有時候是由不同的當地語系化名稱所知道，這表示無法使用 "WinNT://Microsoft/Administrators" 之類的字串識別碼直接取出它們。 在這種情況下，使用者可以系結至該群組已知的 SID 物件、取出當地語系化的組名，然後將其提供給 GetObject 方法。 如需詳細資訊，請參閱 [知名的 sid](/windows/desktop/SecAuthZ/well-known-sids)。

## <a name="examples"></a>範例

下列 Visual Basic 範例顯示如何系結至群組物件，並顯示群組的描述。


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Microsoft/Administrators")
Debug.Print grp.Description

Cleanup
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



下列 c + + 範例顯示如何系結至群組物件，並顯示群組的描述。


```C++
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://localHost/Administrators";
BSTR bstr;

hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&pGroup);

if(FAILED(hr)) {goto Cleanup;}

hr = pGroup->get_Description(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Description: %S\n",bstr);

Cleanup:
    SysFreeString(bstr);
    if(pGroup) 
        pGroup->Release();

    return hr;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsGroup 定義為27636B00-410F-11CF-B1FF-02608C9E7553<br/>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[介面屬性方法](interface-property-methods.md)
</dt> </dl>

 

