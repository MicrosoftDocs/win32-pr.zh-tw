---
description: 更新此 ICoNtextNode 的區域。
ms.assetid: e7001411-17e4-4f33-af04-dd3220275895
title: 'ICoNtextNode：： SetLocation 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 20daefeab7a9e36d5e968d5d14bfa5110d733487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971415"
---
# <a name="icontextnodesetlocation-method"></a>ICoNtextNode：： SetLocation 方法

更新此 [**ICoNtextNode**](icontextnode.md)的區域。

## <a name="syntax"></a>語法


```C++
HRESULT SetLocation(
  [in] IAnalysisRegion *pIAnalysisRegion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pIAnalysisRegion* \[在\]
</dt> <dd>

[**IAnalysisRegion**](ianalysisregion.md) ，描述要設定 [**ICoNtextNode**](icontextnode.md)物件位置的區域。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

使用這個方法來更新內容節點的位置 (參閱 [**ICoNtextNode：： GetLocation**](icontextnode-getlocation.md)) 。

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

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**ICoNtextNode::GetLocation**](icontextnode-getlocation.md)
</dt> <dt>

[**ICoNtextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




