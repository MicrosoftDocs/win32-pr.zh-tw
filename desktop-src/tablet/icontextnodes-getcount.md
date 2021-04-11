---
description: 抓取此集合中包含的 ICoNtextNode 物件數目。
ms.assetid: 7cc60bea-9a4c-4ac8-ad1a-0fca5e941c5e
title: 'ICoNtextNodes：： GetCount 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8d694849b3436f9f30a687579362d01a111ace80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113368"
---
# <a name="icontextnodesgetcount-method"></a>ICoNtextNodes：： GetCount 方法

抓取此集合中包含的 [**ICoNtextNode**](icontextnode.md) 物件數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pulCount* \[擴展\]
</dt> <dd>

這個集合中所包含的 [**ICoNtextNode**](icontextnode.md) 物件數目。

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

 

 




