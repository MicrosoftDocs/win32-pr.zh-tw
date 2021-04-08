---
description: 抓取代表資料區塊的 PROPVARIANT 和輸入字串。 呼叫這個方法與呼叫的方法相同。
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: IRichChunk：： RemoteGetData 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRichChunk.RemoteGetData
api_type:
- COM
api_location: ''
ms.openlocfilehash: 002c85b189a3994b70795c05228ae5331c610284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112389"
---
# <a name="irichchunkremotegetdata-method"></a>IRichChunk：： RemoteGetData 方法

抓取代表資料區塊的 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 和輸入字串。 呼叫這個方法與呼叫的方法相同 [**。**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata)

## <a name="syntax"></a>語法


```C++
HRESULT RemoteGetData(
  [out] ULONG       *pFirstPos,
  [out] ULONG       *pLength,
  [out] LPWSTR      *ppsz,
  [out] PROPVARIANT *pValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFirstPos* \[擴展\]
</dt> <dd>

接收範圍的以零為基底的開始位置。 此參數可以是 **Null**。

</dd> <dt>

*pLength* \[擴展\]
</dt> <dd>

接收範圍的長度。 此參數可以是 **Null**。

</dd> <dt>

*ppsz* \[擴展\]
</dt> <dd>

接收相關聯的 Unicode 字串值，如果無法使用，則 **為 Null** 。

</dd> <dt>

*pValue* \[擴展\]
</dt> <dd>

如果無法使用，則會接收相關聯的 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 值或 **VT \_ 空白** 。 此參數可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
