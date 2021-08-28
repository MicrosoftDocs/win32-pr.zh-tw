---
title: 'IADsNamespaces 屬性方法 (Iads .h) '
description: IADsNamespaces 介面屬性方法會取得並設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- IADsNamespaces 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsNamespaces Property Methods
- IADsNamespaces.DefaultContainer
- IADsNamespaces.get_DefaultContainer
- IADsNamespaces.put_DefaultContainer
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8daeed67202add437ee06b9905cbd70a0c202863c476155216f2340be1c7b70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691426"
---
# <a name="iadsnamespaces-property-methods"></a>IADsNamespaces 屬性方法

[**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)介面屬性方法會取得並設定下表所述的屬性。 如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**DefaultContainer**
</dt> <dd> <dl>

**DefaultContainer** 屬性會識別基底容器物件，您可以在流覽時將其系結至起點作為起點。 這項資料會從下列登錄值儲存和取出。

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

ADSI 定義了 **DefaultContainer** 屬性，以提供快速的方式來取得先前定義之 ADSI 容器物件的指標。

<dt>

存取類型：讀取/寫入
</dt> <dt>

腳本資料類型： **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultContainer(
  [out] BSTR* pbstrDefault
);
HRESULT put_DefaultContainer(
  [in] BSTR bstrDefault
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>備註

提供者必須以每個使用者為基礎來提供此屬性。 預設容器會在 IADsNamespaces 的調用之後立即設定 **：:p 的 \_ DefaultContainer**。 不需要呼叫 [**IADs。 SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 。 事實上，系統提供的命名空間物件會傳回這個物件上所呼叫之 **IADs. SetInfo** 方法的 **E \_ >notimpl** 。 當容器是命名空間物件時，列舉作業一律會產生提供者專屬命名空間物件的清單。 當使用 [**IADsContainer**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) 來取得 namespace 物件時，會忽略 *bstrClass* 參數。 這是因為容器（也就是命名空間物件）只包含一種類型的物件，也就是提供者特定的命名空間物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsNamespaces 定義為28B96BA0-B330-11CF-A9AD-00AA006BC149<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[介面屬性方法](interface-property-methods.md)
</dt> </dl>

 

 





