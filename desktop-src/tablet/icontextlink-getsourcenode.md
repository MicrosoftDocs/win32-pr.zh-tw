---
description: 抓取 ICoNtextNode 物件，此物件為這個 ICoNtextLink 的來源。
ms.assetid: 2f55ae9c-9f63-4d49-9bf0-9e169b819e79
title: 'ICoNtextLink：： GetSourceNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetSourceNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 609f3012608586f7e6c3279cd0dab4232f58ca3e0e31145124622e87684e06f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940408"
---
# <a name="icontextlinkgetsourcenode-method"></a>ICoNtextLink：： GetSourceNode 方法

抓取 [**ICoNtextNode**](icontextnode.md) 物件，此物件為這個 [**ICoNtextLink**](icontextlink.md)的來源。

## <a name="syntax"></a>語法


```C++
HRESULT GetSourceNode(
  [out] IContextNode **ppSrcContextNodeId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppSrcCoNtextNodeId* \[擴展\]
</dt> <dd>

[**ICoNtextNode**](icontextnode.md)物件的指標，該物件為此 [**ICoNtextLink**](icontextlink.md)的來源。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用來源節點時，請在 *ppSrcCoNtextNodeId* 上呼叫 IUnknown：： Release。

 

如果 [**ICoNtextLink**](icontextlink.md) 物件是在包含撰寫的節點和包含繪圖的節點之間進行連結，則來源節點通常是包含繪圖的節點。

如果 ICoNtextLink 物件的連結 (類型是 [](icontextlink.md) ，請參閱 [**ICoNtextLink：： GetCoNtextLinkDirection**](icontextlink-getcontextlinkdirection.md)) ，來源節點是包含目的地節點的節點。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextLink**](icontextlink.md)
</dt> <dt>

[**ICoNtextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)
</dt> <dt>

[**CoNtextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

