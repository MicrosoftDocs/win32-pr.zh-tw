---
description: 抓取位於指定之索引處的 ICoNtextLink。
ms.assetid: 46bb71b9-5ef3-4756-97f6-40e0aaa82826
title: 'ICoNtextLinks：： GetCoNtextLink 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ecc0ed9ba457a7a91cb2e1b615ac7419ce5a94c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113393"
---
# <a name="icontextlinksgetcontextlink-method"></a>ICoNtextLinks：： GetCoNtextLink 方法

抓取位於指定之索引處的 [**ICoNtextLink**](icontextlink.md) 。

## <a name="syntax"></a>語法


```C++
HRESULT GetContextLink(
  [in]  ULONG        ulIndex,
  [out] IContextLink **ppContextLink
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ulIndex* \[在\]
</dt> <dd>

要取得之 [**ICoNtextLink**](icontextlink.md) 物件的以零為基底的索引。

</dd> <dt>

*ppCoNtextLink* \[擴展\]
</dt> <dd>

位於指定索引處之 [**ICoNtextLink**](icontextlink.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 ppCoNtextLink 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （ \* 當您不再需要使用內容連結時）。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextLinks**](icontextlinks.md)
</dt> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

