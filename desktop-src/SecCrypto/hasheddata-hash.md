---
description: 建立指定之字串的雜湊。
ms.assetid: 8d3e16e7-7b93-410c-b771-7684d1bf2160
title: HashedData 雜湊方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Hash
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d36973340a7dbf67f8a8b0d1aa4cd5738ef97d74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990122"
---
# <a name="hasheddatahash-method"></a>HashedData 雜湊方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**HashAlgorithm 類別**](/previous-versions/windows/)。\]

**雜湊** 方法會建立指定之字串的雜湊。

## <a name="syntax"></a>語法


```VB
HashedData.Hash( _
  ByVal newVal _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*newVal* 
</dt> <dd>

包含要雜湊之值的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

若要建立大量資料的雜湊，請呼叫每個資料片段的 **雜湊** 方法。 在讀取屬性之前，會將每個資料片段的雜湊串連至 [**Value**](hasheddata-value.md) 屬性。 當讀取屬性時，會重設 **Value** 屬性的內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
