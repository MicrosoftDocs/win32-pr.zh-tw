---
description: 如果呼叫程式是在載入器標注中叫用，則此函式會強制結束通話程式。 否則，它不會有任何作用。
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: LdrFastFailInLoaderCallout 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrFastFailInLoaderCallout
api_type:
- DllExport
api_location:
- NTDll.dll
ms.openlocfilehash: f74b9cdc0aec666242a8267fab8d6255c75dc94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986175"
---
# <a name="ldrfastfailinloadercallout-function"></a>LdrFastFailInLoaderCallout 函式

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

如果呼叫程式是在載入器標注中叫用，則此函式會強制結束通話程式。 否則，它不會有任何作用。

## <a name="syntax"></a>語法


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此常式不會攔截所有可能的鎖死案例;載入器標注中的執行緒可能會取得鎖定，而載入器標注以外的某個執行緒則會保留相同的鎖定，並呼叫載入器。 換句話說，載入器鎖定和用戶端鎖定之間可能會有鎖定順序反轉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>Ntdll.dll .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>NTDll.dll</dt> </dl> |



 

 




