---
description: 取得指定之全域唯一識別碼 (GUID) 的 ICoNtextNode 物件。
ms.assetid: b8340666-98ab-4d8c-93c7-58ed05ef30d2
title: 'IInkAnalyzer：： FindNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d3d7e6cd4b24b2cb0977284d62b2bad9e26a8d8944ebc653e22d97d0455d883f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967267"
---
# <a name="iinkanalyzerfindnode-method"></a>IInkAnalyzer：： FindNode 方法

取得指定之全域唯一識別碼 (GUID) 的 [**ICoNtextNode**](icontextnode.md) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT FindNode(
  [in]  const GUID         *pId,
  [out]       IContextNode **ppContextNodeFound
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pId* \[在\]
</dt> <dd>

[**ICoNtextNode**](icontextnode.md)物件的識別碼。

</dd> <dt>

*ppCoNtextNodeFound* \[擴展\]
</dt> <dd>

具有 *pId* 識別碼之 [**ICoNtextNode**](icontextnode.md)物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 *ppCoNtextNodeFound* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。

 

如果沒有這類 [**ICoNtextNode**](icontextnode.md) 物件做為 [**IInkAnalyzer**](iinkanalyzer.md) 根節點的子系，則會傳回 **Null** 。

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

[**IInkAnalyzer：： FindInkLeafNodes 方法**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**IInkAnalyzer：： FindInkLeafNodesForStrokes 方法**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer：： FindLeafNodes 方法**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesOfType 方法**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesOfTypeForStrokes 方法**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesOfTypeInSubTree 方法**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesWithCallBack 方法**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

