---
description: 指定 ICoNtextNode 物件上可能發生的確認類型。
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: 'ConfirmationType 列舉 (IACom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfirmationType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 2c43971c6ccf44513c11e46d4bc5db86d973d7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972162"
---
# <a name="confirmationtype-enumeration"></a>ConfirmationType 列舉

指定 [**ICoNtextNode**](icontextnode.md) 物件上可能發生的確認類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum ConfirmationType { 
  ConfirmationType_None                   = 0,
  ConfirmationType_NodeTypeAndProperties  = 1,
  ConfirmationType_TopBoundary            = 4
} ConfirmationType;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType \_ 無**
</dt> <dd>

未套用任何確認。 [**IInkAnalyzer**](iinkanalyzer.md)可以視需要隨時變更內容節點或任何其子系。

</dd> <dt>

<span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType \_ NodeTypeAndProperties**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md)無法變更指定之內容節點的類型或任何屬性。

</dd> <dt>

<span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType \_ TopBoundary**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md)將不會執行作業，包括新增筆墨或與其他 [**CoNtextNodes**](icontextnodes.md)合併，而導致 TopBoundary 移至目前的上方界限之外。 例如：

-   應用程式會分析一組筆墨，並識別出 ParagraphNode。
-   應用程式會確認此段落的 TopBoundary。
-   應用程式的使用者會將新筆墨寫入目前的段落上方。 再次呼叫 [分析] 時，新的筆墨將不會併入確認的段落節點。
-   因為只確認最上層界限，所以 CoNtextNode 可以繼續以其他方向成長。 刪除筆劃可能會導致頂端界限下移。 轉譯 CoNtextNode 可能會導致位置變更，但不允許將其他筆墨合併到新的位置。

此 ConfirmationType 僅適用于段落節點。

</dd> </dl>

## <a name="remarks"></a>備註

您只能將 **NodeTypeAndProperties** 值用於筆墨單字和筆墨繪圖節點 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。 否則，會從 [**ICoNtextNode：： Confirm**](icontextnode-confirm.md)傳回 **E \_ INVALIDARG** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextNode：： Confirm**](icontextnode-confirm.md)
</dt> <dt>

[**ICoNtextNode::IsConfirmed**](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




