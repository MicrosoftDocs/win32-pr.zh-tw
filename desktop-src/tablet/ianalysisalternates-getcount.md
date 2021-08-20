---
description: 捕獲 IAnalysisAlternates 集合中包含的 IAnalysisAlternate 物件數目。
ms.assetid: 17b71b5a-638a-4e6e-a43b-4ca3c8eba257
title: 'IAnalysisAlternates：： GetCount 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 84ff5941d4db6ca569c8a7a10a622e4b3dcdfc947284064fa009e030adae1493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967487"
---
# <a name="ianalysisalternatesgetcount-method"></a>IAnalysisAlternates：： GetCount 方法

捕獲 [**IAnalysisAlternates**](ianalysisalternates.md)集合中包含的 [**IAnalysisAlternate**](ianalysisalternate.md)物件數目。

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

不帶正負號的32位整數，設定為包含在 [**IAnalysisAlternates**](ianalysisalternates.md)集合中的 [**IAnalysisAlternate**](ianalysisalternate.md)物件數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




