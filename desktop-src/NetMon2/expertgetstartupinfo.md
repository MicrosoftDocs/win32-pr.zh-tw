---
description: ExpertGetStartupInfo 函式會抓取專家的啟動設定資訊。
ms.assetid: 15f080ed-50b7-40c6-b283-dbe416a2b0e9
title: 'ExpertGetStartupInfo 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetStartupInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f34ecc3d0c3eeb085d2a7c0f8c4cb0426663093c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386102"
---
# <a name="expertgetstartupinfo-function"></a>ExpertGetStartupInfo 函式

**ExpertGetStartupInfo** 函式會抓取專家的啟動設定資訊。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI ExpertGetStartupInfo(
  _In_  HEXPERTKEY         hExpertKey,
  _Out_ PEXPERTSTARTUPINFO pExpertStartupInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hExpertKey* \[在\]
</dt> <dd>

獨特的專家識別碼。 網路監視器在呼叫 [Run](run.md)函式時，將 *hExpertKey* 傳遞給專家。

</dd> <dt>

*pExpertStartupInfo* \[擴展\]
</dt> <dd>

包含啟動資訊之 [EXPERTSTARTUPINFO](expertstartupinfo.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值為 NMERR。

## <a name="remarks"></a>備註

如果專家必須判斷所使用的啟動資訊，則會使用 **ExpertGetStartupInfo** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




