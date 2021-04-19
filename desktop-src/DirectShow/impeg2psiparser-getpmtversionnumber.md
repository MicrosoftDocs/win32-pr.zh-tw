---
description: 此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。 這不是支援的 DirectShow API。
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: IMpeg2PsiParser：： GetPmtVersionNumber 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPmtVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3af4b20067af52216181848f4cc63ac5a7784ba9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106984538"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a>IMpeg2PsiParser：： GetPmtVersionNumber 方法

此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。 這不是支援的 DirectShow API。

`GetPmtVersionNumber`方法會 \_ 從指定的 PMT 抓取版本號碼欄位。 當程式的定義變更時，版本號碼就會遞增。

## <a name="syntax"></a>語法


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*wProgramNumber* \[在\]
</dt> <dd>

指定程式的 [程式 \_ 代碼] 欄位，如 PAT 所指定。

</dd> <dt>

*pPmtVersion* \[擴展\]
</dt> <dd>

接收版本號碼欄位之變數的指標 \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT** 值。 可能的值包括（但不限於）下表所示的值。



| 傳回碼                                                                          | Description         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 成功。<br/> |



 

## <a name="remarks"></a>備註

使用 **GetRecordProgramNumber** 方法來取得程式編號。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMpeg2PsiParser 介面**](impeg2psiparser.md)
</dt> <dt>

[**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[PSI 剖析器篩選範例](psi-parser-filter-sample.md)
</dt> </dl>

 

 




