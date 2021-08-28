---
description: 建立 ICoNtextNodes 物件。
ms.assetid: d6d37595-307b-4cbc-9d48-ad10f8b272dd
title: 'IInkAnalyzer：： CreateCoNtextNodes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4663493e6847ac3904916c93220386c6db13f0ef27fc60b36e048852b6cf0b00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967297"
---
# <a name="iinkanalyzercreatecontextnodes-method"></a>IInkAnalyzer：： CreateCoNtextNodes 方法

建立 [**ICoNtextNodes**](icontextnodes.md) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT CreateContextNodes(
  [out] IContextNodes **ppContextNodes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppCoNtextNodes* \[擴展\]
</dt> <dd>

[**ICoNtextNodes**](icontextnodes.md)物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 *ppCoNtextNodes* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。

 

您可以使用這個方法來建立與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯的空 [**ICoNtextNodes**](icontextnodes.md)集合。 新的 **ICoNtextNodes** 集合不是 **IInkAnalyzer** 物件的內容樹狀結構的一部分。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**ICoNtextNodes**](icontextnodes.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

