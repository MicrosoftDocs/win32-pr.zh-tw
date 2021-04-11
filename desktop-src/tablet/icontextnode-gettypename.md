---
description: 抓取這個 ICoNtextNode 的人們看得懂的型別名稱。
ms.assetid: 02031efd-1e9c-4e96-8dc1-280cc1a6e58f
title: 'ICoNtextNode：： GetTypeName 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetTypeName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9d7bc4a24b7abc3ee507d7bda0c547f4c55a787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113376"
---
# <a name="icontextnodegettypename-method"></a>ICoNtextNode：： GetTypeName 方法

抓取這個 [**ICoNtextNode**](icontextnode.md)的人們看得懂的型別名稱。

## <a name="syntax"></a>語法


```C++
HRESULT GetTypeName(
  [out] BSTR *pbstrContextNodeType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbstrCoNtextNodeType* \[擴展\]
</dt> <dd>

這個 [**ICoNtextNode**](icontextnode.md)的人們可讀取型別名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) \* 當您不再需要使用字串時，請在 *pbstrCoNtextNodeType* 上呼叫 SysFreeString。

 

例如，這個方法會將筆墨單位元組點的 *pbstrCoNtextNodeType* 設定為 "InkWordNode"， (查看 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [內容節點類型](context-node-types.md)) 。

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

[**ICoNtextNode：： GetType**](icontextnode-gettype.md)
</dt> <dt>

[內容節點類型](context-node-types.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

