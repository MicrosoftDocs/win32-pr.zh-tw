---
description: 釋放 \_ \_ 透過 ChainCoNtext 屬性取得的 PCCERT 鏈內容。
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: IChainCoNtext：： FreeCoNtext 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.FreeContext
- ChainContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 10a6d0576cefd1c28e8f05fe455b89be90dcd36386b4312ef1921511616bce2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005486"
---
# <a name="ichaincontextfreecontext-method"></a>IChainCoNtext：： FreeCoNtext 方法

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。\]

**FreeCoNtext** 方法會釋放 \_ \_ 透過 [**ChainCoNtext**](ichaincontext-chaincontext.md)屬性取得的 PCCERT 鏈內容。

## <a name="syntax"></a>語法


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a>參數

<dl> <dt>

*pChainCoNtext* \[在\]
</dt> <dd>

\_要釋放的 PCCERT 鏈 \_ 內容。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT**。 S 的值 \_ 表示成功。 任何其他值則表示作業失敗。

## <a name="remarks"></a>備註

這個方法不會釋放 \_ \_ [**連鎖**](chain.md) 物件內所包含的 PCCERT 鏈內容。 它只能用來釋放 \_ \_ 透過 [**ChainCoNtext**](ichaincontext-chaincontext.md) 屬性取得的 PCCERT 鏈內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IChainCoNtext**](ichaincontext.md)
</dt> </dl>

 

 




