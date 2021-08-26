---
description: IMpeg2PsiParser：： GetRecordProgramNumber 方法-會以 DirectShow SDK 的範例程式碼形式提供此方法的執行。 這不是支援的 DirectShow API。
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: IMpeg2PsiParser：： GetRecordProgramNumber 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetRecordProgramNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: e42e991fc7e288fc36dafcd167fe21ffb4983baeeb34bbb80e1bf67981e24779
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083698"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a>IMpeg2PsiParser：： GetRecordProgramNumber 方法

此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。 這不是支援的 DirectShow API。

方法會抓取 `GetRecordProgramNumber` 指定程式的程式編號。

## <a name="syntax"></a>語法


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwIndex* \[在\]
</dt> <dd>

指定定義程式的 PAT 中的專案，從零編制索引。

</dd> <dt>

*pwVal* \[擴展\]
</dt> <dd>

\_從 PAT 接收程式編號欄位之變數的指標。

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

 

 




