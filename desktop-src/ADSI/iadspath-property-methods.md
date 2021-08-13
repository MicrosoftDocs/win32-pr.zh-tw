---
title: 'IADsPath 屬性方法 (Iads .h) '
description: IADsPath 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 6fc7ce1a-575b-48c4-9f66-3ea22d60c96b
ms.tgt_platform: multiple
keywords:
- IADsPath 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsPath Property Methods
- IADsPath.Type
- IADsPath.get_Type
- IADsPath.put_Type
- IADsPath.VolumeName
- IADsPath.get_VolumeName
- IADsPath.put_VolumeName
- IADsPath.Path
- IADsPath.get_Path
- IADsPath.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 743410e7ceea97b7066979bf753a4e73afbc8a852b5b36175a9d62109b6d6ef8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691326"
---
# <a name="iadspath-property-methods"></a>IADsPath 屬性方法

[**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath)介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**路徑**
</dt> <dd> <dl>

檔案系統目錄的路徑。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* retval
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

**類型**
</dt> <dd> <dl>

檔案系統的檔案類型。

<dt>

存取類型：讀取/寫入
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
);
```


</dt> </dl> </dd> <dt>

**VolumeName**
</dt> <dd> <dl>

檔案系統現有磁片區的名稱。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_VolumeName(
  [out] BSTR* retval
);
HRESULT put_VolumeName(
  [in] BSTR bstrVolumeName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsPath 定義為 B287FCD5-4080-11D1-A3AC-00C04FB950DC<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath)
</dt> <dt>

[**ADS \_ 路徑**](/windows/win32/api/iads/ns-iads-ads_path)
</dt> </dl>

 

 





