---
description: 傳回編碼資料的字串表示。
ms.assetid: d1231e6d-57d7-4b5a-ab37-d4ee1b29cf25
title: EncodedData 格式方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Format
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b3d4316a2de24410a14d496b71e46746ea580109f8d6ede10c4c1a0f57fc22f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874868"
---
# <a name="encodeddataformat-method"></a>EncodedData 格式方法

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**AsnEncodedData 類別**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1)。\]

**Format** 方法會傳回已編碼資料的字串表示。

## <a name="syntax"></a>語法


```VB
EncodedData.Format( _
  [ ByVal bMultiLines ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*bMultiLines* \[在中，選擇性\]
</dt> <dd>

布林值，指出傳回的字串是否包含多行。 若 **為 True**，則傳回的字串可能包含多個以 **vbCrLf** 分隔的行。 預設值為 **[False]** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

人們可讀取的字串，表示已編碼的資料。 如果 CAPICOM 無法理解編碼的資料，就會傳回資料的十六進位標記法。

## <a name="remarks"></a>備註

傳回字串的格式可能會在不同版本的 CAPICOM 之間變更。 請勿依賴您應用程式中的任何特定格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EncodedData**](encodeddata.md)
</dt> </dl>

 

 
