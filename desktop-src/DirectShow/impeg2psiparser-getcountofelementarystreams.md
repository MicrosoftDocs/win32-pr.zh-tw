---
description: IMpeg2PsiParser：： GetCountOfElementaryStreams 方法-會以 DirectShow SDK 的範例程式碼形式提供此方法的執行。 這不是支援的 DirectShow API。
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: IMpeg2PsiParser：： GetCountOfElementaryStreams 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfElementaryStreams
api_type:
- COM
api_location: ''
ms.openlocfilehash: e241697884a4b665c160dc9991e4cb7f02c76f1ba32bc7a0656515faf1117a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767378"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a>IMpeg2PsiParser：： GetCountOfElementaryStreams 方法

此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。 這不是支援的 DirectShow API。

方法會抓取 `GetCountOfElementaryStreams` 指定程式中的基本資料流程數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*wProgramNumber* \[在\]
</dt> <dd>

指定程式的 [程式 \_ 代碼] 欄位，如 PAT 所指定。

</dd> <dt>

*pwVal* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收程式中的基本資料流程數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT** 值。 可能的值包括（但不限於）下表所示的值。



| 傳回碼                                                                          | 描述         |
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

 

 




