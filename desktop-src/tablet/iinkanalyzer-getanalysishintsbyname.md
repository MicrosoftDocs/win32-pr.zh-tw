---
description: 抓取所有附加至 IInkAnalyzer 並具有指定名稱的分析提示 ICoNtextNode 物件。
ms.assetid: 15269ee0-055c-424e-be49-945f47e8a77e
title: 'IInkAnalyzer：： GetAnalysisHintsByName 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHintsByName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 24c69cd1dd321b5f142fe07b7463941fc0944a2206f1f8d6baf0ebbe8459b6ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719190"
---
# <a name="iinkanalyzergetanalysishintsbyname-method"></a>IInkAnalyzer：： GetAnalysisHintsByName 方法

抓取所有附加至 [**IInkAnalyzer**](iinkanalyzer.md)並具有指定名稱的分析提示 [**ICoNtextNode**](icontextnode.md)物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetAnalysisHintsByName(
  [in]  BSTR          hintName,
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hintName* \[在\]
</dt> <dd>

要搜尋的提示名稱。

</dd> <dt>

*ppAnalysisHints* \[擴展\]
</dt> <dd>

分析提示會 [**ICoNtextNode**](icontextnode.md) [**IInkAnalyzer**](iinkanalyzer.md) 中具有指定名稱的物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md) 傳回值。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 *ppAnalysisHints* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。

 

如果沒有將這類分析提示節點附加至 [**IInkAnalyzer**](iinkanalyzer.md)，這個方法會傳回空集合。

分析提示節點是 [**ICoNtextNode**](icontextnode.md) ，其內容節點類型為 AnalysisHint (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [內容節點類型](context-node-types.md)) 。

若要將內容資訊加入至提示，請使用 [**ICoNtextNode：： AddPropertyData**](icontextnode-addpropertydata.md) ，並將 *pPropertyDataId* 參數設定為 [分析提示屬性](analysis-hint-properties.md) 常數中 (guid) 的其中一個全域唯一識別碼。

若要尋找內容節點上設定的屬性值，請使用 [**ICoNtextNode：： GetPropertyDataIds**](icontextnode-getpropertydataids.md)。 若要尋找屬性的值，請使用 [**ICoNtextNode：： GetPropertyData**](icontextnode-getpropertydata.md)。

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

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer：： CreateAnalysisHint 方法**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer：:D eleteAnalysisHint 方法**](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[**IInkAnalyzer：： GetAnalysisHints 方法**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

