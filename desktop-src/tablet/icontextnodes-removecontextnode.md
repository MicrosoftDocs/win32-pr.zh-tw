---
description: 從此集合移除 ICoNtextNode 物件。
ms.assetid: ddda506d-4e39-486d-ac7d-211dc7869a73
title: 'ICoNtextNodes：： RemoveCoNtextNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.RemoveContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 371722cca3d8ccc132c151b37e9d1a469bdb0c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972643"
---
# <a name="icontextnodesremovecontextnode-method"></a>ICoNtextNodes：： RemoveCoNtextNode 方法

從此集合移除 [**ICoNtextNode**](icontextnode.md) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT RemoveContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCoNtextNode* \[在\]
</dt> <dd>

要移除的 [**ICoNtextNode**](icontextnode.md) 物件。

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

[**ICoNtextNodes**](icontextnodes.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




