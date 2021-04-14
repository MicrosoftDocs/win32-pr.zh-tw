---
description: 判斷 ICoNtextNode 物件是否包含儲存在指定之識別碼下的資料。
ms.assetid: ac3a85a2-abf8-4ac4-8779-d9fda89497d4
title: 'ICoNtextNode：： ContainsPropertyData 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ContainsPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc45e1ebe519e5988ad73e1481c68e9e9811ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469144"
---
# <a name="icontextnodecontainspropertydata-method"></a>ICoNtextNode：： ContainsPropertyData 方法

判斷 [**ICoNtextNode**](icontextnode.md) 物件是否包含儲存在指定之識別碼下的資料。

## <a name="syntax"></a>語法


```C++
HRESULT ContainsPropertyData(
  [in]  const GUID         *pPropertyDataId,
  [out]       VARIANT_BOOL *pbContains
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPropertyDataId* \[在\]
</dt> <dd>

資料的識別碼。

</dd> <dt>

*pbContains* \[擴展\]
</dt> <dd>

**變異 \_** 如果 [**ICoNtextNode**](icontextnode.md)物件包含在指定的識別碼下儲存的資料，則為 TRUE;否則， **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

除了應用程式專屬的資料之外，您也可以使用這個方法來判斷這個 [**ICoNtextNode**](icontextnode.md) 是否包含其他內部資料 (請參閱) 的 [ [分析提示屬性](analysis-hint-properties.md) ] 和 [ [內容節點屬性](context-node-properties.md) ]。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**ICoNtextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**ICoNtextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**ICoNtextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**ICoNtextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**ICoNtextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**ICoNtextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




