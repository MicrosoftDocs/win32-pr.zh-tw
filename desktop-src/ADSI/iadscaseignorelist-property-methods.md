---
title: 'IADsCaseIgnoreList 屬性方法 (Iads .h) '
description: IADsCaseIgnoreList 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 4f73adbf-abe3-4552-a3e4-19cff22e0ad0
ms.tgt_platform: multiple
keywords:
- IADsCaseIgnoreList 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsCaseIgnoreList Property Methods
- IADsCaseIgnoreList.CaseIgnoreList
- IADsCaseIgnoreList.get_CaseIgnoreList
- IADsCaseIgnoreList.put_CaseIgnoreList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e2f07d3c4afa6cd55f6a757ccae6f2d1076b954e0afdd0c82c8a5247af33f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961917"
---
# <a name="iadscaseignorelist-property-methods"></a>IADsCaseIgnoreList 屬性方法

[**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**CaseIgnoreList**
</dt> <dd> <dl>

不區分大小寫字串的排序次序。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreList(
  [out] VARIANT* retVal
);
HRESULT put_CaseIgnoreList(
  [in] VARIANT vCaseIgnoreList
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
| IID<br/>                      | IID \_ IADsCaseIgnoreList 定義為7B66B533-4680-11D1-A3B4-00C04FB950DC<br/>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)
</dt> <dt>

[**ADS \_ CASEIGNORE \_ 清單**](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)
</dt> </dl>

 

 





