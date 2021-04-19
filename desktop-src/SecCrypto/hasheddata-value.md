---
description: 在成功呼叫 Hash 方法之後，取得雜湊的資料。
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: HashedData。 Value 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 496bdd76400c746ae3209a2e3c99b6cf4e5bc4b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982943"
---
# <a name="hasheddatavalue-property"></a>HashedData。 Value 屬性

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**HashAlgorithm 類別**](/previous-versions/windows/)。\]

**Value** 屬性會在成功呼叫 [**Hash**](hasheddata-hash.md)方法之後，取得雜湊的資料。 雜湊值會以十六進位格式傳回。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
HashedData.Value As String
```



## <a name="property-value"></a>屬性值

字串，包含十六進位格式的雜湊資料。

## <a name="remarks"></a>備註

若要建立大量資料的雜湊，請呼叫每個資料片段的 [**雜湊**](hasheddata-hash.md) 方法。 在讀取屬性之前，會將每個資料片段的雜湊串連至 **Value** 屬性。 當讀取屬性時，會重設 **Value** 屬性的內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**HashedData**](hasheddata.md)
</dt> </dl>

 

 
