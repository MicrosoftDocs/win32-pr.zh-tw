---
description: 針對先前使用 ICoNtextNode：： SavePropertiesData 建立的位元組陣列，重新建立應用程式特定和內部屬性資料。
ms.assetid: 2d24d0da-16f1-4ddc-8e2e-93c312ecfa42
title: 'ICoNtextNode：： LoadPropertiesData 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.LoadPropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc495aaa52ebfbca088f954b34f22f9d6e1e53d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971229"
---
# <a name="icontextnodeloadpropertiesdata-method"></a>ICoNtextNode：： LoadPropertiesData 方法

針對先前使用 [**ICoNtextNode：： SavePropertiesData**](icontextnode-savepropertiesdata.md)建立的位元組陣列，重新建立應用程式特定和內部屬性資料。

## <a name="syntax"></a>語法


```C++
HRESULT LoadPropertiesData(
  [in]  ULONG        cbPropertiesDataSize,
  [in]  BYTE         *pbPropertiesData,
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cbPropertiesDataSize* \[在\]
</dt> <dd>

屬性資料陣列的大小。

</dd> <dt>

*pbPropertiesData* \[在\]
</dt> <dd>

8位不帶正負號的整數陣列，包含要載入的屬性資訊。

</dd> <dt>

*pfSuccessful* \[擴展\]
</dt> <dd>

**變異 \_** 如果成功載入屬性資料，則為 TRUE;否則， **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

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

[**ICoNtextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**ICoNtextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**ICoNtextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**ICoNtextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**ICoNtextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




