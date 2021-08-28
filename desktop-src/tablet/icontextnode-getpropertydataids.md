---
description: 抓取具有屬性資料的識別碼。
ms.assetid: c9c491b7-95e2-421a-8632-f65844cd5ef9
title: 'ICoNtextNode：： GetPropertyDataIds 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyDataIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 94aab2b91a5da9588de65f5a48bf496bdceae71bf4aa90f82f3969cbe6a9e76e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935368"
---
# <a name="icontextnodegetpropertydataids-method"></a>ICoNtextNode：： GetPropertyDataIds 方法

抓取具有屬性資料的識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetPropertyDataIds(
  [out] ULONG *pulGuidCount,
  [out] GUID  **ppGuids
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pulGuidCount* \[擴展\]
</dt> <dd>

屬性的數目。

</dd> <dt>

*ppGuids* \[擴展\]
</dt> <dd>

具有屬性資料的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *ppGuids* 的記憶體。

 

這個方法會傳回已加入之屬性資料的應用程式特定識別碼。 它也會傳回內部屬性資料的識別碼，此識別碼是由 [內容節點屬性](context-node-properties.md) 常數所描述。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**ICoNtextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**ICoNtextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**ICoNtextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

