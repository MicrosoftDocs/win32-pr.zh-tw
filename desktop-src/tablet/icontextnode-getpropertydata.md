---
description: 抓取特定識別碼的應用程式特定資料或其他屬性資料。
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: 'ICoNtextNode：： GetPropertyData 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 381d137dd73056a2a6f4c2e9cd3746f9f16c5b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690600"
---
# <a name="icontextnodegetpropertydata-method"></a>ICoNtextNode：： GetPropertyData 方法

抓取特定識別碼的應用程式特定資料或其他屬性資料。

## <a name="syntax"></a>語法


```C++
HRESULT GetPropertyData(
  [in]      const GUID  *pPropertyDataId,
  [in, out]       ULONG *pulPropertyDataSize,
  [out]           BYTE  **ppbPropertyData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPropertyDataId* \[在\]
</dt> <dd>

資料的識別碼。

</dd> <dt>

*pulPropertyDataSize* \[in、out\]
</dt> <dd>

資料的大小（以位元組為單位）。 未使用傳入的值。

</dd> <dt>

*ppbPropertyData* \[擴展\]
</dt> <dd>

8位不帶正負號的整數陣列的指標，其中包含屬性資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *ppbPropertyData* 的記憶體。

 

除了使用 [**ICoNtextNode：： AddPropertyData**](icontextnode-addpropertydata.md)來取得已加入的應用程式特定資料以外，這個方法還會用來抓取 [內容節點屬性](context-node-properties.md) 常數所描述的通用屬性。

字串類型屬性包括：

-   GUID \_ CNP \_ RECOGNIZEDSTRING
-   GUID \_ CNP \_ SHAPENAME
-   GUID \_ AHP \_ ANALYSISHINTNAME
-   GUID \_ AHP \_ PREFIXTEXT
-   GUID \_ AHP \_ SUFFIXTEXT
-   GUID \_ AHP 的 \_ 模擬

傳回值為 **WCHAR \** _。如果您將 \_ *ppbPropertyData* 參數轉換成 **WCHAR \**_ ，其傳回的長度為 `(length of the string + 1) _ sizeof(WCHAR)` 。

布林值類型屬性包括：

-   GUID \_ AHP \_ OVERRIDELANGUAGEID
-   GUID \_ AHP \_ COERCETOFACTOID
-   GUID \_ AHP \_ WORDMODE

傳回值是 **VARIANT \_ BOOL**。 如果您將 \* *ppbPropertyData* 參數轉換成 **VARIANT \_ BOOL \** _ 其傳回的長度為 `sizeof(VARIANT_BOOL)` 。

GUID \_ AHP \_ 指南是一個指南型別屬性。 傳回值為 _*InkAnalysisRecognitionGuide \**_。 如果您將 \_ *ppbPropertyData* 參數轉換成 **InkAnalysisRecognitionGuide \** _ 其傳回的長度為 `sizeof(InkAnalysisRecognitionGuide)` 。

整數類型屬性包括：

-   GUID \_ CNP \_ LINENUMBER
-   GUID \_ CNP \_ POINTSPERINCH
-   GUID \_ CNP \_ CONFIDENCELEVEL
-   GUID \_ CNP \_ 確認
-   GUID \_ CNP \_ MAXIMUMSTROKECOUNT
-   GUID \_ CNP \_ 分割
-   GUID \_ CNP \_ ALIGNMENTLEVEL

傳回值為 _*LONG \**_。 如果您將 \_ *ppbPropertyData* 參數轉換成 **LONG \** _ 其傳回的長度為 `sizeof(LONG)` 。

明細度量-類型屬性包括：

-   GUID \_ CNP \_ ASCENDERS
-   GUID \_ CNP \_ 下行
-   GUID \_ CNP \_ 基準
-   GUID \_ CNP \_ 中線

傳回值為 _*LONG \**_。 如果您將 \_ *ppbPropertyData* 參數轉換成 **LONG \** _ 其傳回的長度是，則表示 `sizeof(LONG)_4` 起始點的 (x，y) 值，後面接著 (x，y) 值的結束點。

GUID \_ CNP \_ TEXTRECOGNIZERID 是 **guid** 屬性。 傳回值為 **GUID \** _。如果您將 \_ *ppbPropertyData* 參數轉換成 **GUID \**_ ，則其傳回的長度為 `sizeof(GUID)` 。

GUID \_ CNP \_ ROTATEDBOUNDINGBOX 是旋轉周框方塊屬性。 傳回值為 _*LONG \**_。 如果您將 \_ *ppbPropertyData* 參數轉換成 **LONG \** _ 其傳回的長度是，表示方塊 `sizeof(LONG)_8` 四個角落的 (x，y) 值。

GUID \_ CNP \_ HOTPOINT 是作用點屬性。 傳回值為 **LONG \** _。如果您將 \_ *ppbPropertyData* 參數轉換成 **LONG \**_ ，其傳回的長度為 `sizeof(LONG)_2` ，表示該點的 (x，y) 值。

GUID \_ AHP \_ 單詞表是一個字組清單屬性。 傳回值為 **WCHAR \** _。如果您將 \_ *ppbPropertyData* 參數轉換成 **WCHAR \**_ ，其傳回的長度是 `n _ sizeof(WCHAR)` ，其中 `n` 是清單中字串數目的總和，加上每個字串的每個 **Null** 終止字元的字串長度。

## <a name="examples"></a>範例

此範例顯示存取段落內容節點類型之 AlignmentLevel 內容節點屬性的方法。


```C++
// Checks a paragraph context node's alignment level property.
// Only paragraph type context nodes contain the alignment level property.
HRESULT CMyClass::ExploreParagraphNode(
    IContextNode *pParagraphNode)
{
    // Get the AlignmentLevel property data for the paragraph.
    LONG * alignmentLevel = NULL;
    ULONG ulDataLen = 0;

    HRESULT hr = pParagraphNode->GetPropertyData(
        (const GUID*)&GUID_CNP_ALIGNMENTLEVEL,
        &ulDataLen,
        (BYTE**)&alignmentLevel);

    if( FAILED(hr) ||
        ulDataLen != sizeof(LONG) ||
        alignmentLevel == NULL )
    {
        // Insert code that handles an error here.
    }
    else
    {
        // Insert code that uses the alignment level here.
    }

    // Free the memory allocated for the property data.
    ::CoTaskMemFree(alignmentLevel);

    return hr;
}
```



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

[**ICoNtextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**ICoNtextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**ICoNtextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**ICoNtextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**ICoNtextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**ICoNtextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

