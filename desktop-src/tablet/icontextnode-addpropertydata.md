---
description: 新增應用程式特定資料的片段。
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: 'ICoNtextNode：： AddPropertyData 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8c9988217aed21ff1142f0e2083bee568ed12c31d90530ac1f3e9f5719c46446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719692"
---
# <a name="icontextnodeaddpropertydata-method"></a>ICoNtextNode：： AddPropertyData 方法

新增應用程式特定資料的片段。

## <a name="syntax"></a>語法


```C++
HRESULT AddPropertyData(
  [in] const GUID  *pPropertyDataId,
  [in]       ULONG ulPropertyDataSize,
  [in]       BYTE  *pbPropertiesData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPropertyDataId* \[在\]
</dt> <dd>

 (GUID) 的全域唯一識別碼，用來識別資料的類型。

</dd> <dt>

*ulPropertyDataSize* \[在\]
</dt> <dd>

資料的大小（以位元組為單位）。

</dd> <dt>

*pbPropertiesData* \[在\]
</dt> <dd>

\[在中，大小 \_ 為 (ulPropertyDataSize) \]

8位不帶正負號的整數陣列，包含要加入的屬性資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

使用 **ICoNtextNode：： AddPropertyData** 來建立資料與內容節點之間的關聯。 若要稍後取出資料，請使用 [**ICoNtextNode：： GetPropertyData**](icontextnode-getpropertydata.md)。

筆墨分析器可能會刪除節點作為筆墨分析的一部分，除非確認內容節點 (請參閱 [**ICoNtextNode：： Confirm**](icontextnode-confirm.md)) 。 如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。

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

[**ICoNtextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**ICoNtextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**ICoNtextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**ICoNtextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**ICoNtextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> </dl>

 

 




