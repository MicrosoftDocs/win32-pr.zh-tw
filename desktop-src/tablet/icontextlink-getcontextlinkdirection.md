---
description: 抓取這個 ICoNtextLink 所代表的關聯性類型。
ms.assetid: 03c13eba-1493-4fb7-b684-f15147e5a0eb
title: 'ICoNtextLink：： GetCoNtextLinkDirection 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetContextLinkDirection
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 96506836e89f4bb2f8b202373df09b5cc6ee1c7f6e9e01f3b68bb2bbe2c8b56a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057908"
---
# <a name="icontextlinkgetcontextlinkdirection-method"></a>ICoNtextLink：： GetCoNtextLinkDirection 方法

抓取這個 [**ICoNtextLink**](icontextlink.md) 所代表的關聯性類型。

## <a name="syntax"></a>語法


```C++
HRESULT GetContextLinkDirection(
  [out] ContextLinkDirection *pContextLinkDirection
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCoNtextLinkDirection* \[擴展\]
</dt> <dd>

此 [**ICoNtextLink**](icontextlink.md) 所代表的方向。

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

[**ICoNtextLink**](icontextlink.md)
</dt> <dt>

[**CoNtextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




