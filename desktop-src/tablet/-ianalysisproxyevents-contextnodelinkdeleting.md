---
description: 在 IInkAnalyzer 刪除兩個 ICoNtextNode 物件之間的 ICoNtextLink 物件之前發生。
ms.assetid: bc9716b8-8793-4886-aff4-d880024129a6
title: '_IAnalysisProxyEvents：： CoNtextNodeLinkDeleting 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc4ba9586fc4c520b9ee44b039bd56f8ef2ade3c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195791"
---
# <a name="_ianalysisproxyeventscontextnodelinkdeleting-event"></a>\_IAnalysisProxyEvents：： CoNtextNodeLinkDeleting 事件

在 [**IInkAnalyzer**](iinkanalyzer.md)刪除兩個 [**ICoNtextNode**](icontextnode.md)物件之間的 [**ICoNtextLink**](icontextlink.md)物件之前發生。

## <a name="syntax"></a>語法


```C++
HRESULT ContextNodeLinkDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeDeleted
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInkAnalyzer* \[在\]
</dt> <dd>

刪除連結的 [**IInkAnalyzer**](iinkanalyzer.md) 。

</dd> <dt>

*pCoNtextLinkToBeDeleted* \[在\]
</dt> <dd>

要刪除的 [**ICoNtextLink**](icontextlink.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。 此事件發生于筆墨分析的協調階段，或為了回應從 [**ICoNtextNode**](icontextnode.md)移除 [**ICoNtextLink**](icontextlink.md)的 **IInkAnalyzer** 方法。

如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**ICoNtextLink**](icontextlink.md)
</dt> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




