---
description: IMpeg2PsiParser：： GetPatVersionNumber 方法-會以 DirectShow SDK 的範例程式碼形式提供此方法的執行。 這不是支援的 DirectShow API。
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: IMpeg2PsiParser：： GetPatVersionNumber 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: ffd03bea09fb9041b91bb214287442eb59a7101be7a8841e0d38e28bcdaf3ecb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767358"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a>IMpeg2PsiParser：： GetPatVersionNumber 方法

此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。 這不是支援的 DirectShow API。

`GetPatVersionNumber`方法會 \_ 從 PAT 抓取版本號碼欄位。 傳輸資料流程最多包含一個 PAT。 當資料表中的資訊變更時，版本號碼就會遞增。

## <a name="syntax"></a>語法


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPatVersion* \[擴展\]
</dt> <dd>

接收版本號碼欄位之變數的指標 \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT** 值。 可能的值包括（但不限於）下表所示的值。



| 傳回碼                                                                          | 描述         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMpeg2PsiParser 介面**](impeg2psiparser.md)
</dt> <dt>

[PSI 剖析器篩選範例](psi-parser-filter-sample.md)
</dt> </dl>

 

 




