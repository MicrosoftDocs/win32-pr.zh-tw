---
description: IInkAnalyzer：： Search 方法-提供模糊、不區分大小寫片語的搜尋，以供分析的寫入筆劃和已分析的繪圖筆劃具有辨識的類型。
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: 'IInkAnalyzer：： Search 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Search
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 94ccdebf8c8a134a845ff3df3017d710d1da93f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113726"
---
# <a name="iinkanalyzersearch-method"></a>IInkAnalyzer：： Search 方法

提供模糊、不區分大小寫片語的搜尋，以供分析的書寫筆劃和已分析的繪圖筆劃具有可辨識的類型。

## <a name="syntax"></a>語法


```C++
HRESULT Search(
  [in]      BSTR  bstrPhraseToMatch,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrPhraseToMatch* \[在\]
</dt> <dd>

將在替代中針對目前分析之筆劃找到的片語。

</dd> <dt>

*pulSearchResultCount* \[in、out\]
</dt> <dd>

從搜尋傳回的結果數目上限。

</dd> <dt>

*ppulStrokeCountPerResult* \[擴展\]
</dt> <dd>

每個搜尋結果中筆劃數目陣列的指標。

</dd> <dt>

*pulStrokeIdsCount* \[in、out\]
</dt> <dd>

*PpulStrokeIds* 中的筆觸識別碼數目。

</dd> <dt>

*ppulStrokeIds* \[擴展\]
</dt> <dd>

筆觸識別碼陣列的指標，代表一組筆觸。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

此搜尋會尋找多單字和單一單字子字串。 系統會搜尋替代辨識結果和替代 segmentations。

所有傳入的字串都會轉換成單一大小寫，以利用目前線程的 LCID 來進行這項轉換，以遵循文化特性案例慣例。

傳遞的字串會被視為片語。 單字和字元必須以指定的順序出現在筆劃的 alterantes 中。 片語的第一個和最後一個單字可能會以子字串的形式來比對， (第一個出現在替代的單字和最後一個單字的 begginging 出現在其中一個) ，但是任何其他文字 (片語內的單字) 必須顯示為全字。

如果傳入的字串在字元之間沒有空白字元，則可以在替代的單一單字內的任何位置找到子字串。

只有字元之間存在空格才會變更搜尋結果。 未以字元括住的空白字元會被忽略。 空白字元的類型會被忽略 (索引標籤或字元之間的空格會提供相同的結果) 。 空白字元的數量並不重要-字元之間的一個空格或兩個空格將提供相同的結果。

搜尋不會產生 PopulateCoNtextNode 事件。 只會搜尋已填入的筆劃。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> </dl>

 

 




