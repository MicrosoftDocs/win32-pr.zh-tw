---
description: 取得解碼器物件（如果有的話）。
ms.assetid: b8a1c7c9-e7ac-4b0e-a342-5b923ab83df3
title: EncodedData 解碼方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Decoder
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 334895ed683d0c582628b4b623a7343ca561be22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990760"
---
# <a name="encodeddatadecoder-method"></a>EncodedData 解碼方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**AsnEncodedData 類別**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1)。\]

如果有一個解碼器物件存在， **則此方法** 會取得該物件。

## <a name="syntax"></a>語法


```VB
EncodedData.Decoder()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="remarks"></a>備註

如果編碼的資料沒有解碼器物件，則會傳回 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
