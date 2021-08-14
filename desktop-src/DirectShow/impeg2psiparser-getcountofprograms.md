---
description: IMpeg2PsiParser：： GetCountOfPrograms 方法-會以 DirectShow SDK 的範例程式碼形式提供此方法的執行。 這不是支援的 DirectShow API。
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: IMpeg2PsiParser：： GetCountOfPrograms 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfPrograms
api_type:
- COM
api_location: ''
ms.openlocfilehash: c0c5609f82db98caea02e08f1e4fbd3877eeccbae25a5e83da3ac2804577b100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398105"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a>IMpeg2PsiParser：： GetCountOfPrograms 方法

此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。 這不是支援的 DirectShow API。

`GetCountOfPrograms`方法會捕獲傳輸資料流程中的程式數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNumOfPrograms* \[擴展\]
</dt> <dd>

接收程式數目之變數的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 HRESULT 值。 可能的值包括（但不限於）下表所示的值。



| 傳回碼                                                                          | Description         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMpeg2PsiParser 介面**](impeg2psiparser.md)
</dt> <dt>

[PSI 剖析器篩選範例](psi-parser-filter-sample.md)
</dt> </dl>

 

 




