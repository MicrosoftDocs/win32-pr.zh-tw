---
description: 取得字型特性。
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: 'ID3DX10Font：： GetTextMetrics 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetTextMetrics
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 97cbddc59dd84d0a5b83610212fe94e87a49757da0430d64cb420280c815d9cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047046"
---
# <a name="id3dx10fontgettextmetrics-method"></a>ID3DX10Font：： GetTextMetrics 方法

取得字型特性。

## <a name="syntax"></a>語法


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTextMetrics* \[在\]
</dt> <dd>

類型： **TEXTMETRIC \***

[TEXTMETRIC](/previous-versions//ms534202(v=vs.85))結構的指標，其中包含字型屬性。 如果已定義 Unicode，函數會傳回 TEXTMETRICW 結構。 否則，函數會傳回 TEXTMETRICA 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

如果函式成功則為非零，否則為 0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
