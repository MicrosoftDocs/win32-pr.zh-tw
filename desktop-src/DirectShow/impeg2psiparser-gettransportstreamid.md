---
description: IMpeg2PsiParser：： GetTransportStreamId 方法-此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。 這不是支援的 DirectShow API。
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: IMpeg2PsiParser：： GetTransportStreamId 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetTransportStreamId
api_type:
- COM
api_location: ''
ms.openlocfilehash: a24253b021abacf398a3a169b63bbb2f01ec2354
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084566"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a>IMpeg2PsiParser：： GetTransportStreamId 方法

此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。 這不是支援的 DirectShow API。

`GetTransportStreamId`方法會 \_ 從 PAT 抓取傳輸資料流程 \_ 識別碼欄位。 這個值是由使用者定義，可用來區別特定的傳輸資料流程與相同網路上的其他資料流程。 傳輸資料流程最多包含一個 PAT。

## <a name="syntax"></a>語法


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStreamId* \[擴展\]
</dt> <dd>

接收傳輸 \_ 資料流程識別碼欄位之變數的指標 \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT** 值。 可能的值包括（但不限於）下表所示的值。



| 傳回碼                                                                          | Description         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMpeg2PsiParser 介面**](impeg2psiparser.md)
</dt> <dt>

[PSI 剖析器篩選範例](psi-parser-filter-sample.md)
</dt> </dl>

 

 




