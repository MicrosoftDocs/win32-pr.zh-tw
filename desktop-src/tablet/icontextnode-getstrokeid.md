---
description: 抓取 ICoNtextNode 物件內索引值所參考之筆劃的筆觸識別碼。
ms.assetid: faac142e-cac1-45f9-9b40-76c50ac7006b
title: 'ICoNtextNode：： GetStrokeId 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b193b3719ac6b67284e3ff8c4297455888f6c9cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690599"
---
# <a name="icontextnodegetstrokeid-method"></a>ICoNtextNode：： GetStrokeId 方法

抓取 [**ICoNtextNode**](icontextnode.md) 物件內索引值所參考之筆劃的筆觸識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetStrokeId(
  [in]  ULONG ulIndex,
  [out] LONG  *plStrokeId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ulIndex* \[在\]
</dt> <dd>

要傳回之筆劃的索引。

</dd> <dt>

*plStrokeId* \[擴展\]
</dt> <dd>

目前 [**ICoNtextNode**](icontextnode.md)物件內 *ulIndex* 參數所參考之筆劃的筆觸識別碼。

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

[**ICoNtextNode::GetStrokeIds**](icontextnode-getstrokeids.md)
</dt> <dt>

[**ICoNtextNode::GetStrokeCount**](icontextnode-getstrokecount.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




