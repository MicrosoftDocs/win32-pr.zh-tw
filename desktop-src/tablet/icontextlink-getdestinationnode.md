---
description: 抓取 ICoNtextNode 物件，此物件為這個 ICoNtextLink 的目的地。
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: 'ICoNtextLink：： GetDestinationNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetDestinationNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 86d34bfcca39f7df9d9010e8dae32747ca8f1d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318467"
---
# <a name="icontextlinkgetdestinationnode-method"></a>ICoNtextLink：： GetDestinationNode 方法

抓取 [**ICoNtextNode**](icontextnode.md) 物件，此物件為這個 [**ICoNtextLink**](icontextlink.md)的目的地。

## <a name="syntax"></a>語法


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppDstCoNtextNodeId* \[擴展\]
</dt> <dd>

[**ICoNtextNode**](icontextnode.md)物件的指標，該物件是這個 [**ICoNtextLink**](icontextlink.md)的目的地。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用目的地節點時，請在 *ppDstCoNtextNodeId* 上呼叫 IUnknown：： Release。

 

如果 [**ICoNtextLink**](icontextlink.md) 物件是在包含撰寫的節點和包含繪圖的節點之間進行連結，則目的地節點通常是包含寫入的節點。

如果 ICoNtextLink 物件的連結 (類型是 [](icontextlink.md) ，請參閱 [**ICoNtextLink：： GetCoNtextLinkDirection**](icontextlink-getcontextlinkdirection.md)) ，目的節點是包含的 [**ICoNtextNode**](icontextnode.md)物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextLink**](icontextlink.md)
</dt> <dt>

[**ICoNtextLink::GetSourceNode**](icontextlink-getsourcenode.md)
</dt> <dt>

[**CoNtextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

